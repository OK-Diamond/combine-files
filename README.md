## How do add this to your terminal
- Run:
```powershell
notepad $PROFILE
```
- If prompted to create a file, click accept.
- Paste this into the file:
```
function combine-files {
    & "<path to python - something like C:/Python312/python.exe>" "<path to this folder>/combine-files/combine_files.py" @args
}
```
- Ctrl-S to save, then close the window
- You should now be able to run the script through `combine-files` in your terminal.

Run `combine-files -h` for info on args.