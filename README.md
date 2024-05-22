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

Table Browser (showing multi-tab selection for table and selection of fields to be included in display with memo field contents displayed in editboxes):
![2021-04-16_13-44-51](https://user-images.githubusercontent.com/28057069/115063874-29f59c80-9eba-11eb-9509-8d3b81e950b8.png)

Comparison Tool (showing a comparison of SCX forms):
![2021-04-15_9-25-31](https://user-images.githubusercontent.com/28057069/114876921-cb9ec000-9dcc-11eb-8a0f-d25aff375856.png)

<b>Installation Guidelines</b>

The tools are already compiled to APP files and are ready to be used.  They depend on the following Active-X components:

<ul>
<li>cmax40.dll - the main editor component</li>
<li>bbListView.ocx - listview component</li>
<li>ax_ug.ocx - excel like grid component that supports multiple sheets</li>
</ul>

The following components are only licensed for use with these tools:

<ul>
<li>cmax40.dll (CodeMax)</li>
<li>bblistview.ocx (bbListView)</li>
</ul>

Neither of the two above components are available any longer for license purchase; however, my license allows me to distribute with these tools.  CodeMax v2.x source code was released and can be found on the internet; the version included here is v3.x with modifications to the source code by me for faster language parsing.

CodeMax requires MSXML 4.0 min and has a dependency to the MS Visual C++ redistributable package; bbListView has a dependency to MS Visual C++ redistributable package as well.  Both redistributables are included in the support zip.

ax_ug.ocx is the Ultimate Grid (available as open-source on CodeProject website) packaged as an activex.  Look for documentation on it on CodeProject; note that the method and event names are not exactly the same.  You can use the object browser in VFP to extract the names.  This also requires the MS Visual C++ redistributable package.

The various versions of the MS Visual C++ redistributable packages are for each of the different active-xs.  The active-x components will require manually registering them via Regsvr32.exe.  First install the MS Visual C++ redistributable packages and the MSXML support (if not already installed).  Then register the components.

There are other ActiveX components that are used that should be available with VFP installed.  These include the MS Image control, MS Image Combobox, MS RichText Editor, MS Treeview, and MS ListView controls.

The custom GKKArial.ttf file is used in the editors in the search/find textboxes.  It has a special space character so as to preserve spaces entered for searching (so these are not trimmed via ALLTRIM() command).  The GKKConvert.fll file is another support file - place in same folder as the APP files; it is used by the Struct.vcx class (can be found on internet).

You can look at the various .ISS files which are INNO Script files for the INNO Setup Installer for more information.

<b>Usage Tips</b>

The project manager replacement was written to allow for opening forms, visual classes, programs using the tools above, as well as, the normal built-in VFP editors.  The first time you try to open a form, visual class, or program, it will prompt you for the app file location.  Once located, it is stored.

These editors do support the adding/editing/deleting of properties.  The property display/sheet sheet in these two editors is the ax_ug.ocx component which gives very good visual display of the properties and the setting of values.

Alot of the functionality of Thor tool has also been incorporated into these editors.  Having the source code you are free to add more as needed.


<b>Code Editor Tips/Features</b>

<ul>
<li>Current line is background highlighted.</li>
<li>Block text selection supported; press the alt key while dragging with the cursor to select a column block.   Selected text can be copied as a block for insertion.</li>
<li>There is tooltip help for commands (hover over a command to see the help text); F1 will open help with the selected text.</li>
<li>Pasting code lines tries to automatically following the current indent; this is not always on target...</li>
<li>Bookmark references are retained correctly when lines before it is deleted.</li>
<li>On the right side a blue bar is displayed that represents bookmarks.  Hovering will show a tooltip of the line.  You can click on the blue bar to quickly navigate to the line.</li>
<li>On the toolbar next to the bookmarks are two navigation buttons.  The left one will move back to the previous cursor position; the right one moves forward to position that you just moved back from.</li>
<li>The code peek has a cookie crumb on the right to move between 'code peeks'.  To use right click on a method and then select 'Code Peek'.  This brings up a window over the code editor that displays the method.  Right-click on a method in the code-peek window and it will then display that method and now a series of red/yellow dots is displayed on the top-right corner of the code peek window.  Clicking allows movement between the different methods (tooltip text displays the method name).  Clicking back onto the main editor will auto-close the code peek window.  This is where a bug occurs in that the right bookmark display of the blue bars is not restored to the correct zorder.
<li>You can customize the color selections and other features -- see the more toolbar button.</li>
<li>The editor displays the matching IF-ENDIF and other blocks.  Put the cursor on one of the code blocks and it will highlight the matching code block.  Note that the CASE-ENDCASE is highlighted but not the CASE withing the code block.</li>
<li>The matching will aide in displaying when you do not have a closing code block.  It will not display the matches.  For example, the ENDDO would not be highlighted below since the ENDIF is missing.</li>

    DO WHILE .T.
        IF m.variable != .T.
    ENDDO

<li>There is autocompletion of commands.  When you press enter after typing IF something=somethingelse, it will automatically add the ENDIF at the same indent level as the IF.  Same with SCAN, DO WHILE, DO CASE, FOR.</li>
<li>The code block matching expects to the find ENDFOR and not LOOP as the end of a FOR loop.</li>
<li>The Form editor will show a picklist of fields for the aliases defined in the data environment of the form; triggered by typing the alias name and then a period.</li>
<li>A right-click menu is available on the Treeview display of the objects/methods that is context sensitive to the item clicked on.  DON'T TRY TO DELETE AN OBJECT FROM THE FORM/CLASS -- this will not save correctly.</li>
<li>For ActiveX components the codesense does not get class specific PEMS; i.e., for treeview, it would not display a list of PEMs for oleTreeview.Row.(PEM List).</li>
<li>You can copy methods and properties from other forms or classes (in the SCX and VCX editors) to the form/class being edited.  See buttons on toolbar.</li>
<li>The VCX editor can open the entire VCX class library or just a single class in the library file.  Selecting the VCX class library will open the entire library; selecting the class opens just that class.</li>
<li>If the VCX or SCX is in use somewhere else, the editor will still open it but just in read-only mode.</li>
<li>There is a toolbar button to display non-declared variables on the toolbar; does a yellow background highlight of the variable.</li>
<li>There is a toolbar button to display all occurrences of a selected phrase; does an off-green highlight of the selected phrase.</li>
<li>Yellow change bars are displayed on the left for edited lines; cleared on save</li>
<li>The save will be default first save the original files with a .bak extension added</li>
<li>Errors on compile are shown in the bottom and you can double-click on a line to jump to it.</li>
<li>The editor supports incremental search.  In the toolbar, there is a textbox - start typing text and it will jump to the first matching text.  Clicking on the search button next to it (one with green arrow) will jump to the next matching text.</li>
<li>You can have your cursor on a word and press the 'Quick find text' toolbar button and it will jump to the next occurrence.</li>
<li>There is a bug in the search/replace -- it does not skip the highlighted change (been annoyance but have not yet fixed).</li>
<li>Macro functions are available for recording and playback for repeating keystrokes.</li>
<li>The printing uses RTF format for output</li>
<li>Right-clicking on a method tab displays a short-cut menu of choices;  you can revert back to original and you can compare to original version (as well as tab close options)</li>
<li>The color toolbar button will insert the selected color as an RGB() expression</li>
<li>Selecting an RGB() expression and then using the right-click menu you can display the color on screen</li>
<li>There is a copy buffer on the right-click menu</li>
</ul>

<b>Known Issues</b>

The visual class editor and form editor do not support deleting of objects nor the addition of objects.  I began coding a replacement for the visual layout editor but it has not been finished -- it will only display.  I use the standard VFP editors to do the layout and then switch to my editors for the coding.

The assign and access methods are not saved when adding from the properties sheet.  Somewhere I made a change that affected this saving and have not corrected it...
