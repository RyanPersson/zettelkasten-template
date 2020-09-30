# scripts-building


#done

You need several scripts.

Need to be able to launch 2 from windows taskabr.
    create/open note 
 &  create/open person object (keep private?)

run-zet.bat:
```shell
@echo off

cd C:\Anki\public

For /f "tokens=2-4 delims=/ " %%a in ('date /t') do (set mydate=%%a-%%b-%%c)

SET /P filename=[Please enter the filename]

(
echo # %filename%
echo %mydate%
) >> %filename%.md


code . --goto %filename%.md

exit
```

Switch to WSL syntax & call with other script. #todo 
<br>

---

<br>

run-build-todos.bat: Calls bash script from windows side. Can by pinned to taskbar.
```shell
$echo off

cd C:\Anki\scripts

wsl.exe ./build-todos
```

NEED call-build-person.bat calls wsl.exe ./build-person

NEED call-build-card.bat calls wsl.exe ./build-card 

need build-todos:   current.
```shell
#!/usr/bin/bash

cd ../public

ag -i \#todo > ToDo-output.txt

mv ToDo-output.txt $desktop
```

Try using with grep? Just curious
Need to use: 
```
grep \#todo ../public/*.md
```

Also need:

gather done

order todos

Wow actually works, and backwards too.


IF my vscode is at the root instance, it can access both public & personal, even if they are seperate repositories.

Pasting media should work for this too

---

<br>
another good script. build-todos
```shell
#!/usr/bin/bash

cd ../public

grep \#todo *.md > public-output.txt  # grabs #todo lines with grep

sed -i 's/.*.md/\r\[\[&\]\]\r/' public-output.txt  # replaces .*.md with \n [[.*.md]] \n
cat public-output.txt
sed -i 's/.md\]\]/\]\]/' public-output.txt # replaces .md]] with ]]
cat public-output.txt

# mv renames the file public-output.txt
mv public-output.txt ..

exit
```