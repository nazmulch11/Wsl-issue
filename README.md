# Solve Log error: "/usr/bin/env: ‘bash\r’: No such file or directory" - Docker desktop for Windows

Solution


"One of the issues with Docker (or any Linux/macOS based system) on Windows is the difference in how line endings are handled... the best thing is to avoid the issue by setting git config --global core.autocrlf input which makes git clone using unix endings, and converts windows endings on commit"

So I tried to use the git command $ git config --global core.autocrlf true, to clone again the carpa repository and rebuild all docker images but I got same error log.

However after a few searches I found same error in the issues log of other github repository and after to read all replies I tried to clone again carpa repository using --config core.autocrlf=input as parameter of clone git command such as $ git clone https://github.com/encisosystems/carpa.git --config core.autocrlf=input

It worked for me, the project run ok!
