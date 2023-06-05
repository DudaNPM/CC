Uma vez que todos os nós da topologia CORE usam na realidade o mesmo filesystem,
o primeiro passo é criar uma pasta para cada nó de teste na diretoria /home/core,
como por exemplo Servidor1, Orca, Grilo.

Abrindo a linha de comandos na diretoria da pasta do nó que servirá de servidor executar os comandos
"wget http://marco.uminho.pt/disciplinas/CC-LEI/tp2-folder1.zip"
"wget http://marco.uminho.pt/disciplinas/CC-LEI/tp2-folder2.zip"
"wget http://marco.uminho.pt/disciplinas/CC-LEI/tp2-folder3.zip"
para obter as pastas de teste.

De seguida copiar o executável Server.jar para o nó que servirá de servidor (por exemplo Servidor1) e
o executável FFSync.jar para os restantes nós.

Na topologia Core abrir uma bash no nó que servirá de servidor (por exemplo Servidor1) e ir para
a sua diretoria (cd /home/core/Servidor1/). Usar o comando "java -jar Server.jar" para correr o programa.

Repare que pode ser necessário instalar o openjdk para executar os ficheiros .jar através do comando "sudo apt install openjdk-17-jre". 

Repetir o processo para os nós que desejam sincronizar as pastas e depois de se encontrar na diretoria
do mesmo usar o comando "java -jar FFSync.jar pasta ip" em que "pasta" é o nome da pasta a sincronizar e
"ip" é o endereço ip do parceiro com quem se sincronizar.

Nota: apenas pastas com o mesmo nome podem ser sincronizadas.