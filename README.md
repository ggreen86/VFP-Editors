# VFP-Editors

I wrote several tools for editing VFP forms, classes, menus, tables, and program (prg) files.  Also, I wrote a global search tool, comparison tool, a table browse tool, and a library tool. These all are APP files that run inside the VFP design-time environment. To integrate them I wrote a replacement for the PJX file and associated project manager and a toolbar for using in VFP Design-Time environment to make it easier to access these tools. 

I have added to this repository each of the zip files for each tool-set.  The support zip is required for all tools -- it contains the Active-X components (two) that must be manually registered with REGEDIT32.EXE and a custom Arial TrueType font.  The Active-X components are an Editor component and a spreadsheet grid component.

Features included are:
<ul>
<li>Intellisense,</li>
<li>Code insert (SQL commands, REPLACE WITH command with fields, field lists, list of controls, and RGB() color value),</li>
<li>Code refactoring,</li>
<li>Bookmarks shown in the left sidebar (with fast selection from the right sidebar similar to Eclipse),</li>
<li>Code tips,</li>
<li>Code completion,</li>
<li>Help for commands/syntax,</li>
<li>Code comparison (current method code to last saved method code),</li>
<li>Copy buffers for code snippets (with full edit capability of the snippet list),</li>
<li>Goto definition (opens PRG based functions in a separate editor session),</li>
<li>Where-used references (provides a list with hyperlink jump to the code),</li>
<li>Quick search (text entry into a text box that provides for incremental search in the current edit buffer without having to open an input form that can jump to repeated values),</li>
<li>Code peek,</li>
<li>Line numbers,</li>
<li>Hot keys for commands,</li>
<li>Highlight mode for undeclared variables,</li>
<li>Highlight mode for current selection,</li>
<li>Beautify code,</li>
<li>Win32 DECLARE-DLL insert from list,</li>
<li>Color value selection from color-wheel (RGB() value insert),</li>
<li>Color display of a value in a RGB() command,</li>
<li>Memberdata edit and extension of memberdata beyond the VFP limit,</li>
<li>Macro recording and execution,</li>
<li>Add properties or methods from another form or visual class,</li>
<li>Enhanced printing of the methods or properties,</li>
<li>Enhanced property editor,</li>
<li>Current selected line highlight,</li>
<li>Auto-indention when inserting code,</li>
<li>Change bar for line changes in the left sidebar,</li>
<li>Jump to matching code blocks (i.e., jumps from IF to associated ENDIF and other code blocks such as CASE-ENDCASE or matching parenthesis),</li>
<li>Transpose code at the equal '=' sign (moves what is on the right side of the equal sign to the left side and the left side to the right side),</li>
<li>If there is a missing code block command (i.e., missing the closing ENDIF), then the editor will show the below code blocks without highlight,</li>
<li>Compile errors are shown in a list with hyperlink to the code line with the error,</li>
<li>Show white space toggle,</li>
<li>Quick back navigation to last cursor position (allows forward or backward navigation),</li>
<li>Goto line number,</li>
<li>Display of current cursor position in the status bar,</li>
<li>Display of current selected text length in the status bar,</li>
<li>Display of the current object that is being edited in the method code,</li>
<li>Tooltip text of the full path of the method in the Tab (shows the full object hierarchy),</li>
</ul>

I think the above list covers most of the features that I added. There is also a personalization form for choosing your own color highlights and other features.  Some screen shots of the editors:

Form (SCX) Editor (method edit mode) (The Class VCX Editor is the same layout and can edit all classes in a single classlib):
![2021-04-12_16-03-54](https://user-images.githubusercontent.com/28057069/114871566-698f8c00-9dc7-11eb-8cf2-f3cf7ce9bb83.png)

Form (SCX) Editor (property edit mode):
![2021-04-12_16-08-32](https://user-images.githubusercontent.com/28057069/114871750-9d6ab180-9dc7-11eb-9b6f-f02477b078ae.png)

Menu (MNU) Editor:
![2021-04-12_16-11-31](https://user-images.githubusercontent.com/28057069/114871900-c723d880-9dc7-11eb-95b9-aef91733cfe0.png)

Comparison Tool (showing a comparison of SCX forms):
![2021-04-15_9-25-31](https://user-images.githubusercontent.com/28057069/114876921-cb9ec000-9dcc-11eb-8a0f-d25aff375856.png)

