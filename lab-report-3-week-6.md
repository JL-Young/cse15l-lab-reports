# Lab Report 3 - Week 6

Return to [index](https://jl-young.github.io/cse15l-lab-reports/)

---
## Streamlining SSH Configuration

Set an alias in config file that corresponds to logging into specific servers. This allows one to type a short alias instead of the entire user@server line.

- edit .ssh/config file through VSCode

`~/.ssh/config`

![config-file](lab-report-3/SSH-streamline_config-file.jpg)

- log in to account using alias

`ssh <user>`

![log-in](lab-report-3/SSH-streamline_log-in.jpg)

- copy file to account using alias

`scp <file> <user>`

![file-move](lab-report-3/SSH-streamline_file-move.jpg)

---
## Setup Github Access from ieng6

Creation of keys that link an account in a remotely hosted server to a Github account.
Similar to with local machines, this allows one to access Github repositories (or whichever permissions granted) from the remote server.

- public key location on Github

[Github > Settings > Keys](https://github.com/settings/keys)

![public-key-location-github](lab-report-3/SSH-Keys_public-location-github.jpg)

- public key location on ieng6 server

```
ssh <user> 
cd .ssh
more id_rsa.pub
```

![public-key-location-laptop](lab-report-3/SSH-Keys_public-location-ieng6.jpg)

- private key location

`ssh <user> "cd .ssh; ls"` (private key is file id_rsa)

![private-key-location](lab-report-3/SSH-Keys_private-location-ieng6.jpg)

- git commands to commit and push a change to Github from ieng6

```
ssh <user>
git clone <repository SSH link>
\\ make changes (e.g. mv <file>)
\\ perform following commands within cloned repository
git add <changed file>
git commit -m "<write commit comment>"
git push
```

![ieng6-git-commands](lab-report-3/SSH-Keys_commands.jpg)

[link to commit](https://github.com/JL-Young/demo/commit/497e4d1610ac4a39aa62db6dcb93d91ad0a3a192)

![ieng6-commit-link](lab-report-3/SSH-Keys_commit-link.jpg)

---
## Copy Whole Directories with `scp -r`

To copy an entire directory is not the same as copying a single file.
The `scp` command allows one to copy __recursively__ to achieve this.
Moreover, one can combine multiple commands in one line by using a semicolon.
Additionally, commands to be performed within a remote server are enclosed by parentheses after the log in command.

- copy markdown-parse directory to ieng6

`scp -r <directory> <user@server>:.` 
(:. specifies home directory)

![ieng6-copy-directory](lab-report-3/Directory_copy-1.jpg)

![ieng6-copy-directory](lab-report-3/Directory_copy-2.jpg)

- log in, compile, and run markdown-parse tests on ieng6

```
ssh <user>
javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java
java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest
```
(Linux commands)

![ieng6-compile-run](lab-report-3/Directory_compile-run.jpg)

- copy markdown-parse, and compile and run tests on ieng6 in one line

```
scp -r markdown-parser cs15lsp22<3-letter ID>@ieng6.ucsd.edu:.; ssh <user> "cd markdown-parser;/software/CSE/oracle-java-17/jdk-17.0.1/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java;/software/CSE/oracle-java-17/jdk-17.0.1/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"
```

![ieng6-combined-commands](lab-report-3/Directory_one-line-1.jpg)

![ieng6-combined-commands](lab-report-3/Directory_one-line-2.jpg)