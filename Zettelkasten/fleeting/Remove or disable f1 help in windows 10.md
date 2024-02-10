

1) Navigate to C:\Windows, find helppane.exe, right click, Properties, Security tab, Advanced.  On the top where it says "Owner:", hit change.  Type in your username and hit Check Names, click OK.  Apply.  Hit okay back to the Security tab.  Next to "to change permissions, click edit"  hit Edit.  Hit Add, type in your username and click Check Names.  Hit okay and then on the permissions give yourself Full Control with all boxes checked.  Click Apply, yes, then OK.  Ok again to close the box.  Then right click, rename it, hit enter and click Continue to provide administrator permission. to rename it.  Or simply click the file and press Delete on your keyboard to get rid of it.  Now you can press F1 without having to be bothered by the help pane popup!

2) Open up command prompt, File, run new task, type in regedit and hit enter.  Click yes if there is a popup. 

Please backup your registry before making any changes by clicking File > Export (make sure All is selected under Export Range).  Make sure to scroll up and select the uppermost level before searching, for me it is "Computer".  Then Edit > Find.  Under Find What: helppane.exe and make sure only Data is selected and nothing else.  This should lead you to the keys that point towards the executable which you can then rename or remove at your own risk.   

3) Use a program like Sharpkeys (search it online) to disable the F1 button (not recommended as it will disable the button entirely).

# Conclusion
1. 
1. goto regedit
2. select computer, click menu edit and find helppane.exe
3. remove helppane.exe