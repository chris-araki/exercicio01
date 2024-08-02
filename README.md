a) No working dir, executar o comando:\
echo 01 > arquivo.txt\
b) Adicionar o arquivo no staging e conferir o status\
B - git add arquivo.txt\
B - git status\
On branch main\
Changes to be committed:\
  (use "git restore --staged <file>..." to unstage)\
        modified:   arquivo.txt\
c) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt“\
C - git commit -m "git add example - arquivo.txt“\
[main e9b0109] git add example - arquivo.txt\
 1 file changed, 1 insertion(+), 1 deletion(-)\
d) Sobrescrever o conteúdo do arquivo.txt:\
echo 02 > arquivo.txt\
e) Verificar o diffing no arquivo\
E - git diff\
diff --git a/arquivo.txt b/arquivo.txt\
index 8a0f05e..9e22bcb 100644\
--- a/arquivo.txt\
+++ b/arquivo.txt\
@@ -1 +1 @@\
-01\
+02\
f) Adicionar novamente o arquivo no staging e conferir o status\
F - git add arquivo.txt\
F - git status\
On branch main\
Changes to be committed:\
  (use "git restore --staged <file>..." to unstage)\
        modified:   arquivo.txt\
g) Verificar o diffing no arquivo\
G - git diff\
diff --git a/arquivo.txt b/arquivo.txt\
index 8a0f05e..9e22bcb 100644\
--- a/arquivo.txt\
+++ b/arquivo.txt\
@@ -1 +1 @@\
-01\
+02\
h) Sobrescrever o conteúdo do arquivo.txt:\
echo 03 > arquivo.txt\
i) Verificar o diffing no arquivo\
I - git diff\
diff --git a/arquivo.txt b/arquivo.txt\
index 8a0f05e..75016ea 100644\
--- a/arquivo.txt\
+++ b/arquivo.txt\
@@ -1 +1 @@\
-01\
+03\
j) Fazer o restore do arquivo da área de staging e verificar o status\
J - git restore --stage arquivo.txt\
J - git status\
On branch main\
Changes not staged for commit:\
  (use "git add <file>..." to update what will be committed)\
  (use "git restore <file>..." to discard changes in working directory)\
        modified:   arquivo.txt\
\
no changes added to commit (use "git add" and/or "git commit -a")\
k) Realizar o commit do arquivo e verificar o log\
K - git add arquivo.txt\
K - git commit -m "git add example - arquivo.txt“\
[main 19d8030] git add example - arquivo.txt\
 1 file changed, 1 insertion(+), 1 deletion(-)\
K - git log\
commit 19d8030c550fa6bd258a7c39cdf4aeba337ee7dc (HEAD -> main)\
Author: chris-araki <41179179+chris-araki@users.noreply.github.com>\
Date:   Fri Aug 2 01:20:43 2024 +0000\
\
    git add example - arquivo.txt\
\
commit e9b0109893eb099f966b7389ff59136e1e3ddbac\
Author: chris-araki <41179179+chris-araki@users.noreply.github.com>\
Date:   Fri Aug 2 01:16:24 2024 +0000\
\
    git add example - arquivo.txt\
[main 19d8030] git add example - arquivo.txt\
 1 file changed, 1 insertion(+), 1 deletion(-)\
l) Adicionar um arquivo gitignore com o seguinte conteúdo:\
*.txt\
L - echo "*.txt" > .gitignore\
m) Criar um arquivo novo.txt e verificar o status\
M - echo "" > novo.txt
