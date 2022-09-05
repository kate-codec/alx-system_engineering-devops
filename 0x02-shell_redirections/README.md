echo Hello, World
# Write a script that prints “Hello, World”, followed by a new line to the standard output.


echo "\"(Ôo)'"
# Write a script that displays a confused smiley "(Ôo)'


cat /etc/passwd
# Display the content of the /etc/passwd file.


cat /etc/passwd /etc/hosts
# Display the content of /etc/passwd and /etc/hosts


tail /etc/passwd
#  Display the last 10 lines of /etc/passwd


head /etc/passwd
#  Display the first 10 lines of /etc/passwd


head --lines=3 iacta | tail --lines=1
#  Write a script that displays the third line of the file iacta.
The file iacta will be in the working directory
You’re not allowed to use sed

echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"
# Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line

ls -la > ls_cwd_content
# Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.

echo -en "" | tail --lines=1 iacta >> iacta
# Write a script that duplicates the last line of the file iacta
The file iacta will be in the working directory

find . -name '*.js' -type f -delete
# Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.



find -mindepth 1 -type d | wc -l
# Write a script that counts the number of directories and sub-directories in the current directory.
The current and parent directories should not be taken into account
Hidden directories should be counted


ls -t | head
# Create a script that displays the 10 newest files in the current directory.
Requirements:
One file per line
Sorted from the newest to the oldest

sort | uniq -u
# # Create a script that takes a list of words as input and prints only words that appear exactly once.
Input format: One line, one word
Output format: One line, one word
Words should be sorted

grep -i root /etc/passwd
# Display lines containing the pattern “root” from the file /etc/passwd


grep -i bin /etc/passwd | wc -l
# Display the number of lines that contain the pattern “bin” in the file /etc/passwd


grep -iA 3 root /etc/passwd
# Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.


grep -iv bin /etc/passwd
#  Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.


grep -i "^[a-z]" /etc/ssh/sshd_config
# Display all lines of the file /etc/ssh/sshd_config starting with a letter.
include capital letters as well


tr Ac Ze
# Replace all characters A and c from input to Z and e respectively.


tr -d cC
# Create a script that removes all letters c and C from input 


rev
# Write a script that reverse its input


cut -d':' -f1,6 /etc/passwd | sort    
# Write a script that displays all users and their home directories, sorted by users.
Based on the the /etc/passwd file


find . -empty -printf "%f\n"   
#  Write a command that finds all empty files and directories in the current directory and all sub-directories.
Only the names of the files and directories should be displayed (not the entire path)
Hidden files should be listed
One file name per line
The listing should end with a new line
You are not allowed to use basename, grep, egrep, fgrep or rgrep


find -type f -name "*.gif" -printf "%f\n" | rev | cut -d'.' -f 2- | rev | LC_ALL=C sort -f   
# Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.
Hidden files should be listed
Only regular files (not directories) should be listed
The names of the files should be displayed without their extensions
The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
One file name per line
The listing should end with a new line
You are not allowed to use basename, grep, egrep, fgrep or rgrep


cut -c 1 | tr -d '\n' | sort   
# An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. Read more.
Create a script that decodes acrostics that use the first letter of each line.
The ‘decoded’ message has to end with a new line
You are not allowed to use grep, egrep, fgrep or rgrep


tail -n +2 | cut -f1 | sort | uniq -c | sort -nr | head -11 | tr -s ' ' | cut -d' ' -f3   
# Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.
Order by number of requests, most active host or IP at the top
You are not allowed to use grep, egrep, fgrep or rgrep
