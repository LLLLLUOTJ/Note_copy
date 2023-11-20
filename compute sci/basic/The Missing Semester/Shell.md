[[shell]]
**Lcture1**
_**Efficiently**_
The shell
interact with your compu
Terminal
bash
->Linux<-
Shell prompt
->(base) lintianjian@lintianjiandeMacBook-Air ~ %
date -> time
echo -> back
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % date

2023年10月23日 星期一 18时18分52秒 CST

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo hello

hello
```
""<-
\ <-
space div each
build in program
file system<-
program langu
Env
->$PATH
all path in compute
which -> know where
number location -> path
like this 
```(base) lintianjian@lintianjiandeMacBook-Air ~ % echo $PATH

/Users/lintianjian/anaconda3/bin:/usr/local/sbin:/usr/local/bin:/Library/Frameworks/Python.framework/Versions/3.11/bin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/Library/Apple/usr/bin
```
in here all in root
relative path
print working direc -> pwd
cd -> change current direc
. -> current direc
.. -> parent direc
ls -> list file in current direc
combine them
~ -> home
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % cd /Users/lintianjian/anaconda3/bin:/usr/local/

cd: no such file or directory: /Users/lintianjian/anaconda3/bin:/usr/local/

(base) lintianjian@lintianjiandeMacBook-Air ~ % cd ../

(base) lintianjian@lintianjiandeMacBook-Air /Users % pwd

/Users

(base) lintianjian@lintianjiandeMacBook-Air /Users % ls

Shared lintianjian
```
cd - -> to the previous
 ls -l -> list the thing of file like wrx who belong
 mv -> move
 mv someone's path to other path -> can even rename
 rm -> rm file
 rm -r/rmdir -> rm dic
 man <- manu pages
 ctrl+L -> clear terminal
 ```
 (base) lintianjian@lintianjiandeMacBook-Air /Users % cd -

~

(base) lintianjian@lintianjiandeMacBook-Air ~ % cd ~

(base) lintianjian@lintianjiandeMacBook-Air ~ % ls -l

-rw-r--r--    1 lintianjian  staff    282 10 21 15:23 utils.py

-rw-r--r--    1 lintianjian  staff    732 10 21 15:20 未命名.ipynb

(base) lintianjian@lintianjiandeMacBook-Air ~ % touch hello.txt

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo hello > hello.txt

(base) lintianjian@lintianjiandeMacBook-Air ~ % mv hello.txt hi.txt

(base) lintianjian@lintianjiandeMacBook-Air ~ % ls

Applications

public_tests-2.py

public_tests.py

utils-2.py

utils-3.py

utils.py

未命名.ipynb

(base) lintianjian@lintianjiandeMacBook-Air ~ % rm hi.txt

//some of them have been delete
 ```
 **Stream**
 -> redef stream
 < file > file
 Hello > file.txt output stream way to file.txt
 cat file.txt -> Hello
 you can do this:
 	cat < file.txt > file2.txt
	cat file2.txt -> Hello
\>> -> attend, don't cover
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % touch hello.txt

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo hello > hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat hello

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat < hello > hello2

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat hello2

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat < hello > hello2

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat hello2

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat < hello >> hello2

(base) lintianjian@lintianjiandeMacBook-Air ~ % cat hello2

hello

hello
```
| -> pipe -> left output input to right
like >> ls -l | tail -n1 -> out put last line of ls -l
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % ls -l | tail -n1

-rw-r--r--    1 lintianjian  staff    732 10 21 15:20 未命名.ipynb
```
For root
surper user
-> sudo -> da as suerper suer
sudo su
$ -> #
lintianjian -> root
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % sudo su

Password:

sh-3.2# exit

exit
```
tee -> see and save
open -> open !

**Lecture2**
define vari
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % foo=bar

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo $foo

bar

(base) lintianjian@lintianjiandeMacBook-Air ~ % foo = bar

zsh: command not found: foo
```
str in bath
- '' and "" is equal in str but not in other
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % echo 'hello'

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo "hello"

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo "hello $foo"

hello bar

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo 'hello $foo'

hello $foo
```
define function
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % vim mcd.sh
```
```
mcd () {

        mkdir -p "$1"

        cd "$1"

}
```
execu and load
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % source mcd.sh
```
using it
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % mcd test

(base) lintianjian@lintianjiandeMacBook-Air test % cd ..
```
- $0 -> name of script
- $1-9 -> vs
- $_ ->  last v
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % rmdir test

(base) lintianjian@lintianjiandeMacBook-Air ~ % mkdir test

(base) lintianjian@lintianjiandeMacBook-Air ~ % cd $_

(base) lintianjian@lintianjiandeMacBook-Air test %
```
- $? -> error
```
(base) lintianjian@lintianjiandeMacBook-Air ~ % echo "hello"

hello

(base) lintianjian@lintianjiandeMacBook-Air ~ % echo $?

0
```
!! last commd
logic
- || -> or
- && -> and
```
(base) lintianjian@lintianjiandeMacBook-Air test % foo=$(pwd)

(base) lintianjian@lintianjiandeMacBook-Air test % echo $foo

/Users/lintianjian/test
```
something using all above
![[Pasted image 20231024110702.png]] 
globin
 \*.sh -> \[\].ch
 word?
 image.{png,jpg}->expend
 {foo,bar}/{a..j}
 ![[Pasted image 20231024112107.png]]
 you can combine with other langurage, too
 ![[Pasted image 20231024112327.png]]
 ![[Pasted image 20231024112404.png]]
 shellcheck
 - give you the whole error mayby
 
 usful tool
 tldr 
 find
 ![[Pasted image 20231024113156.png]]
 locate
 updatedb
 flag -R
 ![[Pasted image 20231024113624.png]]
 history -> print history commd
ctrl + r?
fzf
tree
broot
nnn