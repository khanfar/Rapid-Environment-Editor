Rapid Environment Editor (RapidEE) is an environment variables editor. It includes an easy to use GUI and replaces the small and inconvenient Windows edit box



![1](https://github.com/user-attachments/assets/7b080416-d832-444b-a98e-2b6b138d8cc8)

Show environment variables and values as an editable tree.

RapidEE doesn't require installation and could be run as a "portable application".

Automatically checking for invalid pathnames and filenames

nspector shows miscellaneous information about variables: name, type, value, short file name in the 8.3 naming convention for each long file name and vice versa.

Command line parameters
Set variable value
rapidee -S [-C] [-E] [-U | -M] variableName newValue

-S
set value
-C
cleanup variable value (remove duplicate paths and empty elements)
-E
if variable doesn't exist then create it as expandable
-U
process user variables (default option)
-M
process system (machine) variables


Command line	Result
rapidee -S foo a;b;c;;b	foo=a;b;c;;b
rapidee -S -C foo a;b;c;;b	foo=a;b;c
Insert value
rapidee -I [-C] [-E] [-U | -M] variableName value

-I
insert value
Command line	Result
rapidee -S foo a;b
rapidee -I foo c	
foo=c;a;b
Append value
rapidee -A [-C] [-E] [-U | -M] variableName value

-A
append value
Command line	Result
rapidee -S foo a;b
rapidee -A foo c	
foo=a;b;c
Remove value
rapidee -R [-C] [-U | -M] variableName value

-R
remove value
Command line	Result
rapidee -S foo a;b;c
rapidee -R foo b	
foo=a;c
Delete variable
rapidee -D [-U | -M] variableName

-D
delete variable


