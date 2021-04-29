- [Rename the "directory entry" and not the file's name](https://superuser.com/a/488130)
	-	[How does renaming a loaded .net assembly work?](https://stackoverflow.com/a/14775626)
	-	[https://superuser.com/questions/488127/why-can-i-rename-a-running-executable-but-not-delete-it](Why can I rename a running executable, but not delete it?)

1. Start file.exe {parameters} in {working directory}
2. If offset 0x? == notpatched
	1. Append .bak extension to executable's directory entry (name in folder)
	2. Create copy of file without .bak extension
	3. Patch copy at LAA offset
	4. Restart the process with the original command line and working directory.
		

