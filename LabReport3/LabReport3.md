# Command-Line Options for `grep`
## `grep` is a command-line utility used to search through files for a specific pattern or regular expression. 
### Here are four interesting options for grep, along with examples of their usage on files and directories located in the `./technical` directory.

#### 1.  `grep -i, --ignore-case`
> [Source](https://sourcegear.com/diffmerge/webhelp/sec__opt__folderfilters__case.html)
>The -i or --ignore-case option tells grep to perform a case-insensitive search. 
>This means that the search will match both uppercase and lowercase letters, regardless of how they appear in the file.

Example one :
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/84ce4d18-a490-42dd-9431-8b791b114bf8)\
>I added four lines of my name in both capital and lower letters to test out this command, as I called the command line\
>`grep -i "hanning" technical/911report/chapter-1.txt` The outcome prints all "hanning" despite the difference in capital and lower letter.

Example two :
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/46246851-622e-454c-aa7e-99e003a63f80)\
>I called the command on the `technical/911report/preface.txt` file, and the command returned the three lines that contains "law", as we can see, there are two lower case "law" and one upper case "law".

<br/><br/>
#### 2. `grep -rl "pattern" --include ".extension" "directories"`
> [Source](https://docs.oracle.com/cd/E19620-01/805-3902/6j3n40vtk/index.html)
>This command will search for files with a specific extension, I use the --include option to specify the file pattern to search for.

Example one :
>I typed in `grep -rl "911" --include "*.txt" technical/`
>This will search for the pattern "911" only in files with the .txt extension in the technical directory and its subdirectories, and print only the names of the files that contain the pattern.
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/41fdbe51-9eeb-4efd-8e0e-0cd3041a3d66)\
>The output prints all the files end with .txt that contains "911".

Example two :
>I typed in `grep -rl "Hanning" --include "*.txt" technical/`
>This will search for the pattern "Hanning" only in files with the .txt extension in the technical directory and its subdirectories, and print only the names of the files that contain the pattern.
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/00542b32-5470-4fc1-8cc7-d019a2132923)\
>As we can see, we found "Hanning" only in the chapter-1.txt file. And the file path is printed.

<br/><br/>
#### 3. `grep -q or --quiet or --silent`
> [Source](https://stackoverflow.com/questions/48115340/how-to-use-grep-to-detect-if-specific-text-is-found-inside-a-folder)
>This command makes grep suppress all normal output and only indicate whether the pattern was found or not using the exit status.

Example one : 
>I typed in `grep -q "September 11" technical/911report/preface.txt && echo "Found" || "Not found"`, intend to search for "September 11" in the prefact.txt file and it will print Found if is found and Not found if it is not found.
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/06728a10-d3db-42b3-ac94-4f4de7cc886f)
>As we can see, we found September 11 in the preface.txt

Example two :
>I typed in two commands `grep -q "Hanning" technical/911report/preface.txt && echo "Found" || "Not found"` and `grep -q "Hanning" technical/911report/chapter-1.txt && echo "Found" || "Not found"` to search pattern "Hanning" in both preface.txt and "chapter-1.txt" files,and the result will return in Found or Not found.
>Here is the result
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/10958c16-90c6-45ab-865a-8c9eed0cf5c9)
>As we can see, we found in chapter-1.txt but not in preface.txt because I only added my name in chapter-1.txt.

<br/><br/>
#### 4. `grep "^Strings" + filepath`
> [Source](https://docs.oracle.com/cd/E19253-01/806-7612/filesearch-96061/index.html)
>This command searches for lines that start with the specific "Strings" in the file.

Example one :
>I deleted all the indented spaces before each line in technical/911report/preface.txt and I used `grep "^We" technical/911report/preface.txt` to search for all lines start with "We"
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/acba6e9e-b275-4fae-88b3-b3c8971dec68)\
>As we can see, the terminal prints out all the lines start with capital letter 'W' and lower letter 'e'.

Example two :
>I used `grep "^11" technical/911report/chapter-13.4.txt` to search for all the lines start with "11" in the file chapter-13.4.txt.
>![image](https://github.com/TacoKilla420/cse15l-lab-reports/assets/102259888/059f1779-cb75-4406-adb4-063ca686afa2)\
>As we can see, the command prints out both two and three digits sentences number as long as the number starts with prefix "11".
