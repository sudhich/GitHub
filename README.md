# GitHub
### ** git commond **  
foder_name=GitTutorial    
file=Image.bmp,Document.txt  
(1)git status(abhi meri gimedari nahi hai)   
"""$ git status  
   fatal: not a git repository (or any of the parent directories): .git    
"""      
(2)git init(ab meri jimedari ho gayi hai)  {$rm -rf .git} --> [**this commond delete the git repo**](ab meri koi jimedari nahi hai) $ git status fatal: not a git     (out_this )|                             (out_put)|---->                                                      repository (or any of the parent directories): .git
   """$ git init   
         Initialized empty Git repository in D:/GitTutorial/.git/  
   """     
**After making some file and folder in GitTutorial(folder_name) then run this commond.**  
                     $ git status  
                     On branch master  

                     No commits yet  

                     Untracked files:  
                     (use "git add <file>..." to include in what will be committed)  
                          New Bitmap Image.bmp(show red)  
                          New Text Document.txt(show red)  

                     nothing added to commit but untracked files present (use "git add" to track)  
(3)git add --a /{git add .} (it go to staging area all files, but if you want to only one particular file go to staging area then run this $git add "<file_name_with_extention>")  
(4)git status  
                     $ git status 
                     On branch master

                     No commits yet

                     Changes to be committed:
                       (use "git rm --cached <file>..." to unstage)
                             new file:   New Bitmap Image.bmp(show green)
                             new file:   New Text Document.txt(show green) 

(5)$ git commit -m "1st commit"  
Author identity unknown  
  
*** Please tell me who you are.  
  
Run  
  
  git config --global user.email "you@example.com"  
  git config --global user.name "Your Name"  
  
to set your account's default identity.  
Omit --global to set the identity only in this repository.  
  
fatal: unable to auto-detect email address (got 'sudhir@DESKTOP-D9KEELJ.(none)')  

(5)git config --global user.email "you@example.com"    
  git config --global user.name "Your Name"  
  **After that run this**
$ git commit -m "1st commit"  
[master (root-commit) 1590871] 1st commit  
 2 files changed, 0 insertions(+), 0 deletions(-)  
 create mode 100644 New Bitmap Image.bmp 
 create mode 100644 New Text Document.txt  
 **And then run this**    
 $ git status
On branch master
nothing to commit, working tree clean
**And then**  
$ git log  
commit 15908717e0113c6f76c7978a3fb29a7a9ad1fc47 (HEAD -> master)  
Author: Sudhir <sudhir1208@gmail.com>  
Date:   Mon Apr 17 11:41:22 2023 +0530  
  
    1st commit  

(6)**Here modified two file but we want to save only (New Text Document.txt) into main directory**  
$ git status   
On branch master  
Changes not staged for commit:  
  (use "git add <file>..." to update what will be committed)  
  (use "git restore <file>..." to discard changes in working directory)  
        modified:   New Rich Text Document.rtf   
        modified:   New Text Document.txt  

**So we do this step aftre checking.**  
$ git add "New Text Document.txt"  
**Then**   
$ git add "New Text Document.txt"    {go to staging area only this file "New Text Document.txt" but if you want all the file go to staging area then $git add --a}  
$ git commit -m " go to commit New Text Document.txt"  
[master 3de3f5e]  go to commit New Text Document.txt  
 1 file changed, 1 insertion(+), 1 deletion(-)  
 **So show this only**  
 $ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   New Rich Text Document.rtf  

no changes added to commit (use "git add" and/or "git commit -a")
(7) $git clone link  
   *Ex--*
   $git clone https://github.com/tensorflow/tensorflow.git
   *But if you want to your own name then*
   $git clone https://github.com/tensorflow/tensorflow.git MyOwnName
   
                                                $ git status
                                             On branch master

                                             No commits yet

                                             Changes to be committed:
                                               (use "git rm --cached <file>..." to unstage)
                                                     new file:   .gitignore
                                                     new file:   New Bitmap Image.bmp
                                                     new file:   New Rich Text Document.rtf
                                                     new file:   rename.txt
                                                     new file:   static/tex.txt

                                             Changes not staged for commit:
                                               (use "git add <file>..." to update what will be committed)
                                               (use "git restore <file>..." to discard changes in working directory)
                                                     modified:   rename.txt


   
                                                $ git add rename.txt

                                             sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)
                                             $ git status
                                             On branch master

                                             No commits yet

                                             Changes to be committed:
                                               (use "git rm --cached <file>..." to unstage)
                                                     new file:   .gitignore
                                                     new file:   New Bitmap Image.bmp
                                                     new file:   New Rich Text Document.rtf
                                                     new file:   rename.txt
                                                     new file:   static/tex.txt

   
   
   
   
   
   
   
   
   
   
   
(8).gitignore me file_name or dir/(inner){/dir/(outer)} mention karege to wosko ignore kar dega.  
(9)$ git status
On branch master
nothing to commit, working tree clean
### BY touch commond we create text file.   
(10)$ touch name_err.log (after running this command name_err file will get created whose name is name_err.log)   
(11)$ git status  
On branch master     
Untracked files:   
  (use "git add <file>..." to include in what will be committed)  
        name_err.log  
  
nothing added to commit but untracked files present (use "git add" to track)  
(12)$ touch .gitignore    
(13)$ git status    
On branch master  
Untracked files:  
  (use "git add <file>..." to include in what will be committed)   
        .gitignore   
        name_err.log  
   
nothing added to commit but untracked files present (use "git add" to track)   
  
  **Here name_err.log file name write into the .gitignore then run this below commond then only one file remain untrack means name_err.log ignore them and similarly if you want to ignore any directory then write directory name into the .gitignore.**  
    
  $ git status  
On branch master   
Untracked files:  
  (use "git add <file>..." to include in what will be committed)  
        .gitignore  
  
nothing added to commit but untracked files present (use "git add" to track)  
(14)$ git add .  /{git add --a}   
(15)$ git status    
On branch master  
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  
        new file:   .gitignore     
(16)$ git commit -m "gitignoire file exp"  
[master 878bd19] gitignoire file exp  
 1 file changed, 1 insertion(+)  
 create mode 100644 .gitignore  
 (17)$ git status  
On branch master  
nothing to commit, working tree clean  
 **After creating static folder and putting them into staging area**  
(18)$ git status    
On branch master  
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  
        modified:   .gitignore  
        new file:   static/tex.txt  
(19)$ git status  
On branch master   
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  
        modified:   .gitignore  
        new file:   static/tex.txt  

Changes not staged for commit:  
  (use "git add <file>..." to update what will be committed)  
  (use "git restore <file>..." to discard changes in working directory)  
        modified:   static/tex.txt  
 (20)$ git diff  
diff --git a/static/tex.txt b/static/tex.txt  
index 85df507..165afc9 100644  
--- a/static/tex.txt   
+++ b/static/tex.txt  
@@ -1 +1 @@  
-abcd  
\ No newline at end of file  
+Sudhir Bhai  
\ No newline at end of file  
(21)$ git add .  
(22)$ git diff  
(23)$ git status  
On branch master  
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  
        modified:   .gitignore  
        new file:   static/tex.txt  
(24)$ git diff --staged  (**Here if we are already in staging area then how will compare previous task then run this commond git diff --staged)
diff --git a/.gitignore b/.gitignore  
index cacc0f6..43b195e 100644  
--- a/.gitignore  
+++ b/.gitignore  
@@ -1,3 +1,3 @@  
 name_err.log  
-*.log  
+*.log  --> means all_file.git  
  
diff --git a/static/tex.txt b/static/tex.txt  
new file mode 100644  
index 0000000..165afc9  
--- /dev/null  
+++ b/static/tex.txt  
@@ -0,0 +1 @@ 
+Sudhir Bhai  
\ No newline at end of file  
 **If we want to direct commit without bring to staging area then run this commond**  
(25)$ git status  
On branch master  
Changes not staged for commit:  
  (use "git add <file>..." to update what will be committed)  
  (use "git restore <file>..." to discard changes in working directory)  
        modified:   New Text Document.txt  
   
Untracked files:  
  (use "git add <file>..." to include in what will be committed)   
        second.txt     
  
no changes added to commit (use "git add" and/or "git commit -a")   
**look this**  
$ git commit -a -m "Direct Commit"  
[master 1289f2e] Direct Commit   
 1 file changed, 2 insertions(+), 1 deletion(-)   
**look also**  
$ git status  
On branch master  
Untracked files:  
  (use "git add <file>..." to include in what will be committed) 
        second.txt   

nothing added to commit but untracked files present (use "git add" to track)  

*It means untracked file direct commit me nahi jayegi only tracked file jayegi.*  
   
   
**If we want to delete file using git commond then use this commond**   
(26)$ git status  
On branch master  
nothing to commit, working tree clean  
  
sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)  
$ git rm second.txt  
rm 'second.txt'  
   
sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)  
$ git status    
On branch master     
Changes to be committed:     
  (use "git restore --staged <file>..." to unstage)       
        deleted:    second.txt    
sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)   
$ git commit -m "remove second.txt file"  
[master 297450c] remove second.txt file  
 1 file changed, 0 insertions(+), 0 deletions(-)    
 delete mode 100644 second.txt  

sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)  
$ git status  
On branch master  
nothing to commit, working tree clean   

(27)**If you want to rename your file name then do this**  
$ git status  
On branch master  
nothing to commit, working tree clean  
$ git mv New_Text_Document.txt rename.txt  
$ git status  
On branch master  
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  
        renamed:    New_Text_Document.txt -> rename.txt  
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    New_Text_Document.txt -> rename.txt


sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)  
$ git commit -m "rename the file name"  
[master 126ef8a] rename the file name   
 1 file changed, 0 insertions(+), 0 deletions(-)  
 rename New_Text_Document.txt => rename.txt (100%)  
  
sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)  
$ git status  
On branch master  
nothing to commit, working tree clean  
(28) **Show all changes**
$ git log -p
commit 126ef8a2a9eccb071317e626cf382e2b41e112f4 (HEAD -> master)
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:58:17 2023 +0530

    rename the file name

diff --git a/New_Text_Document.txt b/rename.txt
similarity index 100%
rename from New_Text_Document.txt
rename to rename.txt

commit 38230a0251a156527418f2e4d1e8a0a47d0a7372
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:55:45 2023 +0530

    remove second.txt file

diff --git a/New Text Document.txt b/New_Text_Document.txt
similarity index 100%
rename from New Text Document.txt
rename to New_Text_Document.txt

commit 297450c82afc1affd29dd4d019719272ff3bc1a3
:...skipping...
commit 126ef8a2a9eccb071317e626cf382e2b41e112f4 (HEAD -> master)
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:58:17 2023 +0530

    rename the file name

diff --git a/New_Text_Document.txt b/rename.txt
similarity index 100%
rename from New_Text_Document.txt
rename to rename.txt

commit 38230a0251a156527418f2e4d1e8a0a47d0a7372
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:55:45 2023 +0530

    remove second.txt file

diff --git a/New Text Document.txt b/New_Text_Document.txt
similarity index 100%
rename from New Text Document.txt
rename to New_Text_Document.txt

commit 297450c82afc1affd29dd4d019719272ff3bc1a3
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:48:40 2023 +0530

    remove second.txt file

diff --git a/second.txt b/second.txt
deleted file mode 100644
index e69de29..0000000

commit a69e33b2ee7c5755e6809c9432e0c358cf99dd78
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:36:10 2023 +0530

    Direct Commit 2

diff --git a/second.txt b/second.txt
new file mode 100644
index 0000000..e69de29

commit 1289f2e3446d168285c06ede5d77b0572d702d4e
Author: Sudhir <sudhir1208@gmail.com>
Date:   Sat Apr 22 17:31:26 2023 +0530

    Direct Commit

:
### If you want previous written data(by mistake edited) from a file run this commond.
(29)

                           $ git status
                           On branch master
                           Changes not staged for commit:
                             (use "git add <file>..." to update what will be committed)
                             (use "git restore <file>..." to discard changes in working directory)
                                   modified:   rename.txt

                           no changes added to commit (use "git add" and/or "git commit -a")

                           sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)
                           $ git restore rename.txt

                           sudhir@DESKTOP-D9KEELJ MINGW64 /d/GitTutorial (master)
                           $ git status
                           On branch master
                           nothing to commit, working tree clean

        

## For previous commit then run this commond.
         $ git checkout -f
     
     
git remote add origin [copied web address]    
git push -u origin main  
