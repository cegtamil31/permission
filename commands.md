## Vim Commands
| COMMAND | DESCRIPTION |
| --- | --- |
| a | Append text after the cursor |
| A | Append text at the end of the line |
|b|goes to the beginning of a word|
| c | Change operator |
| ce | Change made from the cursor to the end of the word |
| c$ | Change made from the cursor to the end of the line |
| c#e | Changes # number of words from the cursor |
| c#$ | Changes # number of lines from the cursor | 
| d | Delete operator |
| de |  Deletes the word until start of the current word including the last character | 
| dw | Deletes the word until start of the next word excluding the first character |
| d$ | Deletes the entire line leaving it's space |
| d#e | Deletes the # number of word until start of the current word including the last character |
| d#w | Deletes the # number of word until start of the next word excluding the first character | 
| d#$ | Deletes the # number of lines leaving its space | 
| dd | Deletes the entire line along with it's space |
| #dd | Deletes the # number of lines along with it's space | 
| e | Moves to the word's last character |
|:e (filename)|opens the specified file|
| #e | Moves # number of words' last character |
| gg | Goes to the start  of the file |
|ge|end of the previous word|
| G | Goes to the bottom of the file |
| #G | Goes to the # line number in the file | 
| Ctrl + G | Shows the location of the cursor in the file |
| h | Moves the cursor left | 
| i | Insert the text before the cursor |
| I | Insert the text before the first non-balnk in the line |
| Ctrl + I | Traverses forward during search |
| j | Moves the cursor down |
| k | Moves the cursor up |
| l |  Moves the cursor right |   
|n|to search for the same phrase again in forward direction|
|N|to search for the same phrase again in backward direction|
|o|opens a new line and puts in insert mode (lowercase)|
|O|puts in insert mode at the cursor position (uppercase)|
|ctrl+o|to go back where you come from|
|x|used for deleting a character|
|p|to paste the clipboard after the cursor|
|P|to paste the clipboard before the cursor|
|:q!|exits the editor without saving the changes made|
|r(a,b,c,..2,....)|replace a character at the cursor posiiton|
|R|to replace more than one character|
|:r (filename)|retrieves the contents of the specified file and puts below the cursor point|
|:r (external command)|retrieves the output of the external command|
|:r (filename)|read the specified file|
|:s/old/new/|substitutes the given word with a new word at the cursor position|
|:s/old/new/g|substitutes all the occurences  of the word with new word at the particular line|
|:%s/old/new/g|changes every occurence of the string in the whole file|
|:%s/old/new/gc|prompts for substitution globally|
|:#i,#s/old/new/g|substitution takes place between the specified line numbers (#,#)|
|:set ic|to ignore case in searching and substituting|
|:set hls|for highlighting partial matches in searches|
|:set is|highlights the first occurence of the matched pattern from the cursor|
|:set noic|cancels the ignore case option|
|:set nohls|to remove the highlighting option|
|u|undo changes for the word the cursor is position at|
|U|undo changes for the entire line|
|v|visual selelction operator, used for selecting text|
|v :w (filename)|selects text and writes into the specified file|
|vw|visual word selection|
|w|move to the next word|
|:wq|saving and exiting a file|
|:w (filename)|writes the copy of current file to the specified file|
|#w(1,2,3)|to move the cursor to specified words forward|
|W|next word and also used for skiping special characters|
|x|used for deleting a character|
|x|used for deleting a character|
|y|yank operator,used for copying text|
|yw|yank operator,used for copying word|
|/ (pattern)|searches for the specified pattern|
|/ (pattern) \c|used for ignoring case for specific search|
|:! (external command)|used for executing external command|
|%|used in paranthesis matching for the purpose of debugging|
|^|navigates to the beginning of the text of a particular line|
|0|navigates to the beginning of the line|
|$|navigates to the end of the text of the current line|
|? (pattern)|backward pattern search|

## USER AND GROUP PERMISSION MODES

| COMMAND | DESCRIPTION |
| --- | --- |
|4|read permission|
|2|write permission|
|1|execute permission|
|0|no permission|
|7|read,write,execute permission|
|6|read,write permission|
|5|read,execute permission|
|3|write,execute permission|
|-rwx-rw-r--|(rwx)-user permission,(rw)-group permission,(r)-others|
|chmod u(+,-,=)(r/w/x)/g(+,-,=)(r/w/x)/o(+,-,=)(r/w/x) (file name/folder name)|change modes for user,groups & others|
|chmod 755(eg) (file name/folder name)|(7)-user permission,(5)-group permission,(5)-other|
|users|list users|
|cut -d : -f1 /etc/passwd|list application users|
|groups|list groups|
|cut -d : -f1 /etc/group|list application groups|
|adduser username|add new user|
|sudo usermod -a -G groupname username|add user to existing respective group|




