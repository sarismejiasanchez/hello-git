
user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ touch hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ls
Documentation.md  hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git init
Initialized empty Git repository in C:/Users/user/Hello Git/.git/

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md
        hellogit.py

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   hellogit.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md


user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Este es mi primer commit"
[main (root-commit) 686d47d] Este es mi primer commit
 1 file changed, 1 insertion(+)
 create mode 100644 hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log
commit 686d47d64da297908967465292ef9128664c547c (HEAD -> main)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md
        hellogit2.py

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add hellogit2.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Este es mi segundo commit"
[main 4dcdad1] Este es mi segundo commit
 1 file changed, 1 insertion(+)
 create mode 100644 hellogit2.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log
commit 4dcdad18b3aa6872bd877acaed84b38c437d3cba (HEAD -> main)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:04:50 2023 -0500

    Este es mi segundo commit

commit 686d47d64da297908967465292ef9128664c547c
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hellogit.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout hellogit.py
Updated 1 path from the index

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log
commit 4dcdad18b3aa6872bd877acaed84b38c437d3cba (HEAD -> main)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:04:50 2023 -0500

    Este es mi segundo commit

commit 686d47d64da297908967465292ef9128664c547c
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hellogit.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se actualiza el texto del print"
[main 82ee4cf] Se actualiza el texto del print
 1 file changed, 1 insertion(+), 1 deletion(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log
commit 82ee4cf7ed8a55d919ef85aed153c0c924d2dedd (HEAD -> main)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:13:27 2023 -0500

    Se actualiza el texto del print

commit 4dcdad18b3aa6872bd877acaed84b38c437d3cba
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:04:50 2023 -0500

    Este es mi segundo commit

commit 686d47d64da297908967465292ef9128664c547c
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log --graph
* commit 82ee4cf7ed8a55d919ef85aed153c0c924d2dedd (HEAD -> main)
| Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
| Date:   Wed Jan 11 21:13:27 2023 -0500
|
|     Se actualiza el texto del print
|
* commit 4dcdad18b3aa6872bd877acaed84b38c437d3cba
| Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
| Date:   Wed Jan 11 21:04:50 2023 -0500
|
|     Este es mi segundo commit
|
* commit 686d47d64da297908967465292ef9128664c547c
  Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
  Date:   Wed Jan 11 20:59:32 2023 -0500

      Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log --graph --pretty=oneline
* 82ee4cf7ed8a55d919ef85aed153c0c924d2dedd (HEAD -> main) Se actualiza el texto del print
* 4dcdad18b3aa6872bd877acaed84b38c437d3cba Este es mi segundo commit
* 686d47d64da297908967465292ef9128664c547c Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log --graph --decorate --all --oneline
* 82ee4cf (HEAD -> main) Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git config --global alias.tree "log --graph --decorate --all --oneline"

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 82ee4cf (HEAD -> main) Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ touch .gitignore

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .gitignore

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se a??ade el .gitignore"
[main 401635f] Se a??ade el .gitignore
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .gitignore

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git diff
diff --git a/hellogit.py b/hellogit.py
index 552c925..c39719b 100644
--- a/hellogit.py
+++ b/hellogit.py
@@ -1 +1 @@
-print("New Hello Git!")
\ No newline at end of file
+print("New Hello Git with changes!")
\ No newline at end of file

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git log
commit 401635f819e95a4eef91a4764de07d8211e8b352 (HEAD -> main)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:26:51 2023 -0500

    Se a??ade el .gitignore

commit 82ee4cf7ed8a55d919ef85aed153c0c924d2dedd
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:13:27 2023 -0500

    Se actualiza el texto del print

commit 4dcdad18b3aa6872bd877acaed84b38c437d3cba
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 21:04:50 2023 -0500

    Este es mi segundo commit

commit 686d47d64da297908967465292ef9128664c547c
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout 686d47d64da297908967465292ef9128664c547c
error: Your local changes to the following files would be overwritten by checkout:
        hellogit.py
Please commit your changes or stash them before you switch branches.
Aborting

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout hellogitgit.py
error: pathspec 'hellogitgit.py' did not match any file(s) known to git

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout hellogit.py
Updated 1 path from the index

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout 686d47d64da297908967465292ef9128664c547c
Note: switching to '686d47d64da297908967465292ef9128664c547c'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((686d47d...))
$ git status
HEAD detached at 686d47d
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((686d47d...))
$ git log
commit 686d47d64da297908967465292ef9128664c547c (HEAD)
Author: sarismejiasanchez <sarismejiasanchez@gmail.com>
Date:   Wed Jan 11 20:59:32 2023 -0500

    Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((686d47d...))
$ git tree
* 401635f (main) Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d (HEAD) Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((686d47d...))
$ git checkout 401635f
Previous HEAD position was 686d47d Este es mi primer commit
HEAD is now at 401635f Se a??ade el .gitignore

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((401635f...))
$ git tree
* 401635f (HEAD, main) Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((401635f...))
$ git checkout main
Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 401635f (HEAD -> main) Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        00_commands.md
        00_documentation.md

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se a??ade el codigo y la documentacion de la clase 00"
[main 16e1af6] Se a??ade el codigo y la documentacion de la clase 00
 2 files changed, 538 insertions(+)
 create mode 100644 00_commands.md
 create mode 100644 00_documentation.md

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 16e1af6 (HEAD -> main) Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 4dcdad1 (HEAD -> main) Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git reflog
4dcdad1 (HEAD -> main) HEAD@{0}: reset: moving to 4dcdad1
4dcdad1 (HEAD -> main) HEAD@{1}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 HEAD@{2}: checkout: moving from main to ccfd892
4dcdad1 (HEAD -> main) HEAD@{3}: reset: moving to 4dcdad1
4dcdad1 (HEAD -> main) HEAD@{4}: reset: moving to 4dcdad1
4dcdad1 (HEAD -> main) HEAD@{5}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 HEAD@{6}: checkout: moving from 4dcdad18b3aa6872bd877acaed84b38c437d3cba to ccfd892
4dcdad1 (HEAD -> main) HEAD@{7}: reset: moving to 4dcdad1
ccfd892 HEAD@{8}: checkout: moving from main to ccfd892
4dcdad1 (HEAD -> main) HEAD@{9}: reset: moving to 4dcdad1
4dcdad1 (HEAD -> main) HEAD@{10}: reset: moving to 4dcdad1
ccfd892 HEAD@{11}: commit: Se actualizan los commands de la clase
16e1af6 HEAD@{12}: commit: Se a??ade el codigo y la documentacion de la clase 00
401635f HEAD@{13}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to main
687e6e9 HEAD@{14}: checkout: moving from main to 687e6e9
401635f HEAD@{15}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to main
687e6e9 HEAD@{16}: checkout: moving from 401635f819e95a4eef91a4764de07d8211e8b352 to 687e6e9
401635f HEAD@{17}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to 401635f
687e6e9 HEAD@{18}: commit: Se a??ade el codigo y la documentacion de la clase 00
401635f HEAD@{19}: checkout: moving from 686d47d64da297908967465292ef9128664c547c to 401635f
686d47d HEAD@{20}: checkout: moving from main to 686d47d64da297908967465292ef9128664c547c
401635f HEAD@{21}: commit: Se a??ade el .gitignore
82ee4cf HEAD@{22}: commit: Se actualiza el texto del print
4dcdad1 (HEAD -> main) HEAD@{23}: commit: Este es mi segundo commit
686d47d HEAD@{24}: commit (initial): Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout ccfd892
Note: switching to 'ccfd892'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ccfd892 Se actualizan los commands de la clase

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((ccfd892...))
$ git checkout main
Warning: you are leaving 4 commits behind, not connected to
any of your branches:

  ccfd892 Se actualizan los commands de la clase
  16e1af6 Se a??ade el codigo y la documentacion de la clase 00
  401635f Se a??ade el .gitignore
  82ee4cf Se actualiza el texto del print

If you want to keep them by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> ccfd892

Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 4dcdad1 (HEAD -> main) Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout ccfd892
Note: switching to 'ccfd892'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ccfd892 Se actualizan los commands de la clase

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((ccfd892...))
$ git tree
* ccfd892 (HEAD) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 (main) Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((ccfd892...))
$ git checkout main
Warning: you are leaving 4 commits behind, not connected to
any of your branches:

  ccfd892 Se actualizan los commands de la clase
  16e1af6 Se a??ade el codigo y la documentacion de la clase 00
  401635f Se a??ade el .gitignore
  82ee4cf Se actualiza el texto del print

If you want to keep them by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> ccfd892

Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git reset --hard ccfd892
HEAD is now at ccfd892 Se actualizan los commands de la clase

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* ccfd892 (HEAD -> main) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$  clase_1git tag

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* ccfd892 (HEAD -> main, tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tag
clase_1

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git checkout tags/clase_1
Note: switching to 'tags/clase_1'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ccfd892 Se actualizan los commands de la clase

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((clase_1))
$ git tree
* 1ae9508 (main) Este es mi sexto commit
* ccfd892 (HEAD, tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git ((clase_1))
$ git checkout main
Previous HEAD position was ccfd892 Se actualizan los commands de la clase
Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 1ae9508 (HEAD -> main) Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git branch login

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 1ae9508 (HEAD -> main, login) Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git switch login
Switched to branch 'login'
M       00_commands.md
M       00_documentation.md

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git status
On branch login
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   00_documentation.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        login.py

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git add login.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git status
On branch login
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   login.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   00_documentation.md


user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git commit -m "Login"
[login ad3803f] Login
 1 file changed, 1 insertion(+)
 create mode 100644 login.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git tree
* ad3803f (HEAD -> login) Login
* 1ae9508 (main) Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git switch main
Switched to branch 'main'
M       00_commands.md
M       00_documentation.md

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   00_commands.md
        modified:   00_documentation.md


user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se actualiza la documentacion y comandos de la clase 01"
[main 70444f4] Se actualiza la documentacion y comandos de la clase 01
 2 files changed, 142 insertions(+), 3 deletions(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 70444f4 (HEAD -> main) Se actualiza la documentacion y comandos de la clase 01
| * ad3803f (login) Login
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git switch main
error: Your local changes to the following files would be overwritten by checkout:
        login.py
Please commit your changes or stash them before you switch branches.
Aborting

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash
Saved working directory and index state WIP on login: df2ee81 Correccion conflicto

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash list
stash@{0}: WIP on login: df2ee81 Correccion conflicto

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git switch main
Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git switch login
Switched to branch 'login'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash list
stash@{0}: WIP on login: df2ee81 Correccion conflicto

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash pop
On branch login
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   login.py

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (3a014ac921c1057561a8b462533f1b412483973b)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git add login.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git commit -m "Login v2"
[login 9b1cc84] Login v2
 1 file changed, 1 insertion(+), 1 deletion(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash
Saved working directory and index state WIP on login: 9b1cc84 Login v2

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash list
stash@{0}: WIP on login: 9b1cc84 Login v2

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git stash drop
Dropped refs/stash@{0} (267d92f4b7078a1b76c9bb06f9749fa2133f3906)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git switch main
Switched to branch 'main'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Commands Clase 01"
[main d83f162] Commands Clase 01
 1 file changed, 59 insertions(+)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* d83f162 (HEAD -> main) Commands Clase 01
| * 9b1cc84 (login) Login v2
| *   df2ee81 Correccion conflicto
| |\
| |/
|/|
* | 76e3379 Git 3 v3
| * 16c53c8 Git 3 login
| *   43e19bb Merge branch 'main' into login
| |\
| |/
|/|
* | de6a856 Git 3 v2
* | 70444f4 Se actualiza la documentacion y comandos de la clase 01
| * ad3803f Login
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git switch login
Switched to branch 'login'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git status
On branch login
nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
$ git switch main
Switched to branch 'main'
M       00_documentation.md

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Documentation Clase 01"
[main 5449135] Documentation Clase 01
 1 file changed, 17 insertions(+), 17 deletions(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git diff login
diff --git a/00_commands.md b/00_commands.md
index dc13bcf..43ea4e5 100644
--- a/00_commands.md
+++ b/00_commands.md
@@ -754,5 +754,144 @@ $ git tree
 * 4dcdad1 Este es mi segundo commit
 * 686d47d Este es mi primer commit

+user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
+$ git switch main
+error: Your local changes to the following files would be overwritten by checkout:
+        login.py
+Please commit your changes or stash them before you switch branches.
+Aborting
+
+user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
+$ git stash
+Saved working directory and index state WIP on login: df2ee81 Correccion conflicto
+
+user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
+$ git stash list
+stash@{0}: WIP on login: df2ee81 Correccion conflicto
+
+user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (login)
+$ git switch main
+Switched to branch 'main'
+
+user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
+$ git switch login

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git merge login
Merge made by the 'ort' strategy.
 hellogit3.py | 2 +-
 login.py     | 1 +
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 100644 login.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git branch -d login
Deleted branch login (was 9b1cc84).

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git branch
* main

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git reflog
ec3bbba (HEAD -> main) HEAD@{0}: merge login: Merge made by the 'ort' strategy.
5449135 HEAD@{1}: commit: Documentation Clase 01
d83f162 HEAD@{2}: checkout: moving from login to main
9b1cc84 HEAD@{3}: checkout: moving from main to login
d83f162 HEAD@{4}: commit: Commands Clase 01
76e3379 HEAD@{5}: checkout: moving from login to main
9b1cc84 HEAD@{6}: reset: moving to HEAD
9b1cc84 HEAD@{7}: commit: Login v2
df2ee81 HEAD@{8}: checkout: moving from main to login
76e3379 HEAD@{9}: checkout: moving from login to main
df2ee81 HEAD@{10}: reset: moving to HEAD
df2ee81 HEAD@{11}: commit (merge): Correccion conflicto
16c53c8 HEAD@{12}: checkout: moving from main to login
76e3379 HEAD@{13}: commit: Git 3 v3
de6a856 HEAD@{14}: checkout: moving from login to main
16c53c8 HEAD@{15}: commit: Git 3 login
43e19bb HEAD@{16}: merge main: Merge made by the 'ort' strategy.
ad3803f HEAD@{17}: checkout: moving from main to login
de6a856 HEAD@{18}: commit: Git 3 v2
70444f4 HEAD@{19}: commit: Se actualiza la documentacion y comandos de la clase 01
1ae9508 HEAD@{20}: checkout: moving from login to main
ad3803f HEAD@{21}: commit: Login
1ae9508 HEAD@{22}: checkout: moving from main to login
1ae9508 HEAD@{23}: checkout: moving from login to main
1ae9508 HEAD@{24}: checkout: moving from main to login
1ae9508 HEAD@{25}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 (tag: clase_1) HEAD@{26}: checkout: moving from main to tags/clase_1
1ae9508 HEAD@{27}: commit: Este es mi sexto commit
ccfd892 (tag: clase_1) HEAD@{28}: reset: moving to ccfd892
4dcdad1 HEAD@{29}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 (tag: clase_1) HEAD@{30}: checkout: moving from main to ccfd892
4dcdad1 HEAD@{31}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 (tag: clase_1) HEAD@{32}: checkout: moving from main to ccfd892
4dcdad1 HEAD@{33}: reset: moving to 4dcdad1
4dcdad1 HEAD@{34}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 (tag: clase_1) HEAD@{35}: checkout: moving from main to ccfd892
4dcdad1 HEAD@{36}: reset: moving to 4dcdad1
4dcdad1 HEAD@{37}: reset: moving to 4dcdad1
4dcdad1 HEAD@{38}: checkout: moving from ccfd892b3419028433c7a6af623b5bfee6b5be2f to main
ccfd892 (tag: clase_1) HEAD@{39}: checkout: moving from 4dcdad18b3aa6872bd877acaed84b38c437d3cba to ccfd892
4dcdad1 HEAD@{40}: reset: moving to 4dcdad1
ccfd892 (tag: clase_1) HEAD@{41}: checkout: moving from main to ccfd892
4dcdad1 HEAD@{42}: reset: moving to 4dcdad1
4dcdad1 HEAD@{43}: reset: moving to 4dcdad1
ccfd892 (tag: clase_1) HEAD@{44}: commit: Se actualizan los commands de la clase
16e1af6 HEAD@{45}: commit: Se a??ade el codigo y la documentacion de la clase 00
401635f HEAD@{46}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to main
687e6e9 HEAD@{47}: checkout: moving from main to 687e6e9
401635f HEAD@{48}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to main
687e6e9 HEAD@{49}: checkout: moving from 401635f819e95a4eef91a4764de07d8211e8b352 to 687e6e9
401635f HEAD@{50}: checkout: moving from 687e6e9c4003f949789fabfee6c28b5354b61969 to 401635f
687e6e9 HEAD@{51}: commit: Se a??ade el codigo y la documentacion de la clase 00
401635f HEAD@{52}: checkout: moving from 686d47d64da297908967465292ef9128664c547c to 401635f
686d47d HEAD@{53}: checkout: moving from main to 686d47d64da297908967465292ef9128664c547c
401635f HEAD@{54}: commit: Se a??ade el .gitignore
82ee4cf HEAD@{55}: commit: Se actualiza el texto del print
4dcdad1 HEAD@{56}: commit: Este es mi segundo commit
686d47d HEAD@{57}: commit (initial): Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
*   ec3bbba (HEAD -> main) Merge branch 'login'
|\
| * 9b1cc84 Login v2
| *   df2ee81 Correccion conflicto
| |\
| * | 16c53c8 Git 3 login
| * |   43e19bb Merge branch 'main' into login
| |\ \
| * | | ad3803f Login
* | | | 5449135 Documentation Clase 01
* | | | d83f162 Commands Clase 01
| |_|/
|/| |
* | | 76e3379 Git 3 v3
| |/
|/|
* | de6a856 Git 3 v2
* | 70444f4 Se actualiza la documentacion y comandos de la clase 01
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tag clase_2

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
*   ec3bbba (HEAD -> main, tag: clase_2) Merge branch 'login'
|\
| * 9b1cc84 Login v2
| *   df2ee81 Correccion conflicto
| |\
| * | 16c53c8 Git 3 login
| * |   43e19bb Merge branch 'main' into login
| |\ \
| * | | ad3803f Login
* | | | 5449135 Documentation Clase 01
* | | | d83f162 Commands Clase 01
| |_|/
|/| |
* | | 76e3379 Git 3 v3
| |/
|/|
* | de6a856 Git 3 v2
* | 70444f4 Se actualiza la documentacion y comandos de la clase 01
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ls -al ~/.ssh
ls: cannot access '/c/Users/user/.ssh': No such file or directory

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh-keygen -t ed25519 -C "sarismejiasanchez@gmail.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/user/.ssh/id_ed25519): id_rsa
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in id_rsa
Your public key has been saved in id_rsa.pub
The key fingerprint is:
SHA256:nRV/7jZtrJ5GA2mHndTB93DGWgvL8RP6ZhYys1hPtRo sarismejiasanchez@gmail.com
The key's randomart image is:
+--[ED25519 256]--+
|            . .+.|
|             =ooO|
|            o=BBO|
|         . o=E=X.|
|        S o.oo@ +|
|           . ooO.|
|             .+o*|
|              .=.|
|             o+  |
+----[SHA256]-----+

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ eval "$(ssh-agent -s)"
Agent pid 1860

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh-add ~/.ssh/id_rsa
/c/Users/user/.ssh/id_rsa: No such file or directory

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh-add ~/.ssh/id_rsa
Identity added: /c/Users/user/.ssh/id_rsa (sarismejiasanchez@gmail.com)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ eval "$(ssh-agent -s)"
Agent pid 1876

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh-add ~/.ssh/id_rsa
Identity added: /c/Users/user/.ssh/id_rsa (sarismejiasanchez@gmail.com)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ clip < ~/.ssh/id_rsa.pub

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh -T git@github.com
The authenticity of host 'github.com (140.82.113.4)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi sarismejiasanchez! You've successfully authenticated, but GitHub does not provide shell access.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ ssh -T git@github.com
Hi sarismejiasanchez! You've successfully authenticated, but GitHub does not provide shell access.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git remote add origin https://github.com/sarismejiasanchez/hello-git.git

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git push -u origin main
Enumerating objects: 61, done.
Counting objects: 100% (61/61), done.
Delta compression using up to 4 threads
Compressing objects: 100% (49/49), done.
Writing objects: 100% (61/61), 10.60 KiB | 319.00 KiB/s, done.
Total 61 (delta 25), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (25/25), done.
To https://github.com/sarismejiasanchez/hello-git.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   00_documentation.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 6f7d919 (HEAD -> main, origin/main) Se actualiza la documentacion y comandos de la clase 01
*   ec3bbba (tag: clase_2) Merge branch 'login'
|\
| * 9b1cc84 Login v2
| *   df2ee81 Correccion conflicto
| |\
| * | 16c53c8 Git 3 login
| * |   43e19bb Merge branch 'main' into login
| |\ \
| * | | ad3803f Login
* | | | 5449135 Documentation Clase 01
* | | | d83f162 Commands Clase 01
| |_|/
|/| |
* | | 76e3379 Git 3 v3
| |/
|/|
* | de6a856 Git 3 v2
* | 70444f4 Se actualiza la documentacion y comandos de la clase 01
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00
* 401635f Se a??ade el .gitignore
* 82ee4cf Se actualiza el texto del print
* 4dcdad1 Este es mi segundo commit
* 686d47d Este es mi primer commit

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   00_documentation.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "^C

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se actualiza la documentacion y comandos de la clase 02" -m "Configuracion y sincronizacion con GitHub"
[main 0d346ba] Se actualiza la documentacion y comandos de la clase 02
 2 files changed, 72 insertions(+), 2 deletions(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.42 KiB | 364.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/sarismejiasanchez/hello-git.git
   6f7d919..0d346ba  main -> main

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_documentation.md
        modified:   hellogit.py

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add hellogit.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Hello GitHub"
[main 4222942] Hello GitHub
 1 file changed, 1 insertion(+), 1 deletion(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git push
To https://github.com/sarismejiasanchez/hello-git.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/sarismejiasanchez/hello-git.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git fetch
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 660 bytes | 5.00 KiB/s, done.
From https://github.com/sarismejiasanchez/hello-git
   61f7768..1d20721  main       -> origin/main

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git tree
* 4222942 (HEAD -> main) Hello GitHub
| * 1d20721 (origin/main) Create README.md
|/
* 61f7768 Hello GitHub
* bb4dfeb Se actualiza la documentacion y comandos de la clase 02
* 0d346ba Se actualiza la documentacion y comandos de la clase 02
* 6f7d919 Se actualiza la documentacion y comandos de la clase 01
*   ec3bbba (tag: clase_2) Merge branch 'login'
|\
| * 9b1cc84 Login v2
| *   df2ee81 Correccion conflicto
| |\
| * | 16c53c8 Git 3 login
| * |   43e19bb Merge branch 'main' into login
| |\ \
| * | | ad3803f Login
* | | | 5449135 Documentation Clase 01
* | | | d83f162 Commands Clase 01
| |_|/
|/| |
* | | 76e3379 Git 3 v3
| |/
|/|
* | de6a856 Git 3 v2
* | 70444f4 Se actualiza la documentacion y comandos de la clase 01
|/
* 1ae9508 Este es mi sexto commit
* ccfd892 (tag: clase_1) Se actualizan los commands de la clase
* 16e1af6 Se a??ade el codigo y la documentacion de la clase 00

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git pull
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   00_commands.md
        modified:   00_documentation.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git add .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git commit -m "Se actualiza la documentacion y comandos de la clase 02" -m "Configuracion y sincronizacion con GitHub"
[main 11fcf7c] Se actualiza la documentacion y comandos de la clase 02
 2 files changed, 91 insertions(+), 1 deletion(-)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git push
Enumerating objects: 17, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 1.65 KiB | 337.00 KiB/s, done.
Total 9 (delta 5), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), completed with 3 local objects.
To https://github.com/sarismejiasanchez/hello-git.git
   1d20721..11fcf7c  main -> main

user@SARISMEJIASANCHEZ MINGW64 ~ (main)
$ git clone git@github.com:sarismejiasanchez/hello-git-mouredev.git
Cloning into 'hello-git-mouredev'...
remote: Enumerating objects: 505, done.
remote: Counting objects: 100% (103/103), done.
remote: Compressing objects: 100% (54/54), done.

Receiving objects: 100% (505/505), 354.80 KiB | 1.10 MiB/s, done.
Resolving deltas: 100% (278/278), done.

user@SARISMEJIASANCHEZ MINGW64 ~ (main)
$ cd hello-git-mouredev/

user@SARISMEJIASANCHEZ MINGW64 ~/hello-git-mouredev (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.md

no changes added to commit (use "git add" and/or "git commit -a")

user@SARISMEJIASANCHEZ MINGW64 ~/hello-git-mouredev (main)
$ git add hello.md

user@SARISMEJIASANCHEZ MINGW64 ~/hello-git-mouredev (main)
$ git commit -m "A??ado mi nombre de usuario para saludar a la comunidad"
[main c81668a] A??ado mi nombre de usuario para saludar a la comunidad
 1 file changed, 1 insertion(+)

user@SARISMEJIASANCHEZ MINGW64 ~/hello-git-mouredev (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 335 bytes | 335.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:sarismejiasanchez/hello-git-mouredev.git
   89e1674..c81668a  main -> main
  
user@SARISMEJIASANCHEZ MINGW64 ~ (main)
$ cd 'Helo Git'
bash: cd: Helo Git: No such file or directory

user@SARISMEJIASANCHEZ MINGW64 ~ (main)
$ cd 'Hello Git'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git flow
usage: git flow <subcommand>

Available subcommands are:
   init      Initialize a new git repo with support for the branching model.
   feature   Manage your feature branches.
   bugfix    Manage your bugfix branches.
   release   Manage your release branches.
   hotfix    Manage your hotfix branches.
   support   Manage your support branches.
   version   Shows version information.
   config    Manage your git-flow configuration.
   log       Show log deviating from base branch.

Try 'git flow <subcommand> help' for details.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$ git flow init

Which branch should be used for bringing forth production releases?
   - main
Branch name for production releases: [main]
Branch name for "next release" development: [develop]

How to name your supporting branch prefixes?
Feature branches? [feature/]
Bugfix branches? [bugfix/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? []
Hooks and filters directory? [C:/Users/user/Hello Git/.git/hooks]

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (develop)
$ git flow start feature 2auth
usage: git flow <subcommand>

Available subcommands are:
   init      Initialize a new git repo with support for the branching model.
   feature   Manage your feature branches.
   bugfix    Manage your bugfix branches.
   release   Manage your release branches.
   hotfix    Manage your hotfix branches.
   support   Manage your support branches.
   version   Shows version information.
   config    Manage your git-flow configuration.
   log       Show log deviating from base branch.

Try 'git flow <subcommand> help' for details.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (develop)
$ git flow feature start 2auth
Switched to a new branch 'feature/2auth'

Summary of actions:
- A new branch 'feature/2auth' was created, based on 'develop'
- You are now on branch 'feature/2auth'

Now, start committing on your feature. When done, use:

     git flow feature finish 2auth


user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (feature/2auth)
$ code .

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (feature/2auth)
$ git status
On branch feature/2auth
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        auth.py

nothing added to commit but untracked files present (use "git add" to track)

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (feature/2auth)
$ git add auth.py

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (feature/2auth)
$ git flow feature finish 2auth
Switched to branch 'develop'
Updating fabcd2c..5165778
Fast-forward
 auth.py | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 auth.py
Deleted branch feature/2auth (was 5165778).

Summary of actions:
- The feature branch 'feature/2auth' was merged into 'develop'
- Feature branch 'feature/2auth' has been locally deleted
- You are now on branch 'develop'

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (develop)
$ git flow release start 1.0
Switched to a new branch 'release/1.0'

Summary of actions:
- A new branch 'release/1.0' was created, based on 'develop'
- You are now on branch 'release/1.0'

Follow-up actions:
- Bump the version number now!
- Start committing last-minute fixes in preparing your release
- When done, run:

     git flow release finish '1.0'


user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (release/1.0)
$ git flow release finish 1.0
Branches 'main' and 'origin/main' have diverged.
Fatal: And branch 'main' may be fast-forwarded.

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (release/1.0)
$

user@SARISMEJIASANCHEZ MINGW64 ~/Hello Git (main)
$