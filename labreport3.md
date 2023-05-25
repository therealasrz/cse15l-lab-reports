# Lab report 3

---
## Researching Commands
Researching for command `grep`\
## 1.`grep -i` enables case-insensitive searching within a specifies file\

example 1:  searching for "hello" in a file:\
`$ grep -i "hello" string.txt`\
Output:\
`Hello, how are you`\

example 2:  searching for "HeLLo" in a file:\
`$ grep -i "HeLLo" string.txt`\
Output:\
`Hello, how are you`

In general, `-i` enables case-insensitive search in a given file, returning the sentenses that contains the matched words in the file. It's useful when you try to search for keywords related sentances in a file. It's a useful filtering strategy when doing file cleaning.

## 2. `grep -c` displays the count of number of matches

example 1: searching word count for "hello" in a file:\
`$ grep -c "hello" string.txt`\
Output:\
1

example 2: searching word count for "hello" in a file:\
`$ grep -c "HELLO" string.txt`\
Output:\
1

`-i` enables counting number of matches of case-insensitive search in a given file instead of printing the lines themselves., this is specifically useful when running statistical tests on files to calculate the frequency of certain word patterns in certain article

## 3. `grep -o` displays the matched pattern in the result only rather than the entire line

example 1: Extracting URLs from a file\
`$ grep -o "\bhttps?://[^\s]*\b" file.txt`\
Output:\
`http://www.google.com`

example 2: searching word count for "hello" in a file:\
`$ grep -o "HELLO" string.txt`\
Output:\
`Hello`

`grep -o` is useful when you want to extract certain messages that contains the important messages only, such as extracting email addresses, URLs from a file. It's useful when trying to filtering files and extracting certain patterns.

## 4. `grep -v` displays the result that do not match the given pattern

example 1: finding failure in a file\
`$ grep -v "success" file.txt\
Output:\
`An error has occured running this command`

example 2: finding irregular pattern in the file\
`$ grep -o "HELLO" string.txt`\
Output:\
`Good bye my friend`

`grep -v` enables us to displaying lines that do not contain the specified pattern. This is useful when we want to filter the file for sentences that does not match a particular pattern.\

Work Cited: all ideas about the useage of grep commands and inspiration about grep commands are from https://www.geeksforgeeks.org/grep-command-in-unixlinux/ 



