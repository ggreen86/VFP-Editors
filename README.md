# VFP-Editors

I wrote several tools for editing VFP forms, classes, menus, tables, and program (prg) files. These all are APP files that run inside the VFP design-time environment. To integrate them I also wrote a replacement for the PJX file and associated project manager. 

Features included are:

Intellisense,
Code insert (SQL commands, REPLACE WITH command with fields, field lists, list of controls, and RGB() color value),
Code refactoring,
Bookmarks shown in the left sidebar (with fast selection from the right sidebar similar to Eclipse),
Code tips,
Code completion,
Help for commands/syntax,
Code comparison (current method code to last saved method code),
Copy buffers for code snippets (with full edit capability of the snippet list),
Goto definition (opens PRG based functions in a separate editor session),
Where-used references (provides a list with hyperlink jump to the code),
Quick search (text entry into a text box that provides for incremental search in the current edit buffer without having to open an input form that can jump to repeated values)
Code peek
Line numbers
Hot keys for commands
Highlight mode for undeclared variables
Highlight mode for current selection
Beautify code
Win32 DECLARE-DLL insert from list
Color value selection from color-wheel (RGB() value insert)
Color display of a value in a RGB() command
Memberdata edit and extension of memberdata beyond the VFP limit
Macro recording and execution
Add properties or methods from another form or visual class
Enhanced printing of the methods or properties
Enhanced property editor
Current selected line highlight
Auto-indention when inserting code
Change bar for line changes in the left sidebar
Jump to matching code blocks (i.e., jumps from IF to associated ENDIF and other code blocks such as CASE-ENDCASE or matching parenthesis)
Transpose code at the equal '=' sign (moves what is on the right side of the equal sign to the left side and the left side to the right side)
If there is a missing code block command (i.e., missing the closing ENDIF), then the editor will show the below code blocks without highlight
Compile errors are shown in a list with hyperlink to the code line with the error
Show white space toggle
Quick back navigation to last cursor position (allows forward or backward navigation)
Goto line number
Display of current cursor position in the status bar
Display of current selected text length in the status bar
Display of the current object that is being edited in the method code
Tooltip text of the full path of the method in the Tab (shows the full object hierarchy)

I think the above list covers most of the features that I added. There is also a personalization form for choosing your own color highlights and other features.  Some screen shots of the editors:

Form (SCX) Editor (method edit mode) (The Class VCX Editor is the same layout and can edit all classes in a single classlib):
![2021-04-12_16-03-54](https://user-images.githubusercontent.com/28057069/114871566-698f8c00-9dc7-11eb-8cf2-f3cf7ce9bb83.png)

Form (SCX) Editor (property edit mode):
![2021-04-12_16-08-32](https://user-images.githubusercontent.com/28057069/114871750-9d6ab180-9dc7-11eb-9b6f-f02477b078ae.png)

Menu (MNU) Editor:
![2021-04-12_16-11-31](https://user-images.githubusercontent.com/28057069/114871900-c723d880-9dc7-11eb-95b9-aef91733cfe0.png)


