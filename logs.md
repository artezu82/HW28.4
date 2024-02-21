Artem@DESKTOP-SVSCEK5 MINGW64 ~ (main)
$ git clone git@github.com:artezu82/HW28.4.git
Cloning into 'HW28.4'...
warning: You appear to have cloned an empty repository.

Artem@DESKTOP-SVSCEK5 MINGW64 ~ (main)
$ cd HW28.4

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ pwd
/c/Users/Artem/HW28.4

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ cat > index.html
Hello world!

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git add index.html

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html


Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git commit -m "1st commit"
[main (root-commit) 8087e1d] 1st commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ cat > index.html
Good bye the cruel world!

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git add index.html

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git commit -m "changed info"
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git branch --unset-upstream

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git status
On branch main
nothing to commit, working tree clean

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git add index.html
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html


Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git commit -m "changed info"
[main f6af7f1] changed info
 1 file changed, 1 insertion(+)

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ echo "Kind regards, AZ" >> index.html

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git add index.html
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git commit -m "added info"
[main a414851] added info
 1 file changed, 1 insertion(+)

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git checkout -b "develop"
Switched to a new branch 'develop'

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ cat > README.md
Hello, world!

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ cat > LICENCE.md
copyright (c) <year> <copyright holders>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git add README.md

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git add LICENCE.md
warning: in the working copy of 'LICENCE.md', LF will be replaced by CRLF the next time Git touches it

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git commit -m "readme+licence"
[develop 29152fa] readme+licence
 2 files changed, 18 insertions(+)
 create mode 100644 LICENCE.md
 create mode 100644 README.md

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git merge main
Already up to date.

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git status
On branch develop
nothing to commit, working tree clean

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (develop)
$ git checkout main
Switched to branch 'main'

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git merge develop
Updating a414851..29152fa
Fast-forward
 LICENCE.md | 18 ++++++++++++++++++
 README.md  |  0
 2 files changed, 18 insertions(+)
 create mode 100644 LICENCE.md
 create mode 100644 README.md

Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Artem@DESKTOP-SVSCEK5 MINGW64 ~/HW28.4 (main)
$ git push --set-upstream origin main
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 6 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (12/12), 1.56 KiB | 533.00 KiB/s, done.
Total 12 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:artezu82/HW28.4.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
