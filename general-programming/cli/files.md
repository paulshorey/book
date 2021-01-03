# Files

Show hidden files: `ls -a .`  

**`cat ~/ssh/newssh.pub`** read file text, output to STDOUT  
**`sudo echo "some text" >> /some/file`** write 'text' to bottom of file

> **Mac ONLY:**  
> **`cat ~/ssh/newssh.pub | pbcopy`** read file text into clipboard \(Ctrl+C\)  
> **`sudo echo $(pbpaste) >> /some/file`** paste copied text to bottom of file  
> This $\(pbpaste\) seems to avoid having to escape characters which would normally break the CLI command

**Read file:**  
`cat ~/ssh/newssh.pub` \(to stdout\)

**Write to bottom of file:**  
`sudo echo "some text" >> /some/file`

> **Mac ONLY:** **`cat ~/ssh/newssh.pub | pbcopy`** read file text into clipboard \(Ctrl+C\) **`sudo echo $(pbpaste) >> /some/file`** paste copied text to bottom of file This $\(pbpaste\) seems to avoid having to escape characters which would normally break the CLI command

### Bash prepend a text using a temporary file

Here is simple solution using a temporary file to prepend text:

```text
echo 'line 1' > /tmp/newfile
echo 'line 2' >> /tmp/newfile
cat yourfile >> /tmp/newfile
cp /tmp/newfile yourfile
```

Here is one line solution:

```text
echo "text"|cat - yourfile > /tmp/out && mv /tmp/out yourfile
```

**Copy to remote server:**  
`scp myfile.txt remoteuser@remoteserver:/remote/folder/`  
[https://www.simplified.guide/ssh/copy-file](https://www.simplified.guide/ssh/copy-file)

**Find file:**  
`sudo find / -type f -name "postgresql.conf"` \(file name in folder "/"\)  
`find / -type d -name "dir-name-here"` \(find directory\)  
`find / -name "whatever"` \(file or directory\)

**Copy folder to new location**  
First, remove it. Then copy recursively. Then rename \(optional\).  
****`echo 'rm -rf /www/nlp.domains; cp -R /www/ps/www/new/build /www && mv /www/build /www/nlp.domains;' >> ~/.zprofile`  

