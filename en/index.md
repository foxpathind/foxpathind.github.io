# Welcome to FoxpathIND Wiki;-)


## Pandoc usage

```
pandoc -f docx -t markdown -o anotherfile.md DecemberTasks.docx

Word should have level styles to work best.
dash,line will go through to bullet list
```


## Add the page listing here

- Update the page list: 

```
/Dropbox/foxpathind.github.io/en/pages$ls -R >PagesList.md
/Dropbox/foxpathind.github.io/en/pages

cd ~/Documents/conversion-folder/Draft
ls *.md > markdownfilelist.md
sed -E -n 's/(^.*.*$)/ * [\1](\1)/gpw pages.md' markdownfilelist.md 
rm markdownfilelist.md

sed -E  -n 's/(^.*[0-9].*$)/[\1](\1)/gp' <toc.md >tocnew.md

sed -E  -n 's/(^.*.*$)/[\1](\1)/gp' <toc.md >tocnew.md

ls -d */ >folderslist.md

```

UNIX Shell
Works with: Bourne Again SHell

The "find" command gives a one-line solution for simple patterns:

find . -name '*.txt' -type f 

"find" can also be used to find files matching more complex patterns as illustrated in the section on Unix Pipes below.

Using "bash" version 4 or later, you can use "globstar" or "dotglob", depending on whether you want hidden directories to be searched:


http://rosettacode.org/wiki/Category:UNIX_Shell


```
#! /bin/bash
# Warning: globstar excludes hidden directories.
# Turn on recursive globbing (in this script) or exit if the option is not supported:
shopt -s globstar || exit
 
for f in **
do
  if [[ "$f" =~ \.txt$ ]] ; then
    echo "$f"
  fi
done

Here is a solution that does not use "find".

#! /bin/bash
 
indent_print()
{
    for((i=0; i < $1; i++)); do
	echo -ne "\t"
    done
    echo "$2"
}
 
walk_tree()
{
    local oldifs bn lev pr pmat
    if [[ $# -lt 3 ]]; then
	if [[ $# -lt 2 ]]; then
	    pmat=".*"
	else
	    pmat="$2"
	fi
	walk_tree "$1" "$pmat" 0
	return
    fi
    lev=$3
    [ -d "$1" ] || return
    oldifs=$IFS
    IFS="
"
    for el in $1/*; do
	bn=$(basename "$el")
	if [[ -d "$el" ]]; then
	    indent_print $lev "$bn/"
	    pr=$( walk_tree "$el" "$2" $(( lev + 1)) )
	    echo "$pr"
	else
	    if [[ "$bn" =~ $2 ]]; then
		indent_print $lev "$bn"
	    fi
	fi
    done
    IFS=$oldifs
}
 
walk_tree "$1" "\.sh$"

A simplified version that gives the same output:

#! /usr/bin/env bash
 
walk_tree() {
	ls "$1" | while IFS= read i; do
		if [ -d "$1/$i" ]; then
			echo "$i/"
			walk_tree "$1/$i" "$2" | sed -r 's/^/\t/'
		else
			echo "$i" | grep -E "$2"
		fi
	done
}
 
walk_tree "$1" "\.sh$"

UnixPipes

As illustrated above, the "find" command can be used with the -name option to match simple patterns. To find files matching more complex patterns, the results of "find" can be piped, e.g.

find . -type f | egrep '\.txt$|\.TXT$'

One way to run a command against each file that is found is to use "xargs", but if there is any possibility that a filename contains a space or tab character, then the following model should be used:

 find . -type f -name "*.txt" -print0 | xargs -0 fgrep sometext
```
- 
