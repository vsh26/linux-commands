# 🛠️ Linux Commands

If you are beginner in Linux, and have only ever used Windows, do consider reading the following articles, before directly jumping upon the commands, to understand the Linux better.
- [Exploring Linux: Its Origins, Why It’s Different, and How It Compares to Windows and macOS](https://controlplusblog.hashnode.dev/exploring-linux-its-origins-why-its-different-and-how-it-compares-to-windows-and-macos)
- [Why the Juice Seller at MacOS Gets the Order of a Linux User, But Windows Looks Confused](https://controlplusblog.hashnode.dev/why-the-juice-seller-at-macos-gets-the-order-of-a-linux-user-but-windows-looks-confused)

<br>

## ☰ Table of Contents
* [Some basic commands](#-some-basic-commands) - `pwd`, `whoami`, `clear`, `su`,  `exit`, `reboot`, `shutdown`, `date`, `ls`
* [Working with directories](#-working-with-directories) - `mkdir`, `rmdir`, `cd`, `cp`, `mv`
* [Working with files](#-working-with-files)
  + [Reading files](#1%EF%B8%8F⃣-reading-files) - `cat`, `tac`, `less`, `more`, `head`, `tail`
  + [Creating files](#2%EF%B8%8F⃣-creating-files) - `touch`
  + [Deleting files](#3%EF%B8%8F⃣-deleting-files) - `rm`
  + [Editing files](#4%EF%B8%8F⃣-editing-files) - `vi`, `nano`
  + [Dividing file into smaller sections](#5%EF%B8%8F⃣-dividing-file-into-smaller-sections) - `split`
  + [Comparing files](#6%EF%B8%8F⃣-comparing-files) - `cmp`, `diff`
  + [Finding files](#7%EF%B8%8F⃣-finding-files) - `find`, `locate`
* [Operations on file contents](#-operations-on-file-contents)
  + [Sorting the file content](#1%EF%B8%8F⃣-sorting-the-file-content) - `sort`
  + [Finding unique](#2%EF%B8%8F⃣-finding-unique) - `uniq`
  + [Searching the content](#3%EF%B8%8F⃣-searching-the-content) - `grep`, `egrep`
  + [Shuffle content](#4%EF%B8%8F⃣-shuffle-content) - `shuf`
  + [Word count](#5%EF%B8%8F⃣-word-count) - `wc`
  + [String operation command](#6%EF%B8%8F⃣-string-operation-command) - `awk`, `cut`, `sed`, `tr`, `truncate`, `echo`
* [Utility Commands](#-utility-commands) - `history`, `!`, `man`, `which`, `whereis`, `bc`, `calc`, `uptime`, `script`, `alias`, `unalias`
* [Zip and unzip files and folders](#%EF%B8%8F-zip-and-unzip-files-and-folders) - `gzip`, `gunzip`, `tar`, `zip`, `unzip`
* [Downloading files from internet](#-downloading-files-from-internet) - `wget`, `curl`
* [Software package management](#-software-package-management)
  + [Debian-based distributions](#1%EF%B8%8F⃣-debian-based-distributions) - `apt`, `dpkg`
  + [RPM (RedHat Package Manager)-based distributions](#2%EF%B8%8F⃣-rpm-redhat-package-manager-based-distributions) - `yum`, `dnf`, `rpm`
* [Service management](#%EF%B8%8F-service-management) - `systemctl`
* [Shell environment and Environment variables](#-shell-environment-and-environment-variables) - `printenv`, `unset`, `source`
  + [Shell environment](#shell-environment)
  + [Environment variables](#environment-variable)
* [Working with remote servers](#-working-with-remote-servers) - `ssh`, `scp`
* [Linux file system](#%EF%B8%8F-linux-file-system)
  + [What is "Root directory (`/`)"?](#what-is-root-directory-)
  + [Important sub-directories under root directory](#important-sub-directories-under-root-directory) - `/bin`, `/sbin`, `/boot`, `/dev`, `/etc`, `home`, `lib`, `lib64`, etc.
  + [Why do we see `/bin -> /usr/bin`, `/sbin -> /usr/sbin`, `/lib -> /usr/lib`, `/lib64 -> /usr/lib64` on modern systems?](#why-do-we-see-bin---usrbin-sbin---usrsbin-lib---usrlib-lib64---usrlib64-on-modern-systems)
  + [What is `usr.is.merged?`](#what-is-usrismerged)
* [Working with permissions](#%EF%B8%8F-working-with-permissions) - `chmod`, `chown`
  + [`chmod` Command](#-chmod-command)
  + [`chown` Command](#-chown-command)
  + [Default Permissions](#default-permissions)
  + [What is `umask`?](#what-is-umask)
  + [Special permission bits](#special-permission-bits)
  + [ACL (Access Control List)](#acl-access-control-list)
* [Memory info](#-memory-info) - `free`, `top`, `du`, `df`
* [System info](#%EF%B8%8F-system-info) - `hostname`, `lscpu`, `arch`, `lsbsk`, `uname`
* [Process Management](#%EF%B8%8F-process-management) - `ps`, `pgrep`, `kill`, `top`, `htop`, `pkill`, `jobs`, `bg`, `fg`, `nohup`, `at`, `crontab`
* [Networking](#-networking) - `ifconfig`, `ping`, `telnet`, `netstat`, `traceroute`
* [User Management](#-user-management)
  + [Adding user](#adding-user) - `useradd`, `adduser`
  + [Delete user](#delete-user) - `userdel`
  + [Group management](#group-management) - `addgroup`, `groupmod`, `groupdel`
  + [Renaming user](#renaming-user) - `usermod`
  + [Switch user](#switch-user) - `su`
* [Bash Shell Operators](#-bash-shell-operators)
  + [Redirection Operators](#1-redirection-operators) - `>`, `>>`, `<`, `2>`, `2>>`, `&>`, `2>&1`, `<<<`
  + [Pipes and Command Chaining](#2-pipes-and-command-chaining) - `|`, `||`, `&&`, `;`
  + [Control Operators & Grouping](#3-control-operators--grouping) - `&`, `()`, `{}`
  + [Command Substitution](#4-command-substitution) - `$(...)`, `` `...` ``
  + [Arithmetic Operators](#5-arithmetic-operators) - `+`, `-`, `*`, `/`, `%`, `**`, `++`, `--`, `+=`, `-=`
  + [Logical Operators](#6-logical-operators) - `!`, `-a`, `-o`, `&&`, `||`
  + [Comparision Operators](#7-comparison-operators) - `==`, `!=`, `-eq`, `-ne`, `-lt`, `-gt`, `-z`, `-n`
* [Wildcards](#-wildcards) - `*`, `?`, `[ ]`, `[^ ]`, `{ }`

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>
  
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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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
  | `tail -f -5 filename`  | display last 5 lines from `filename` (real-time)             |

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🪛 Utility Commands

<br>

| Examples            | Description                                                     |
|-----------          |-------------                                                    |
| `uptime`            | how long the system has been running, the number of active users, and the system load averages|
| `man <command>`     | read or get more info about a command                           |
| `<command> --help`  | check syntax and options available for a command                |
| `which <command/ program>` | loacte binary for a command or program |
| `whereis <command/ program>` | locate binary, source code and `man` pages for command or program|
| `bc`                | binary calculator                                               |
| `cal`               | displays calendar                                               |
| `script`            | record a terminal session (type `exit` to stop recording        |

<br>

### 📌 `history` command

| Examples            | Description                                                     |
|-----------          |-------------                                                    | 
| `history`           | display previously used commands                                |
| `history -c`           | clear current session history                                |
| `history -w`           | write current history to history file (`.bash_history`)      |
| `history -d <line_number>` | delete specific entry from history file by line number   |

<br>

> [!NOTE]  
> - History is stroed in `.bash_history` file of the user's home directory.
> - Don't delete the `.bash_history` file directly unless required (i.e., `rm ~/.bash_history`)

> [!CAUTION]
> Do not directly use API keys and passwords into commands as they are saved in history file and can be accessed.
> 
> Solution 1: `read -s -p "Enter API key: " API_KEY`
> - `read` - read user input
> - `-s` - silent mode (input not shown on screen)
> - `-p` - display prompt message
> - `API_KEY` - variable used to store the user input (temporary variable)
> 
> Solution 2: Give one blank space before writing command (command will not be saved in history)
> This will only work if `$HISTCONTROL` (bash environment variable) has `ignorespace` in it.

<br>

### 📌 `alias` command
| Examples            | Description                                                     |
|-----------          |-------------                                                    | 
| `alias name="command"`| create shortcuts for commands, valid only for current session |
| `unalias name`      | removes alias `name`                                            |

<br>

> [!NOTE]  
> For permenant changes, add alias to `.bashrc` file.
> - It is a shell script file that runs automatically when we start a new terminal session
> - `source ~/.bashrc` - reload bash file without restarting the current terminal session

<br>

**Example 1 (Temporary alias):**

- ```
  alias gac="git add . && git commit -m"
- **Usage:** `gac "Commit message"`

**Example 2 (Permanent alias):**
- Open `.bashrc` file
- Add the piece of code at the end of file
- ```
  gac(){
    git add . && git commit -m "$*"
  }
- Reload file, `source ~/.bashrc`
- **Usage:** `gac "Commit message"`



<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🧮 Shell environment and Environment variables

### Shell environment
The **shell environment** is the collection of settings, environment variables, functions, and configurations that the shell loads and uses when it starts.

**Components of shell environment**
| Component                 | Description                                        |
| ------------------------- | -------------------------------------------------- |
| **Environment Variables** | Variables like `PATH`, `HOME`, `USER`, `JAVA_HOME` |
| **Aliases**               | Shortcuts for commands (e.g., `alias ll='ls -l'`)  |
| **Functions**             | Custom mini-scripts                                |
| **Prompt settings**       | How your terminal looks (`PS1`)                    |
| **Shell options**         | Settings like `set -o noclobber`                   |
| **Startup files**         | Like `.bashrc`, `.bash_profile`, etc.              |

<br>

**Where is the shell environment defined?**
| File               | Purpose                                       |
| ------------------ | --------------------------------------------- |
| `~/.bashrc`        | User-specific settings for interactive shells |
| `~/.profile`       | Run at login (also loads `.bashrc`)           |
| `/etc/profile`     | System-wide login shell config                |
| `/etc/bash.bashrc` | System-wide interactive shell config          |

<br>

**How to view your current shell environment?**
```
env         # List all environment variables
printenv    # Similar to env
set         # Lists all shell variables (environment + functions)
```
<br>

### Environment variable
An environment variable is a key-value pair stored in your shell’s environment that can affect how processes and programs run.

Example:
```
PATH=/usr/local/bin:/usr/bin:/bin
JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
EDITOR=nano
```

Each of these variables holds some value that the system or applications refer to.

<br>

**Common use cases**
| Variable    | Purpose                                                                                  |
| ----------- | ---------------------------------------------------------------------------------------- |
| `PATH`      | Tells the shell where to look for executable programs (like in `/bin`, `/usr/bin`, etc.) |
| `JAVA_HOME` | Points to the Java installation directory                                                |
| `HOME`      | The current user’s home directory                                                        |
| `SHELL`     | Default shell (e.g., `/bin/bash`)                                                        |
| `USER`      | Username                                                                                 |
| `PWD`       | Present working directory                                                                |
| `EDITOR`    | Default text editor                                                                      |


<br>

**Steps to set an environment variable**

1️⃣ List all existing environment variables
  - `printenv`

2️⃣ Check a specific variable
  - `echo $VARIABLE_NAME`

3️⃣ Setting a temporary environment variable (for the current shell session)
  - `export VARIABLE_NAME=value`

4️⃣ Setting a permanent environment variable (for the future session)
  - Open your `~/.bashrc` or `~/.profile` (shell configuration file)
  - Add `export VARIABLE_NAME=value`
  - Save this file
  - Reload configuration file using `source ~/.bashrc`

5️⃣ Unsetting a temporary environment variable
  - `unset VARIABLE_NAME`

6️⃣ Unsetting a permanent environment variable
  - Open `./bashrc` file, locate the line that exports the variable you want to unset
  - Delete or comment out the line and save the file
  - Reload configuration file using `source ~/.bashrc`

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🌐 Working with remote servers

Read this article, [Mastering SSH: Secure Remote Access with Keys and Configurations](https://controlplusblog.hashnode.dev/mastering-ssh-secure-remote-access-with-keys-and-configurations), to learn more about SSH.

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ssh [OPTIONS] [USER@]HOST [COMMAND]`| Secure Shell (used to securely connect to a remote system over a network)|
  | `ssh user@hostname` | access remote server                                            |
  | `ssh -p 2222 user@hostname` | using specific port                                     |
  | `ssh user@example.com "ls -l /var/www"` | running command on a remote host            |
  | `scp [OPTIONS] [SOURCE] [DESTINATION]` | Secure Copy ( copy files or directories securely between a local and a remote system, or between two remote systems) |
  | `scp file.txt user@hostname:/path/to/destination` | copying files to/from remote host |

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🗂️ Linux file system

<br>

The Linux File System is how data is stored, accessed, and managed on a Linux system. `ext4` (fourth extended file system) is the most commonly used file system in Linux.
- We install Linux onto a partition which is formatted as `ext4`
- Then the partition is mounted at `/` — making it the **root filesystem**
- Linux follows a tree-like hierarchical structure, starting from a root directory `/`, and branching into various subdirectories.

<br>

**"In Linux, everything is a file."**
- Every resource—files, directories, devices, sockets, pipes, and even processes—is treated as a file or file-like object.
- This simplifies how the system interacts with various components — by using a **common interface**: file descriptors and read/write operations.

<br>

### What is "Root directory (`/`)"?
- Top-most level of the Linux file system hierarchy
- Starting point or base of the file system tree, from which all other directories and files branch out.
- All directories and files are organized under it, no matter which physical disk they’re on.

<br>

### Important sub-directories under root directory

The Filesystem Hierarchy Standard (FHS) is followed by sub-directories, which is used by most modern Linux distributions.

![image](https://github.com/user-attachments/assets/aacfbcea-1b28-41b8-a46f-d64ea3427b85)

- **`/bin`**
  - `/bin` stands for “binary”
  - It is a directory that contains user-essential binary executables (compiled programs) for core commands, needed for basic system operation — even in single-user mode or during system recovery.
  - These can be used by all users
  - Commands/ Tools: `ls`, `cp`, `mv`, `rm`, `mkdir`, `cat`, `bash`, etc.
    
- **`/sbin`**
  - `/sbin` stands for "system binaries"
  - It contains binary executables (compiled programs) that are used for system maintenance, repair, booting, and administration.
  - They are mostly used by `root` users
  - Commands/ Tools: `mount`, `fsck`, `reboot`, `shutdown`, `ifconfig`, `ip`, `init`, `modprobe`, `fdisk`, `mkfs`
 
- **`/boot`**
  - `/boot` is a directory that contains all the files needed to boot your Linux system, before the actual operating system (kernel + userland) is running.
  - It's separate from the rest of the Linux system because:
    - It needs to be accessible very early during boot
    - The system doesn’t yet load file systems like `/home` or `/usr` at that point
    - It may use simpler filesystems (like ext4) for compatibility
  - ⚠️ Avoid editing files here — a mistake can make your system unbootable.
    
- **`/dev`**
  - `/dev` contains special files called “device files” that represent hardware devices and virtual devices on your system.
  - These are not regular files or binaries — they are interfaces to hardware managed by the kernel.
  - Most files are dynamically created and managed by:
    - The Kernel
    - The `udev` device manager
  - We can even read/write to these files to communicate with hardware.
  - There are two main types of files in `/dev`:
    - Character devices (`c`) - Data flows one character at a time (like keyboards, serial ports)
    - Block devices (`b`) - Data is transferred in blocks (like HDDs, SSDs, USBs)

- **`/etc`**
  - `/etc` contains system-wide configuration files and directories for the Linux operating system and installed software.
  - It contains configuration files for:
    - The system itself (hostname, users, networking)
    - Installed services and daemons (like SSH, Apache, cron)
    - Startup scripts and init system configs

- **`/home`**
  - `/home` is the directory where all regular users’ personal data and settings are stored.
  - Each user has a subdirectory under `/home` — this is their home directory.
  - Regular users own their home directories and can read/write inside.
  - Other users cannot access each other’s home dirs by default.
  - Admins (`root`) can access all of them.
  - On some systems (like servers), `/home` may be on a separate partition or disk to isolate user data.

- **`/lib`**
  - `/lib` contains shared libraries needed by the essential binaries in `/bin` and `/sbin`.
  - A library is a collection of code (functions, routines) that many programs can share, rather than duplicating that code inside each binary. These are like the "helper files" that programs rely on to run.
  - Types:
    - Shared libraries (`.so` → shared object)
    - Static libraries (`.a` → archive, less common in `/lib`)
  - What's typically inside `/lib`:
    - Low-level C standard libraries
    - Math, memory, and I/O functions
    - Dynamic linker/loader
    
- **`/lib64`**
  - `/lib64` contains `64-bit` shared libraries — specifically, essential `64-bit` system libraries needed by `64-bit` binaries in `/bin` and `/sbin`.
  - On 64-bit Linux systems:
    - 64-bit binaries expect their shared libraries in /lib64
    - 32-bit binaries (if supported) expect them in /lib
  -  Without this separation, a 32-bit and 64-bit version of the same library would overwrite each other.

- **`/lost+found`**
  -`/lost+found` is a special directory created by the `ext4`, `ext3`, and `ext2` file systems to store "orphaned files", after filesystem corruption or unexpected shutdowns, if found during a disk check (`fsck`).
  - The file system repair tool (`fsck`) may find blocks of data that don’t belong to any known file or directory. Instead of discarding them, it stores them in `/lost+found`.
  - It is empty most of the time.
  - If not empty: files with numeric names like `#12345` — these are recovered inode references, not real filenames.
  - You may need to manually inspect the contents (with `file`, `strings`, or `cat`) to understand what was recovered.
  
- **`/media`**
  - `/media` is the standard mount point for removable media (mostly plug-and-play devices), such as USB drives, CDs/DVDs, SD cards, external hard disks, etc.
  - Mount point is a directory where the connection with main filesystem tree happens.
  - Linux automatically mounts external devices when you plug them in.

- **`/mnt`**
  - `/mnt` is a standard directory used as a temporary mount point for manually mounting file systems — such as internal partitions, ISO images, NFS shares, and other storage devices.
  - Unlike `/media`, it is not automatically managed.
  - It’s meant for system administrators or advanced users to mount devices or file systems manually.
    
- **`/opt`**
  - `/opt` stands for “optional” — it is used to install third-party software packages that aren’t part of the default Linux distribution.
  - Think of it as a place for manually installed, large applications that live outside the package manager (like `apt`, `dnf`, or `pacman`).
  - You install software into `/opt` when:
    - It's a standalone app (like a full GUI application or a development tool)
    - You're not using the package manager (e.g., installing from a `.tar.gz` or `.run` file)
    - You want to keep it separate from system-managed packages
  - Each package usually lives in its own subdirectory under /opt.

- **`/proc`**
  - `/proc` is a virtual filesystem that provides a real-time interface to the Linux kernel.
  - It shows live information about your system, hardware, processes, and kernel internals — all in the form of files and directories.
  - It’s mounted automatically at boot and doesn’t occupy real disk space.
  - Everything inside is generated on-the-fly by the kernel.
  - Exa: `cpuinfo`, `meminfo`, etc.

- **`/root`**
  - `/root` is the home directory of the `root` (superuser) account on a Linux system.
  - Why doesn’t home directory for root user live in `/home/root`?
    - `/home` might be on a separate partition, and that partition might not be mounted early during boot.
    - The root user must always have access to their home directory — especially during rescue or maintenance mode.

- **`/run`**
  - `/run` is a temporary, RAM-based filesystem used to store system information and runtime data — like PIDs, sockets, and lock files — that are created and used while the system is running.
  - It is cleared on reboot
    
- **`/snap`**
  - `/snap` is the mount point for installed Snap packages. (When a software is installed via Snap, the actual application gets mounted inside `/snap`)
  
- **`/srv`**
  - `/srv` stands for "service" — it is intended to store data served by the system’s network services, such as:
    - Web servers (e.g., Apache, Nginx)
    - FTP servers
    - File sharing (e.g., NFS, Samba)
    - Other hosted content
  - It holds service-specific data (content of the program to be served), not the programs themselves.
  - Linux does not populate `/srv` by default. It’s up to the system admin or the application to place content there if following FHS standards.
    
- **`/sys`**
  - `/sys` is a virtual filesystem (called sysfs) that exposes information and control interfaces for the Linux kernel.
  - It provides a live view of hardware devices and kernel subsystems — and sometimes allows you to modify them.
  - Purpose of `sys`:
    - Read hardware information (devices, buses, drivers)
    - Change kernel parameters (within limits)
    - Debug and monitor hardware status
    - Communicate with the kernel about system settings
      
- **`/tmp`**
  - `/tmp` is a directory for storing temporary files created by programs and users.
  - It’s meant for:
    - Short-lived data
    - Scratch space for apps
    - Files that don’t need to persist across reboots
  - It is writable by all users, but files are automatically deleted after some time — usually on reboot or after a timeout set by the system.
    
- **`/usr`**
  - `/usr` stands for “Unix System Resources” — despite sounding like it’s just for "user files", it's not for personal user data.
  - Instead, `/usr` contains read-only userland programs and data that are shared across the system.
  - It's basically a second root (`/`) — for all non-essential, multi-user system files.
  - `/usr/bin` : contain non-essential user binaries (`gcc`, `python`, `git`, `node`, `curl`, etc.)
  - `/usr/sbin` : contain non-essential system binaries (`sshd`, `apachectl`, `dpkg-reconfigure`, `useradd`, `passwd`, etc.)
  - `/usr/lib` : contains shared libraries and internal binaries needed by the programs in `/usr/bin` and `/usr/sbin`.
    
- **`/var`**
  - `/var` stands for "variable" and contains data that is expected to change over time — such as logs, caches, mail, spool files, and even package manager metadata.
  - It is writable, unlike `/usr` or `/lib`, and is designed to store dynamic, growing data. 

<br>

### Why do we see `/bin -> /usr/bin`, `/sbin -> /usr/sbin`, `/lib -> /usr/lib`, `/lib64 -> /usr/lib64` on modern systems?

**Symbolic Link/ Symlink/ Soft Link:** A special file that acts as a shortcut or pointer to another file or directory.

In modern Linux systems (especially Ubuntu, Fedora, Arch, etc.), there's a file system simplification effort to merge:
- `/bin` into `/usr/bin`
- `/sbin` into `/usr/sbin`
- `/lib` into `/usr/lib`
- `lib64` into `/usr/lib64`
But for backward compatibility, the `/bin`, `sbin`, `lib`, `lib64` names still exists (as symlink).

<br>

### What is `usr.is.merged`?
It is a marker file used by the system to indicate that this system uses the modern merged `/usr` filesystem layout.

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***
<br>

## 🛡️ Working with permissions

<br>

![image](https://github.com/user-attachments/assets/e6a7a340-4815-4fea-8b2a-520e5634ba7d)

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
     
  2. **Permissions:** Next 9 characters, divided into groups of three. Each group specify the permissions for Owner, Group and Others respectively.
     
* Breakdown of each permission:
  - `r` (read): Permission to read the file or list directory contents.
  - `w` (write): Permission to modify the file or add/remove files in a directory.
  - `x` (execute): Permission to run the file as a program or enter a directory.

  ![image](https://github.com/user-attachments/assets/fc4054ef-574d-4047-bc19-3c2922f3bdcb)

* Exa: `-rwxr-xr--` means:
  - **File type (-):** Regular file
  - **Owner (`rwx`):** The file owner can read (`r`), write (`w`), and execute (`x`).
  - **Group (`r-x`):** Members of the group can read (`r`) and execute (`x`), but not write.
  - **Others (`r--`):** All other users can only read (`r`).

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

![image](https://github.com/user-attachments/assets/86eea5be-a206-4644-975f-31330824f157)

<br>

  - Structure of octal permissions: Permissions are written as three digits, where each digit corresponds to a specific category:
    - First digit: Owner
    - Second digit: Group
    - Third digit: Others

  - Permissions are represented by three bits:
    - `r` (read) = 4
    - `w` (write) = 2
    - `x` (execute) = 1
      
  - The total value for a permission set is the **sum** of these numbers:

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

    | Examples            | Description                                                     |
    |-----------          |-------------                                                    |
    | `chmod 744 file.txt`| Full permissions for the owner, and read-only for others        |
    | `chmod 666 file.txt`| Read and write permissions for everyone                         |
    | `chmod 751 file.txt`| Owner has full permissions, group has read/execute, others have execute only|
    | `chmod 750 file.txt`| No permissions for others                                       |

  <br>
 
  - **Examples:**
    
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
    
    | Examples            | Description                                                     |
    |-----------          |-------------                                                    |
    | `chown user file.txt`| sets `user` as the owner of file.txt                           |
    | `chown username:groupname file.txt` | sets `username` as the owner and `groupname` as the group|
    | `chown :groupname file.txt`| change the group only                                    |
    | `chown -R username:groupname directory/`| change ownership for a directory and all its contents|
    | `chown --reference=source_file target_file`| set ownership to match another file      |

  <br>

### Default permissions
- When a file or directory is created in Linux, it is given default permissions based on:
  - The type of object (file or directory)
  - The user’s umask value

<br>

### What is `umask`?
- `umask` (short for user file creation mask) is a setting in Linux/Unix systems that controls the default permissions given to newly created files and directories.
- When a file or directory is created, Linux:
  - Starts with a default maximum permission
  - Files: `666` (`rw-rw-rw-`)
  - Directories: `777` (`rwxrwxrwx`)
- Subtracts the umask value from that default
- The result becomes the actual permission
  
  ```
  Final Permission = Default Permission - umask
  ```
  
  | Type      | Default | Umask | Final Permission  |
  |-----------|---------|-------|-------------------|
  | File      | 666     | 022   | 644 (rw-r--r--)   |
  | Directory | 777     | 022   | 755 (rwxr-xr-x)   |

<br>

- **Checking current `umask ` value**
  ```
  umask

- **Changing `umask` value**
  - Temporary (Current shell session):
    
    ```
    umask 027
    
  - Permanent: Edit your shell config file (`~/.bashrc`, `~/.zshrc`, etc.)
    
    ```
    echo "umask 027" >> ~/.bashrc
    source ~/.bashrc

- **Common `umask` values and meanings:**
  
    | umask | File Permission | Dir Permission | Description                              |
    | ----- | --------------- | -------------- | ---------------------------------------- |
    | 022   | 644             | 755            | Default on most systems (world-readable) |
    | 027   | 640             | 750            | More secure (no access for others)       |
    | 077   | 600             | 700            | Private (owner-only access)              |

  <br>

### Special permission bits
Linux provides three special permission bits in addition to the standard `rwx` (read, write, execute):

  | Special Bit | Use On           | Purpose                                             | Symbol                        | Numeric |
  | ----------  | ---------------- | --------------------------------------------------- | ----------------------------- | ------- |
  | **SUID**    | Executable files | Run file as file **owner**                          | `rws` (`s` in user exec bit)  | `4`     |
  | **SGID**    | Files & dirs     | Run file as **group owner** OR inherit group in dir | `rws` (`s` in group exec bit) | `2`     |
  | **Sticky**  | Directories      | Restrict deletion to file **owners only**           | `t` (`t` in others' exec bit) | `1`     |

***Special permission bits are added in front of the usual 3-digit mode***

1. **SUID (Set User ID)**
  - When a **file with SUID** is executed, it runs as the **file’s owner**, not the user running it.
  - Used for programs that need elevated privileges temporarily.

2. **SGID (Set Group ID)**
   - On files: When a user runs a file with SGID, it runs with the file’s group privileges.
   - On directories: Files and directories created inside inherit the parent directory’s group, instead of the user’s default group.

3. **Sticky Bit**
   - The Sticky Bit is a special permission used only on directories, and it prevents users from deleting or renaming each other's files — even if they have write access to the directory.

- Reading these in `ls -la`:
  
  | Output Example | Meaning                     |
  | -------------- | --------------------------- |
  | `-rwsr-xr-x`   | SUID set                    |
  | `-rwxr-sr-x`   | SGID set on file            |
  | `drwxr-sr-x`   | SGID set on directory       |
  | `drwxrwxrwt`   | Sticky bit set on directory |

> [!WARNING]  
> SUID can be dangerous if misused — a buggy or malicious script with SUID could give root-level access. That's why:
> - Never set SUID on scripts (.sh, .py) — only on binaries
> - Be cautious which programs have SUID set (e.g., find / -perm -4000 lists all)

<br>

### ACL (Access Control List)
- ACL (Access Control List) allows fine-grained control over who can access a file or directory — more than just one user, one group, and others.
- With ACL, you can give multiple users and groups custom permissions on a single file or directory.

> [!WARNING]  
> ACLs provide powerful control, but can become complex and harder to audit. Use them when standard permissions are not enough — and document your ACL changes well.


<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 💾 Memory info

<br>

  | Examples            | Description                                                         |
  |-----------          |-------------                                                        |
  | `free`              | check free RAM space                                                |
  | `free -h`           | check free RAM space (human-readable)                               |
  | `top `              | check % memory and CPU utilization                                  |
  | `du`                | check disk utilization                                              |
  | `du -h`             | check disk utilization (human-readable)                             |
  | `df`                | check filesystem available and disk space allocated                 |
  | `df -h`             | check filesystem available and disk space allocated (human-readable)|

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🔄️ Process Management

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ps`                | Process status                                                  |
  | `ps aux`            | Process status (`a`: all processes, `u`: user-readble, `x`: background processes (those without terminal)|
  | `ps -ef`            | Show all running processes                                      |
  | `ps -ef \| grep java` | Check if a process(java) running or not                       | 
  | `ps -u`             | Show processes for the current user                             |
  | `ps -p 1234`        | Display specific processes by PID                               |
  | `ps aux --sort=-%mem`| Sort processes by memory usage                                 |
  | `pgrep chron`       | Get PID of process `chron`                                      |
  | `kill [PID]`        | stop a process by PID                                           |
  | `kill -9 [PID]`     | stop a process by PID (`-9` means forcefully)                   |
  | `pkill httpd`       | Stop a process by its name, here `httpd` service                |
  | `top`               | Live, real-time view of system processes                        |
  | `htop`              | Live, real-time view of system processes (more user-friendly)   |
  | `jobs`              | See all active jobs                                             |
  | `bg`                | Resume job in background                                        |
  | `fg`                | Resume job in foreground                                        |
  | `nohup ./script.sh &` | (No Hnag Up -  It allows a command to continue running in the background even after the user has logged out of the terminal session )Running script in background |
  | `at`                | schedule a script to run on a particular date/time              |
  | `crontab`           | schedule a script to run on a particular date/time              |

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🛜 Networking

<br>

  | Examples            | Description                                                     |
  |-----------          |-------------                                                    |
  | `ifconfig`          | Check IP of your machine (older command, may not work)          |
  | `ip`                | Utility for managing networking                                 |
  | `ip a`              | View IP addresses of all network interfaces                     |
  | `ethtool  -i enx0`  | Check if interface `enx0` is virtual or physical                |
  | `ip link set enx0 down` | Set the interface `enx0` down (Not recommended, if its a primary interface)|
  | `ip link set enx0 up`   | Set the interface `enx0` up                                 |
  | `ping URL`          | check if a server or website is accesible or not                |
  | `ping IP`           | check if an IP is accissible or not                             |
  | `dig`               | DNS lookup utility                                              |
  | `dig URL`           | Show DNS resolution for the URL                                 |
  | `dig URL @8.8.8.8`  | Resolve URL through DNS server `8.8.8.8`                        |
  | `ip route`          | Display, add, modify, or delete static routes in the IP routing table |
  | `resolvectl status` | Shows current DNS resolution status                             |
  | `telnet IP Port`    | check if a IP:PORT is accessible and open or not                |
  | `netstat -putan \| grep 80` | check if port is open or not on our server              |
  | `traceroute`        | check all hubs in network path to reach a website               |
  | `sudo losf -i :80`  | Check if service is running on the port                         |
  | `sudo ufw status`   | Check uncomplicated firewall status (internal firewall)         |
  | `sudo ufw enable`   | Enable firewall (default: incoming off, outgoing on)            |
  | `sudo ufw allow ssh` | Allow incoming SSH connections (do this before enabling `ufw`) |
  | `sudo ufw allow http` | Allow incoming HTTP connections                               |

  <br>

  - `/etc/resolve.conf` - It is a configuration file on Unix-like systems that specifies DNS (Domain Name System) servers your system uses to resolve domain names to IP addresses.

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

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

### `sudo`
Not every user can use `sudo` to do any task. The user has to be in the `sudoers` file (`etc/sudoers`).

| Commands                                                  | Description                                                                                                                                                         |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sudo usermod -aG sudo new_user`                          | Adds user `new_user` to group `sudo`. This will allow `new_user` to run commands with `sudo`. (It means `new_user` now has administrative privileges)               |
| `sudo cat /etc/sudoers`                                   | Display the content of `sudoers` file, which is a system file used to configure sudo privileges for users.                                                          |
| `sudo visudo`                                             | Opens the `sudoers` file in the default editor and performs syntax validation before saving, preventing potential misconfigurations.                                  |



<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 📟 Bash Shell Operators

Shell operators are symbols or keywords that let you:
- Chain commands
- Redirect input/output
- Control flow
- Work with variables and files


### 1. Redirection Operators

| Operator | Description                             | Example                             |
|----------|-----------------------------------------|-------------------------------------|
| `>`      | Redirect stdout (overwrite)             | `echo Hello > file.txt`             |
| `>>`     | Redirect stdout (append)                | `echo World >> file.txt`            |
| `<`      | Redirect stdin from file                | `cat < input.txt`                   |
| `2>`     | Redirect stderr                         | `ls nonfile 2> error.log`           |
| `2>>`    | Append stderr to file                   | `ls x 2>> err.log`                  |
| `&>`     | Redirect stdout and stderr              | `command &> all.log`                |
| `2>&1`   | Redirect stderr to stdout               | `command 2>&1 > combined.log`       |
| `<<<`    | Here-string (send a string to stdin)    | `grep root <<< "root:x:0:0"`        |

<br>

### 2. Pipes and Command Chaining

| Operator | Description                                    | Example                               |
|----------|------------------------------------------------|----------------------------------------|
| `\|`      | Pipe output of one command to another           | `ls \| grep ".txt"`                     |
| `\|\|`     | Run second command **only if first fails**      | `mkdir folder \|\| echo "Failed"`       |
| `&&`     | Run second command **only if first succeeds**   | `make && echo "Build success"`        |
| `;`      | Run multiple commands sequentially              | `echo A ; echo B`                     |

<br>

### 3. Control Operators & Grouping

| Operator | Description                                    | Example                                 |
|----------|------------------------------------------------|------------------------------------------|
| `&`      | Run command in background                      | `sleep 10 &`                             |
| `()`     | Run grouped commands in **subshell**           | `(cd /tmp && ls)`                        |
| `{}`     | Group commands in **current shell**            | `{ echo one; echo two; }`               |

<br>

### 4. Command Substitution

| Operator  | Description                                      | Example                            |
|-----------|--------------------------------------------------|------------------------------------|
| `$(...)`  | Run command and insert its output                | `echo "Today is $(date)"`          |
| `` `...` `` | Old syntax (use `$(...)` instead)             | `` echo `date` ``                  |

<br>

### 5. Arithmetic Operators

Used within `(( ))`, `let`, or `[[ ]]`.

| Operator | Description        | Example                          |
|----------|--------------------|----------------------------------|
| `+ - * / %` | Basic arithmetic  | `echo $((5 + 3))`                |
| `**`     | Exponentiation     | `echo $((2**3))`                 |
| `++ --`  | Increment/Decrement | `((x++))`                        |
| `+= -=`  | Compound assignment | `((x+=5))`                       |

<br>

### 6. Logical Operators

| Operator | Description              | Example                            |
|----------|--------------------------|------------------------------------|
| `!`      | NOT                      | `[[ ! -f file.txt ]]`              |
| `-a`     | AND (legacy)            | `[[ -f a -a -r a ]]`               |
| `-o`     | OR (legacy)             | `[[ -f a -o -f b ]]`               |
| `&&`     | AND (modern)            | `[[ -f a && -r a ]]`               |
| `\|\|`     | OR (modern)             | `[[ -f a \|\| -f b ]]`               |

<br>

### 7. Comparison Operators

| Operator | Description               | Example                         |
|----------|---------------------------|---------------------------------|
| `==`     | Strings equal             | `[[ "$a" == "$b" ]]`            |
| `!=`     | Strings not equal         | `[[ "$a" != "$b" ]]`            |
| `-eq`    | Equal (numeric)           | `[[ $a -eq $b ]]`               |
| `-ne`    | Not equal (numeric)       | `[[ $a -ne $b ]]`               |
| `-lt`    | Less than (numeric)       | `[[ $a -lt $b ]]`               |
| `-gt`    | Greater than (numeric)    | `[[ $a -gt $b ]]`               |
| `-z`     | String is empty           | `[[ -z "$a" ]]`                 |
| `-n`     | String is not empty       | `[[ -n "$a" ]]`                 |

<br>

To learn more about each operator: `man bash`

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

<br>

***

<br>

## 🪄 Wildcards

<br>

Wildcards (also called globs) are special characters used by the shell (like Bash) to match patterns in filenames or strings. They're mainly used in filename expansion, searching, and command-line automation.

<br>

| Wildcard             | Meaning                                           | Example              | Matches                          |
| -------------------- | ------------------------------------------------- | -------------------- | -------------------------------- |
| `*`                  | Matches **zero or more characters**               | `ls *.txt`           | `a.txt`, `notes.txt`, `test.txt` |
| `?`                  | Matches **exactly one character**                 | `ls ?.txt`           | `a.txt`, `b.txt`                 |
| `[abc]`              | Matches **one character from the set**            | `ls file[12].txt`    | `file1.txt`, `file2.txt`         |
| `[a-z]`              | Matches **one character in a range**              | `ls file[a-c].txt`   | `filea.txt`, `fileb.txt`         |
| `[!abc]` or `[^abc]` | Matches **any char *not* in set**                 | `ls file[!3].txt`    | `file1.txt`, `file2.txt`         |
| `{a,b}`              | **Brace expansion** (not a wildcard, but similar) | `echo {Mon,Tue}.log` | `Mon.log`, `Tue.log`             |


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

**5. `{ }` (Brace Expansion - not a wildcard, but similar):** Matches a comma-separated list of strings or patterns.

<br>

  | Command             | Description                                                     |
  |-----------          |-------------                                                    |
  | `ls {file1,file2,file3}.txt`| match files with specific names (matches `file1.txt`, `file2.txt`, and `file3.txt`)|
  | `ls *.{txt,log,csv}`| match files with multiple extensions (matches `data.txt`, `errors.log`, `records.csv`, etc.)|

<br>

> [!NOTE]
> - Wildcard are not commands themselves, but are used with other linux commands such as `ls`, `cp`, `rm`, `mv`, `find`, etc.
> - Wildcards match filenames and directory names; they do not search within file content.

<p align="right"><a href="#-table-of-contents">Back to TOC</a></p>

## 📬 Connect with Me  
  
<div align="center">

[![X](https://img.shields.io/badge/X-%23000000.svg?logo=X&logoColor=white)](https://twitter.com/VishalKapgate)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?logo=gmail&logoColor=white)](mailto:vishaldk26@gmail.com)
[![LinkedIn](https://custom-icon-badges.demolab.com/badge/LinkedIn-0A66C2?logo=linkedin-white&logoColor=fff)](https://linkedin.com/in/vishalkapgate)
[![Peerlist](https://img.shields.io/badge/-Peerlist-00AA45?style=flat&logo=peerlist&logoColor=white)](https://peerlist.io/vishalkapgate)

</div>

## 🤝 Contributing
Contributions are welcome!  

- Found an error? Let me know (even spelling mistakes count! 📝).  
- Have useful learning notes? Feel free to fork & enhance this repository!
