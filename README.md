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

The visual class editor and form editor do not support deleting of objects nor the addition of objects.  I began coding a replacement for the visual layout editor but it has not been finished -- it will only display.  I use the standard VFP editors to do the layout and then switch to my editors for the coding.  

These editors do support the adding/editing/deleting of properties.  The property display/sheet sheet in these two editors is the ax_ug.ocx component which gives very good visual display of the properties and the setting of values.

Alot of the functionality of Thor tool has also been incorporated into these editors.  Having the source code you are free to add more as needed.
