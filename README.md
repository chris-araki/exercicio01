a) No working dir, executar o comando:\
echo 01 > arquivo.txt\
b) Adicionar o arquivo no staging e conferir o status\
git add arquivo.txt\
git status\
c) Commitar o arquivo do staging com a descrição "git add example - arquivo.txt“\
git commit -m "git add example - arquivo.txt“\
d) Sobrescrever o conteúdo do arquivo.txt:\
echo 02 > arquivo.txt\
e) Verificar o diffing no arquivo\
git diff\
f) Adicionar novamente o arquivo no staging e conferir o status\
git add arquivo.txt\
git status\
g) Verificar o diffing no arquivo\
git diff\
h) Sobrescrever o conteúdo do arquivo.txt:\
echo 03 > arquivo.txt\
i) Verificar o diffing no arquivo\
git diff\
j) Fazer o restore do arquivo da área de staging e verificar o status\
git restore --stage arquivo.txt\
git status\
k) Realizar o commit do arquivo e verificar o log\
git commit -m "git add example - arquivo.txt“\
git log\
l) Adicionar um arquivo gitignore com o seguinte conteúdo:\
*.txt\
echo "*.txt" > .gitignore\
m) Criar um arquivo novo.txt e verificar o status\
echo "" > novo.txt
