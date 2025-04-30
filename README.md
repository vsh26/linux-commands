# 🛠️Linux Commands

If you are beginner in Linux, and have only ever used Windows, do consider reading the following articles, before directly jumping upon the commands, to understand the Linux better.
- [Exploring Linux: Its Origins, Why It’s Different, and How It Compares to Windows and macOS](https://controlplusblog.hashnode.dev/exploring-linux-its-origins-why-its-different-and-how-it-compares-to-windows-and-macos)
- [Why the Juice Seller at MacOS Gets the Order of a Linux User, But Windows Looks Confused](https://controlplusblog.hashnode.dev/why-the-juice-seller-at-macos-gets-the-order-of-a-linux-user-but-windows-looks-confused)
 
<br>

## 🔧 Some basic commands

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `pwd`               | present working directory (check current location)              |
  | `whoami`            | display name of current logged-in user                          |
  | `clear`             | clear the terminal                                              |
  | `su`                | switch to root user                                             |
  | `su user_name`      | switch to user `username`                                       |
  | `exit`              | exit as current user or close terminal                          |
  | `reboot`            | restart linux server                                            |
  | `shutdown`          | shutdown linux server                                           |
  
<br>

### 📌 `date` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `date`              | check system day, date (date, month, year) and time (HH:MM:SS)  |
  | `date +%D`          | shows only date (MM/DD/YYYY)                                    |
  | `date +%T`          | shows only time (HH:MM::SS)                                     |
  | `date +%Y`          | shows only year                                                 |
  | `date +%m`          | shows only month                                                |
  | `date +%d`          | shows only day of the month (date)                              |
  | `date +%H`          | shows only hour                                                 |
  | `date +%M`          | shows only minute                                               |
  | `date +%T`          | shows only second                                               |
  | `date +%A`          | shows only full weekday name (e.g., Sunday)                     |
  | `date +%B`          | shows only full month name (e.g., January)                      |
  | `date +%H:%M`       | shows time(HH:MM)                                               |
  | `date +"%Y-%m-%d %H:%M:%S"` | shows only time (YYYY-MM-DD HH:MM:SS)                   |
  
  <br>
  
  > [!Note]
  > - `%D`, `T`, etc. are FORMAT SPECIFIERS. We can use format specifiers with the `+` option to customize how the date and time are displayed.

<br>

### 📌 `ls` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls`                | display files and directories present in current location       |
  | `ls -a`             | show all files, including hidden files (those starting with .)  |
  | `ls -l`             | use a long listing format with detailed information (permissions, owner, size, etc.). |
  | `ls -al`            | show all files, including hidden files, in a long listing format|
  | `ls -lh`            | show files in a long listing format, with file sizes in human-readable formats (KB, MB).|
  | `ls -R`             | recursively list the contents of all subdirectories             |
  | `ls -t`             | sort by modification time, newest first                         |
  | `ls -r`             | reverse the order of the sort                                   |
  | `ls /path/to/directory` | list contents of a particular dirctory                      |

  <br>
  
> [!Note]
> - `-a`, `-l`, etc. are FLAGS. Flags are used to specify how a command should operate and what information it should display. We can use a single flag or combine multiple flags together in one command.

<br>

***

<br>

## 📂 Working with directories

<br>


  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `mkdir foldername`  | creates a new folder `folder name`                              |
  | `rmdir foldername`  | deletes a new folder `folder name`                              |
  | `cd path`           | change directory                                                |
  | `cd ..`             | change the current directory to the parent directory of the current working directory|
  | `cd /`              | change the current directory to the root directory              |
  | `cp file1 file2`    | copy contents of `file1` to `file2` (if `file2` already exist it will be overwritten)|
  | `cp path/source/file path/destination` | copy `file` from source to destination, (if `file` already exist in destination it will be overwritten)|
  | `mv path/source/file path/destination` | move `file` from source to destination (cut-paste), (if `file` already exist in destination it will be overwritten)|
  | `mv file1 file2`    | used to rename a file |

<br>

> [!Note]
> - `-i` flag can be used with `cp` and `mv` to get a prompt before overwriting files

<br>

***

<br>

## 📚 Working with files

<br>

### 1️⃣ <ins>Reading files</ins>

<br>

#### 📌 `cat` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `cat filename`      | display the content of file on terminal                         |
  | `cat -n filename`   | displays the file content, numbers each line                    |
  | `cat -E filename`   | show end-of-line character, displays a `$` at the end of each line, making line endings visible|
  | `cat -s filename`   | compresses multiple consecutive blank lines into one            |
  | `tac filename`      | display file in reverse order                                   |
  | `cat file1 file2`   | displays the combined content of multiple files                 |
  | `cat file1 file2 > newFile`   | creates `newfile` containing the contents of both `file1` and `file2`|
  | `cat > newFile`     |  create a new file and input text manually                      |

<br>

> [!Note]
> - ` cat > myfile.txt` Press `Enter`.
Type your text. `Hello, this is a new file! `. Then press `Ctrl+D` to save and exit.

<br>

#### 📌 `less` command
- Used for viewing large files or outputs one screen at a time.
- We can scroll up and down using the arrow keys or other navigation commands (forward as well as backward navigation possible).

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `less filename`     | viewing large files or outputs one screen at a time             |

<br>

#### 📌 `more` command
- Opens `filename` in the more viewer.
- Displays content page by page.
- Allows forward navigation only (no backward scrolling).

<br>
  
  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `more filename`     | viewing large files or outputs page by page                     |

<br>

#### 📌 `head` `tail` commands

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `head -5 filename`     | display top 5 lines from `filename`                          |
  | `tail -5 filename`     | display last 5 lines from `filename`                         |

<br>

### 2️⃣ <ins>Creating files</ins>

<br>

#### 📌 `touch` command (for creating)
- If `filename` does not exist, it will be created as an empty file.
- If `filename` already exists, its access and modification timestamps will be updated to the current time.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `touch filename`    | create a new file `filename`                                    |

<br>

### 3️⃣ <ins>Deleting files</ins>

<br>

#### 📌 `rm` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `rm filename`       | deletes the file `filename`                                     |

<br>

### 4️⃣ <ins>Editing files</ins>

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `vi filename`       | opens file for editing in vi editor                             |
  | `nano filename`     | opens file for editing in nano editor                           |

<br>

### 5️⃣ <ins>Dividing file into smaller sections<ins>

<br>

#### 📌 `split` command
- Syntax: `split [options] [input_file] [prefix]`

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `split -l 100 filename `| split the file into pieces with 100 lines each              |

<br>

> [!Note]
> - To split a file into smaller files containing 100 lines each. This command will create files named `xaa`, `xab`, `xac`, etc., each containing 100 lines from `filename`.
> If filename.txt has 250 lines, it will create:
>   - xaa (lines 1-100)
>   - xab (lines 101-200)
>   - xac (lines 201-250)

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `split -b 1M filename ` | split the file into pieces of specified byte size (here, 1MB)|
  | `split -d -l 100 filename `| use numeric suffixes instead of alphabetic suffixes for the output files|
  | `split -l 100 --additional-suffix=.txt filename.txt`| append a specified suffix to the output file names|
  | `split -n 4 filename.txt`| split the file into N pieces, approximately equal in size. This will create 4 files, each containing a portion of the original file|
  | `split -l 50 data.txt split_` | split file with custom prefix (Output files: `split_aa`, `split_ab`, `split_ac`, etc.)|

<br>

### 6️⃣ <ins>Comparing files</ins>

<br>

#### 📌 `cmp` command
- Compares to files byte by byte
- If files are identical:
  - outputs nothing and returns an exit status of `0`
- If files are different:
  - outputs the position and byte number of the first difference (exit status `1`)
- Returns exit status `2`, if an error occured
- Syntax: `cmp [OPTION]... FILE1 FILE2`

<br>

  | Option             | Description                                                           |
  |--------------------|-----------------------------------------------------------------------|
  | `-b`               | Prints differing bytes for binary files in octal and their ASCII equivalents.|
  | `-i <SKIP>`        | Skips the first `<SKIP>` bytes of both files before comparing.        |
  | `-n <COUNT>`       | Compares only the first `<COUNT>` bytes of both files.                |
  | `-s`               | Suppresses output; returns only the exit status.                      |
  | `-l`               | Displays all differing bytes with their offsets and values.           |

<br>

#### 📌 `diff` command
- Compare two files line by line and display the differences between them.
- The output shows lines that are different, prefixed with:
  - `<` : Lines in `FILE1`
  - `>` : Lines in `FILE2`
- If the files are identical, `diff` produces no output and returns an exit status of `0`
- Syntax: `diff [OPTION]... FILE1 FILE2`

<br>

  | Option             | Description                                                            |
  |--------------------|------------------------------------------------------------------------|
  | `-c`               | Produces output in context format, showing lines around the changes.   |
  | `-u`               | Produces output in unified format (compact version of context format). |
  | `-i`               | Ignores case differences in file comparison.                           |
  | `-w`               | Ignores all whitespace when comparing lines.                           |
  | `-B`               | Ignores blank lines.                                                   |
  | `-r`               | Recursively compares directories.                                      |
  | `-q`               | Reports only whether files differ, without showing details.            |

<br>

### 7️⃣ <ins>Finding files</ins>

<br>

#### 📌 `find` command
- Search for files and directories in a directory hierarchy based on various criteria, such as name, type, size, permissions, modification time, and more.
- Syntax: `find [path...] [expression]`
  - `path`: The directory (or directories) to search. Default is the current directory (`.`).
  - `expression`: The criteria used to filter files or directories.

<br>

  | Option              | Description                                                           |
  |---------------------|-----------------------------------------------------------------------|
  | `-name <pattern>`   | Searches for files or directories by name (case-sensitive).           |
  | `-iname <pattern>`  | Searches for files or directories by name (case-insensitive).         |
  | `-type <type>`      | Searches by type: `f` for files, `d` for directories, `l` for symbolic links, etc.|
  | `-size <n>`         | Searches for files of a specific size (e.g., `+10M`, `-1G`, `100k`).  |
  | `-mtime <n>`        | Finds files modified `<n>` days ago (`+` for more than, `-` for less than).|
  | `-perm <mode>`      | Finds files with specific permissions (e.g., `644`).                  |
  | `-user <username>`  | Searches for files owned by a specific user.                          |
  | `-group <groupname>`| Searches for files belonging to a specific group.                     |
  | `-empty`            | Finds empty files or directories.                                     |
  | `-exec <command>`   | Executes a command on each matched file (e.g., delete or copy).       |
  | `-maxdepth <n>`     | Limits the depth of the search to `<n>` levels.                       |
  | `-mindepth <n>`     | Starts searching only after `<n>` levels.                             |
  | `-not` or `!`       | Negates a condition (e.g., `! -name "*.txt"` finds files not ending in `.txt`).|
  | `-or`               | Combines conditions using logical OR.                                 |
  | `-and`              | Combines conditions using logical AND (default if not specified).     |
  | `-regex <pattern>`  | Matches files or directories using a regular expression.              |

<br>

#### 📌 `locate` command
- Quickly find the location of files and directories by searching through a pre-built database rather than scanning the filesystem in real time.
- It's faster than `find` but requires the database to be regularly updated using the `updatedb` command.
- Syntax: `locate [OPTION]... PATTERN`
  - PATTERN: The name or part of the name of the file or directory you’re searching for
- The `locate` command searches a database, usually `/var/lib/mlocate/mlocate.db`, which contains a snapshot of the filesystem's file and directory structure.
- This database is updated periodically (e.g., daily) or manually using the `updatedb` command.
- Since it relies on a pre-built database, `locate` may not find files that were recently created or moved unless the database is updated.

<br>

  | Options              | Description                                                             |
  |---------------------|-------------------------------------------------------------------------|
  | `-i`               | Performs a case-insensitive search.                                      |
  | `-n <N>`           | Limits the output to the first `<N>` matches.                            |
  | `-r <REGEX>`       | Searches using a regular expression.                                     |

<br>

***

<br>

## 📝 Operations on file contents

<br>

### 1️⃣ <ins>Sorting the file content</ins>

<br>

#### 📌 `sort` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `sort filename`     | sort the content from the file (does not save changes to the original file), case is ignored|
  | `sort -o filename` | **(Overwrite)** sort the content from the file and overwrite the original file|
  | `sort -r filename`  | **(Reverse)** sort the content from the file in reverse order   |
  | `sort -n filename`  | **(Numeric)** sort numerically (useful for sorting numbers)     |
  | `sort -k 2 filename`| **(Key)** sorts the lines based on the second field             |
  | `sort -u filename`  | **(Unique)** suppress duplicate lines in the output            |

<br>

### 2️⃣ <ins>Finding unique</ins>

<br>

#### 📌 `uniq` command

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `uniq filename`     | displays the unique lines from a <ins> sorted file </ins>       |
  | `uniq -c filename.txt`| **(Count)** prefix each unique line with the number of occurrences|
  | `uniq -d filename.txt`| **(Duplicates)** only show duplicate lines                    |
  | `uniq -u filename.txt`| **(Unique)** only show unique lines that are not repeated     |
  | `uniq -i filename.txt`| **(Ignore Case)** treat lines as equal, regardless of case (Uppercase, lowercase)|
  | `uniq -s 5 filename.txt`| skip the first 5 characters when comparing lines            |
  | `uniq -w 3 filename.txt`| compare only the first N characters of each line            |
  | `uniq sorted_data.txt > unique_data.txt`| redirect the unique output to the new file  |

<br>

> [!Note]
> - The `uniq` command only removes **consecutive duplicate**. Therefore, it is often used in conjunction with the `sort` command to ensure all duplicates are adjacent:
> `sort filename.txt | uniq`

<br>

> [!Note]
> - `|` known as the pipe, is a powerful feature in Unix/Linux command-line environments. It is used to chain commands together, allowing the output of one command to be used as the input for another command. This enables users to create complex command sequences that perform multiple operations in a single line.

<br>

### 3️⃣ <ins>Searching the content</ins>

<br>

#### 📌 `grep` command
- The `grep` command in Unix/Linux is used for searching and filtering text based on patterns. It is one of the most powerful and commonly used commands for text processing.
- Basic syntax: `grep [options] 'pattern' [file(s)]`
  - `pattern`: The text or regular expression to search for.
  - `file(s)`: The file or files to search within.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `grep "hello" file1 file2` | find all lines in `file1` `file2` that contain the word `hello`|
  | `grep -i "hello" file1` | **(Ignore Case)** find all lines in `file1` that contain the word `hello`, regardless the case|
  | `grep -v "hello" file1` | **(Invert Match)** displays lines that do not contain the word `hello`|
  | `grep -c "hello" file1` | **(Count Matches)** displays number of lines that contain the word `hello`|
  | `grep -n "hello" file1` | **(Show Line Numbers)** displays matching lines along with their line numbers|
  | `grep -l "hello" file1` | **(List Matching Files)** lists the names of files containing matches (useful when searching multiple files)|
  | `grep -w "hello" file1` | **(Match Whole Words)** matches `hello` as a whole word, but not `hello123` or `ahello`|
  | `grep -r "hello" /path/to/directory` | **(Recursive Search)** searches for `hello` in all files within the specified directory and its subdirectories|

<br>

> [!Note]
> - `-E` flag allows using <ins>**Extended Regular Expressions**</ins> for more complex patterns
> - E.g.: `grep -E "cat|dog" file` (matches any of the specified patterns)

<br>

#### 📌 `egrep command`
- `egrep` command can be used instead of `grep`. It supports extended regular expressions (ERE) by default.
- `egrep` is equivalent to `grep -E`
- Syntax: `egrep [options] 'pattern' [file(s)]`

<br>

  | Option          | Description                                                         |
  |------------------|-----------------------------------------------------------------|
  | `-i`               | Ignore case while matching patterns.                             |
  | `-v`               | Invert match to select non-matching lines.                       |
  | `-c`               | Count the number of matching lines.                              |
  | `-l`               | List the names of files with matches.                            |
  | `-r`               | Recursively search through directories.                          |

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `egrep "cat\|dog" file.txt`      | **(Alteration)** matches any of the specified patterns|
  | `egrep "go+gle" file.txt`        | **(One or More Occurrences)** matches one or more occurrences of the previous character or group (matches `gogle`, `google`, `goooogle`, etc.)|
  | `egrep "colou?r" file.txt`       | **(Zero or One Occurrence)** matches zero or one occurrence of the previous character or group (matches `color` or `colour`)|
  | `egrep "(foo\|bar)baz" file.txt` | **(Grouping)** groups patterns for alternation or quantifiers (matches `foobaz or barbaz`)|
  | `egrep "a*b" file.txt`           | **(Zero or More Occurrences)** matches zero or more occurrences of the previous character or group (matches `b`, `ab`, `aab`, etc.)|
  | `egrep -i "error\|warning" *.log`| searches for `error` or `warning` (case-insensitive) in all .log files|

<br>

### 4️⃣ <ins>Shuffle content</ins>

<br>

#### 📌 `shuf` command
- Used to shuffle or randomly rearrange the lines in a file or generate random permutations of input.
- Syntax: `shuf [OPTION]... [FILE]` (The file whose lines are to be shuffled.)
- If no file is provided, `shuf` reads from standard input.)

<br>
  
  | Option              | Description                                                     |
  |-----------          |-------------                                                    |
  | `-n <count>`        | Output only the specified number of lines                        |
  | `-o <file>`         | Write the output to the specified file                           |
  | `-i <range>`        | Generate random numbers within the specified range (e.g., 1-10)  |
  | `--random-source=<file>`| Use a custom file for random number generation               |
  | `-r`                | Repeat lines in the output (with replacement)                    |

<br>

**E.g.:**

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `shuf filename.txt` | Randomly rearranges the lines in `filename.txt` and outputs them to the terminal|
  | `shuf -i 1-10`      | Outputs a random permutation of numbers from 1 to 10            |
  | `shuf -i 1-50 -n 5` | Randomly selects 5 numbers from the range 1 to 50               |
  | `shuf filename.txt -o shuffled.txt` | Writes the shuffled content of `filename.txt` to `shuffled.txt`|
  | `shuf -i 1-10 -r -n 15` | Outputs 15 numbers randomly selected from the range 1 to 10 with replacement (numbers can repeat).|
  | `echo -e "apple\nbanana\ncherry" \| shuf` | Shuffle standard input                    |

<br>

### 5️⃣ <ins>Word count</ins>

<br>

#### 📌 `wc` command (Word Count)
- Count lines, words, characters, or bytes in files or standard input.
- Syntax: `wc [OPTION]... [FILE]...`
- If no file is provided, `wc` reads from standard input.

<br>

  | Option              | Description                                                     |
  |-----------          |-------------                                                    |
  | `-l`                | Count the number of lines                                       |
  | `-w`                | Count the number of words                                       |
  | `-c`                | Count the number of bytes                                       |
  | `-m`                | Count the number of characters                                  |
  | `-L`                | Print the length of the longest line (in characters)            |

<br>

**E.g.:**

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `wc filename.txt`   | Count lines words and bytes                                     |
  | `wc -l filename.txt`| Count only lines                                                |
  | `wc -l -w filename.txt`| Count lines and words                                        |
  | `wc file1.txt file2.txt` | Count from multiple files                                  |
  | `echo "Hello, World!" \| wc -w` | Count words from standard input                     |
  | `grep "pattern" filename.txt \| wc -l` | Count the number of lines in a file matching a specific pattern |

<br>

### 6️⃣ <ins>String operation command</ins>

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `awk 'pattern { action }' input-file` | text processing and data extraction tool (useful for structured files)|
  | `awk -F , '{print $2}' file.csv` | print a specific column from a CSV file            |
  | `cut OPTION... [FILE...]`| used for extracting specific sections from each line of input, typically from files or piped output|
  | `cut -c1-2 file.txt`| display starting twocharacters of all line                      |
  | `sed [OPTIONS] 'COMMANDS' FILE`| (Stream Editor) used for parsing and transforming text|
  | `sed -n '5p' file.txt`| display a specific line from a file                           |
  | `sed -n 's/from/to/g' file.txt`| replace a specific word within a file                |
  | `tr [OPTIONS] SET1 [SET2]`| (Translate) used for translating or deleting characters from standard input. It can be very useful for simple text transformations, such as changing case, removing whitespace, or replacing specific characters|
  | `tr [:lower:] [:upper:] < file.txt` | convert all lowercase letters in `file.txt` to corresponding uppercase letters|
  | `tr [:punct:] Z < file.txt` | replace all punctuation characters in the `file.txt` with the letter `Z`|
  | `tr [:digit:] Z < file.txt` |  replace all digit characters (0-9) in the `file.txt` with the letter `Z`|
  | `truncate [OPTION]... FILE...`   | used to reduce or extend the size of a file to a specified size. If the file is reduced, data is lost, and if it is extended, the additional space is filled with null bytes.|
  | `truncate -s 100M file.txt` | set the size of `file.txt` to 100MB                     |
  | `echo "ABCDE" \| fold -w1`  | display following line in vertical line - ABCDE         |

<br>

***

<br>

## 🪛 Utility Commands

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `history`           | display previously used commands                                |
  | `<command> --help`  | check syntax and options available for a command                |
  | `man command`       | read or get more info about a command                           |
  | `which command`     | check which executable is using for a command                   |
  | `bc`                | binary calculator                                               |
  | `cal`               | displays calendar                                               |
  | `uptime`            | how long the system has been running, the number of active users, and the system load averages|
  | `script`            | record a terminal session (type `exit` to stop recording        |
  | `alias [name='command']`| create shortcuts for commands, valid only for that session, not permenant (useful for frequently used complex commands)|
  | `unalias name`      | removes alias `name`                                            | 

<br>

***

<br>

## 🗃️ Zip and unzip files and folders

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `gzip filename`     | compress file `filename`                                        |
  | `gzip -k filename`  | compress file `filename` (keeping original file as it is)       |
  | `gzip -d filename`  | decompress file                                                 |
  | `gunzip filename`   | decompress file                                                 |
  | `tar -cf archive.tar newFolder/` | compress folder `newFolder` and creates a tar archive named `archive.tar`|
  | `tar -czf archive.tar.gz newFolder` | compress folder `newFolder` and creates a gzipped tar archive named `archive.tar`|
  | `tar -xf archive.tar` | extracts the contents of `archive.tar` into the current directory|
  | `tar -xzf archive.tar.gz` | extracts the contents of `archive.tar.gz`                |
  | `zip myfiles.zip file1 file2` | compress multiple files in one zipped file `myfiles.zip`|
  | `unzip myfiles.zip` | extracts all files from `myfiles.zip` into the current directory|
  | `unzip -l myfiles.zip` | lists the contents of `myfiles.zip` without extracting the files|

<br>

***

<br>

## 📥 Downloading files from internet

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `wget [URL]`        | downloads file from specified url to current directory          |
  | `wget -O name [URL]`| downloads file from specified url and saves it as `name`        |
  | `curl [URL]`        | call API on linux (used for transferring data to or from a server using various protocols)|

<br>

***

<br>

## 📦 Software package management

<br>

### 1️⃣ <ins>Debian-based distributions</ins>

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `apt`               | Advanced Package Tool (package manager)                         |
  | `dpkg -l \| grep package-name`| check if an package is installed or not on Linux      |
  | `apt list --installed \| grep package-name`| check if an package is installed or not on Linux|
  | `apt search package-name`| list available packages to install                         |

<br>

### 2️⃣ <ins>RPM (RedHat Package Manager)-based distributions</ins>

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `yum`               | Yellowdog Updater, Modified (package manager)                   |
  | `dnf`               | Dandifies YUM (successor to `yum`) (package manager)            |
  | `yum list installed \| grep package-name`| check if an package is installed or not on Linux|
  | `dnf list installed \| grep package-name`| check if an package is installed or not on Linux|
  | `rpm -qa \| grep package-name` | check if an package is installed or not on Linux     |
  | `yum list available`| list available packages to install                              |
  | `dnf list available`| list available packages to install                              |

<br>

***

<br>

## ⚙️ Service management

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `systemctl status service-name`| displays the current status of the specified service |
  | `systemctl start service-name` | starts the specified service                         |
  | `systemctl stop service-name`  | stops the specified service                          |
  | `systemctl list-units --type=service --all` | list all services and their current statuses|

<br>

***

<br>

## 🧮 Environment variables

<br>

1️⃣ List all existing environment variables
  - `printenv`

2️⃣ Check a specific variable
  - `echo $VARIABLE_NAME`

3️⃣ Setting a temporary environment variable (for the current shell session)
  - `export VARIABLE_NAME=value`

4️⃣ Setting a pemanent environment variable (for the current shell session)
  - `export VARIABLE_NAME=value`
  - Add env variable in `./bashrc` (configuration file), using any text editor, and save the file
  - Reload configuration file using `source ~/.bashrc`

5️⃣ Unsetting a temporary environment variable
  - `unset VARIABLE_NAME`

6️⃣ Unsetting a pemanent environment variable
  - Open `./bashrc` file, locate the line that exports the variable you want to unset
  - Delete or comment out the line and save the file
  - Reload configuration file using `source ~/.bashrc`

<br>

***

<br>

## 🌐 Working with remote servers

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ssh [OPTIONS] [USER@]HOST [COMMAND]`| Secure Shell (used to securely connect to a remote system over a network)|
  | `ssh user@hostname` | access remote server                                            |
  | `ssh -p 2222 user@hostname` | using specific port                                     |
  | `ssh user@example.com "ls -l /var/www"` | running command on a remote host            |
  | `scp [OPTIONS] [SOURCE] [DESTINATION]` | Secure Copy ( copy files or directories securely between a local and a remote system, or between two remote systems) |
  | `scp file.txt user@hostname:/path/to/destination` | copying files to/from remote host |

<br>

***

<br>

## 🛡️ Working with permissions

<br>

* File permissions in Linux control who can read, write, or execute files and directories. Permissions are assigned to three categories of users:

  - **Owner:** The user who owns the file.
  - **Group:** The group associated with the file.
  - **Others:** All other users on the system.
 
* How to read permissions?
  1. **File type:** The first character (`-`) indicates the file type
      - `-` : Regular file
      - `d` : Directory
      - `l` : Symbolic link
      - `c` : Character device
      - `b` : Block device
     
    2. **Permissions:** Next 9 characters, divided into groups of three
        - **Owner (`rwx`):** The file owner can read (`r`), write (`w`), and execute (`x`).
        - **Group (`r-x`):** Members of the group can read (`r`) and execute (`x`), but not write.
        - **Others (`r--`):** All other users can only read (`r`).

* Breakdown of each permission:
  - `r` (read): Permission to read the file or list directory contents.
  - `w` (write): Permission to modify the file or add/remove files in a directory.
  - `x` (execute): Permission to run the file as a program or enter a directory.

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls -l filename`    | can be used to display file permissions                         |

<br>

### 📌 `chmod` command
- Used to change file permissions. It allows you to modify who can read, write, or execute a file or directory.
-  1️⃣ **Using Symbolic mode**
  -  Syntax: `chmod [WHO][OPERATOR][PERMISSIONS] FILE`
  - **WHO**:
    - `u`: Owner (user)
    - `g`: Group
    - `o`: Others
    - `a`: All (owner, group, and others)
  - **OPERATOR:**
    - `+`: Add permission
    - `-`: Remove permission
    - `=`: Set exact permission

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `chmod u+x file.txt`| Add execute permission for the owner                            |
  | `chmod o-w file.txt`| Remove write permission for others                              |
  | `chmod a=rw file.txt`| Set read and write permissions for all                         |
  | `chmod --reference=source.txt target.txt` | Copy permissions from another file        |


<br>

- 2️⃣ **Using Numeric (Octal) mode**
  - Permissions are represented by three bits:
    - `r` (read) = 4
    - `w` (write) = 2
    - `x` (execute) = 1
  - The total value for a permission set is the sum of these numbers:

  <br>
  
    | Permission | Value | Meaning            |
    |------------|-------|--------------------|
    | `---`      | 0     | No permissions     |
    | `--x`      | 1     | Execute only       |
    | `-w-`      | 2     | Write only         |
    | `-wx`      | 3     | Write and execute  |
    | `r--`      | 4     | Read only          |
    | `r-x`      | 5     | Read and execute   |
    | `rw-`      | 6     | Read and write     |
    | `rwx`      | 7     | Read, write, and execute |

<br>

  - Structure of octal permissions: Permissions are written as three digits, where each digit corresponds to a specific category:
    - First digit: Owner
    - Second digit: Group
    - Third digit: Others

  <br>
  
  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `chmod 744 file.txt`| Full permissions for the owner, and read-only for others        |
  | `chmod 666 file.txt`| Read and write permissions for everyone                         |
  | `chmod 751 file.txt`| Owner has full permissions, group has read/execute, others have execute only|
  | `chmod 750 file.txt`| No permissions for others                                       |

  <br>
 
  - **Quick reference table:**

  <br>
  
  | Octal   | Owner | Group | Others |
  |---------|-------|-------|--------|
  | `777`   | rwx   | rwx   | rwx    |
  | `755`   | rwx   | r-x   | r-x    |
  | `644`   | rw-   | r--   | r--    |
  | `700`   | rwx   | ---   | ---    |
  | `600`   | rw-   | ---   | ---    |

<br>

### 📌 `chown` command
- Used to change the owner and/or group ownership of a file or directory. It is essential for managing file permissions and access.
- Syntax: `chown [OPTIONS] OWNER[:GROUP] FILE`
  - **OWNER:** The new owner (user) of the file/directory.
  - **GROUP:** The new group of the file/directory. Specifying :GROUP is optional.
  - **FILE:** The file or directory whose ownership is being changed.

 <br>
 
  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `chown user file.txt`| sets `user` as the owner of file.txt                           |
  | `chown username:groupname file.txt` | sets `username` as the owner and `groupname` as the group|
  | `chown :groupname file.txt`| change the group only                                    |
  | `chown -R username:groupname directory/`| change ownership for a directory and all its contents|
  | `chown --reference=source_file target_file`| set ownership to match another file      |

<br>

***

<br>

## 💾 Memory info

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `free`              | check free RAM space                                            |
  | `top `              | check % memory and CPU utilization                              |
  | `du`                | check disk utilization                                          |
  | `df`                | check filesystem available and disk space allocated             |

<br>

***

<br>

## 🖥️ System info

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `hostname`          | check hostname of yourlinux server                              |
  | `lscpu`             | check cpu/core/thread info of your linux server                 |
  | `arch`              | check type of architectureof your linux server                  |
  | `lsblk`             | see list of storage devices, disk partition on your linux server|
  | `uname -a `         | see OS name of linux server                                     |

<br>

***

<br>

## 🔄️ Process Management

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ps -ef`            | Show all running processes                                      |
  | `ps -ef \| grep java` | Check if a process(java) running or not                       | 
  | `ps -u`             | Show processes for the current user                             |
  | `ps aux`            | Show all processes, including those without a terminal          |
  | `ps -p 1234`        | Display specific processes by PID                               |
  | `ps aux --sort=-%mem`| Sort processes by memory usage                                 |
  | `pgrep chron`       | Get PID of process `chron`                                      |
  | `kill -9 [PID]`     | stop a process by PID (`-9` means forcefully)                   |
  | `pkill httpd`       | Stop a process by its name, here `httpd` service                |
  | `jobs`              | See all active jobs                                             |
  | `bg`                | Resume job in background                                        |
  | `fg`                | Resume job in foreground                                        |
  | `nohup ./script.sh &` | (No Hnag Up -  It allows a command to continue running in the background even after the user has logged out of the terminal session )Running script in background |
  | `at`                | schedule a script to run on a particular date/time              |
  | `crontab`           | schedule a script to run on a particular date/time              |

<br>

***

<br>

## 🛜 Networking

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ifconfig`          | Check IP of your machine                                        |
  | `ping URL`          | check if a server or website is accesible or not                |
  | `telnet IP Port`    | check if a IP:PORT is accessible and open or not                |
  | `netstat -putan \| grep 80` | check if port is open or not on our server              |
  | `traceroute`        | check all hubs in network path to reach a website               |

<br>

***

<br>

## 👨‍💻 User Management

**User** - Entity that performs tasks and actions. Each user has an ID.

There are three types of users in Linux:

| User            | Description                   | ID                |
|-----------------|-------------------------------|-------------------|
| 1. Root User    | Super admin                   | 0                 |
| 2. System Users | Ceated by OS to run processes | 1 - 999           |
| 3. Local Users  | Human users                   | > 999 upto 60,000 |

> [!NOTE]
> - For System Users (processes), if all IDs from 1 t0 999 are already in use, then IDs from local users are assigned to the processes
> - For Local Users, the upper limit of 60,000 is for Ubuntu. This number is kept for optimal performance and can be changed if required.

> [!IMPORTANT]
> **Why don't we use root user for everyday tasks?**
>   - We have multiple users working on a system, so giving root access to each user is not a good practice, as it would be very difficult to track user activities.
>   - Insted we create local users. These local users can have the root privileges using `sudo`.
<br>

| Commands                                | Description                                                                             |
|-----------------------------------------|-----------------------------------------------------------------------------------------|
| `whoami`                                | Displays current user                                                                   |
| `sudo cat /etc/passwd`                  | Prints all users                                                                        |
| `sudo cat /etc/shadow`                  | Print hashed passwords and account related security details for all users in the system |
| `id user_name`                          | Displays UID, GID and groups for current user                                           |

### Adding user

**1. `useradd` - low level command for user creation**
 - Creates user, but does not create a home directory and other skeleton. We need to create everything manually.

   | Commands                    | Description                                           |
   |-----------------------------|-------------------------------------------------------|
   | `sudo useradd user_name`    | Creates a new user `user_name` (without any skeleton) |
   | `sudo passwd user_name`     | Set or change password for `user_name`                |
   | `sudo useradd -m user_name` | Creates user `user_name`  with home directory         |

**2. `adduser` - high level command for user creation**
 - Creates user, along with a home directory and other skeleton.

   | Commands                                | Description                               |
   |-----------------------------------------|-------------------------------------------|
   | `sudo adduser user_name`                | Creates a new user `user_name`            |

### Delete user

 | Commands                                | Description                               |
 |-----------------------------------------|-------------------------------------------|
 | `sudo userdel -r user_name`             | Deletes user `user_name`                  |

### Group management

| Commands                               | Description                                 |
|----------------------------------------|---------------------------------------------|
| `sudo cat /etc/group`                  | Prints all groups                           |
| `sudo addgroup group_name`             | Creates a new group `user_name`             |
| `sudo usermod -aG group_name user_name`| Adds user `user_name` to group `group_name` |

  > [!CAUTION]
  > Not using append flag (`a`), will remove all other users from the group


| Commands                               | Description                                 |
|----------------------------------------|---------------------------------------------|
| `sudo groupdel group_name`             | Deletes group `group_name`                  |
| `groups user_name`                     | Displays all groups to which a user belongs |
| `getent group group_name`              | Display all users in group                  |
| `grep group_name /etc/group`           | Display all users in group                  |


### Renaming user

| Commands                                                  | Description                                                                                                                                                         |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sudo usermod -l new_username old_username`               | Change username (but this will not change the home directory)                                                                                                       |
| `sudo groupmod -n new_usernam old_username`               | Change groupname                                                                                                      |
| `sudo mkdir /home/new_username`                           | Create home directory for user `new_user`                                                                                                                           |
| `sudo chown new_username:new_username /home/new_username` | Gives full ownership of `new_username` to the user `new_username` and to the group `new_username`                                                                   |
| `sudo usermod -d /home/new_username new_username`         | Sets `/home/new_username` as home directory for user `new_username`. (It does not automatically create the directory or move the files)                             |
| `sudo usermod -d /home/new_username -m new_username`      | Sets `/home/new_username` as home directory for user `new_username`. (creates the directory if does not exist and move the files from old home dir to new home dir) |

### Switch user
| Commands       | Description                                     |
|----------------|-------------------------------------------------|
| `su user_name` | Switch user (from `current_user` to `user_name`)|

<br>

***

<br>

## 🪄 Wildcards

<br>

**1. `*` (Asterik):** Matches zero or more characters in a filename or string.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls *`              | list all files in a directory                                   |
  | `ls *.txt`          | match files with a specific extension `.txt` (matches `file1.txt`, `notes.txt`, etc.|
  | `ls file*`          | match all files starting with `file` (Matches `file1`, `file2.txt`, `file_backup`, etc.)|
  | `cp *.jpg /backup/` | copy all `.jpg` files to a `backup` directory)                  |
  | `rm temp*`          | delete all files starting with `temp`                           |
  | `find . -name "*.sh"`| find all files ending with `.sh` in the current directory      |

<br>

> [!IMPORTANT]
> - Escaping Wildcards:** To use a wildcard as a literal character (not as a pattern), escape it with a backslash (`\`).
>   - E.g.: `ls \*.txt` - search for a file named `*.txt`(literally)

<br>

**2. `?` (Question Mark):** Matches exactly one character in a filename or string.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls ????`           | match files with exactly four-character names (matches `file`, `test`, but not `files` or `fi`)|
  | `ls file?`          | match filenames like `file1`, `file2`, etc.                     |

<br>

**3. `[ ]` (Square Brackets):** Matches any one character within the brackets.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls [abc]*`         | match files starting with `a`, `b`, or `c` (matches `apple`, `banana`, `cat`, etc.)|
  | `ls *[123]`         | match files ending with `1`, `2`, or `3`                        |
  | `ls [a-z]*`         | match files starting with a lowercase letter                    |
  | `ls *[0-9]*`        | match files with digits in their names                          |

<br>

**4. `[^ ]` (Negated Character Set):** Matches any character not listed inside the brackets.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls [^ab]*`         | match files not starting with `a` or `b` (matches `cat`, `dog`, `zebra`, etc., but not `apple` or `banana`)|

<br>

**5. `{ }` (Curly Braces):** Matches a comma-separated list of strings or patterns.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls {file1,file2,file3}.txt`| match files with specific names (matches `file1.txt`, `file2.txt`, and `file3.txt`)|
  | `ls *.{txt,log,csv}`| match files with multiple extensions (matches `data.txt`, `errors.log`, `records.csv`, etc.)|

<br>

> [!NOTE]
> - Wildcard are not commands themselves, but are used with other linux commands such as `ls`, `cp`, `rm`, `mv`, `find`, etc.
> - Wildcards match filenames and directory names; they do not search within file content.

## 📬 Connect with Me  
  
<div align="center">

[![X](https://img.shields.io/badge/X-%23000000.svg?logo=X&logoColor=white)](https://twitter.com/VishalKapgate)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?logo=gmail&logoColor=white)](mailto:vishaldk26@gmail.com)
[![LinkedIn](https://custom-icon-badges.demolab.com/badge/LinkedIn-0A66C2?logo=linkedin-white&logoColor=fff)](https://linkedin.com/in/vishalkapgate)

</div>

## 🤝 Contributing
Contributions are welcome!  

- Found an error? Let me know (even spelling mistakes count! 📝).  
- Have useful learning notes? Feel free to fork & enhance this repository!
