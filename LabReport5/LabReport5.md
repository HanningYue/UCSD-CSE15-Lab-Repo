# LabReport 5

## Part One : 
### What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

> MacOS, Visual Studio Code, VSCode terminal

### Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

> The `Main.java` program is expected to read the `data.csv` file line by line, then split each line into two numbers. Then perform a division operation with the first number being the dividend and the second number the divisor, and then print the result of each operation. But this is given me the following errors :

> <img width="527" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/f845022d-200e-449a-8278-d91a9c0ad3d3">


### Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

> This is the `Main.java` file : 
> <img width="1005" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/11daabd2-3ead-481e-b102-e96607a404f8">

> This is the `data.csv` file : \
> <img width="131" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/2b637463-16e4-4a26-9f78-2bb5652c11db">

> This is the `script.sh` file : \
> <img width="382" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/c6222ba1-068b-4c24-86e3-36a5b98e8f1f">


## Part Two:
### Response from a TA asking a leading question or suggesting a command to try : 
> TA: "Your program throws an ArithmeticException when it tries to execute the division operation. Can you think of any special cases in division operation that your program should handle but currently doesn't?"

> Also, could you provide with more information such as directory structure?

### Student response 
> This is the directory structure : \
> <img width="170" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/1a1e4ade-635f-43df-8200-1f1af7d4cfb4">

### TA response on how to fix the bug
> "The output shows that there's an ArithmeticException error, as we are trying to divide by zero. The line that's causing this is when the code tries to divide the first element of the line by the second element `Integer.parseInt(splitLine[0]) / Integer.parseInt(splitLine[1])`.

>This happens when the code reads the third line of `data.csv`, which contains the numbers `12` and `0`. Trying to perform division with `0` as the divisor results in this exception.

### Student Follow-up after fixing the bug
> I modified the Main.java file to add a condition that checks if the divisor is zero before performing the division operation. Here is the modified Main.java file:
> <img width="856" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/9c8cbb2c-9e98-4f30-8799-500f9f56efba">

> Here is the successful output: \
> <img width="447" alt="image" src="https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/f6939dec-b970-4381-819f-e7a3ad8044b7">

> The corrected code will handle cases when the divisor is zero, and it will print a special message for these cases instead of throwing an exception.
