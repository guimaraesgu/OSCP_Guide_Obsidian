##### 01. System Info
```
systeminfo

## Variaveis de Ambiente
set
```


##### 02. Info Usuario e Grupo 
```
whoami /all
echo %username%
net user         --> usuarios locais
net user /domain --> usuarios de domínio
net user [usuario] --> info do usuario


## Pegar info de regras de conta de usuario (last login, idade senha)
net accounts 
net accounts /domain

## Identificar grupos Locais
net localgroup
net localgroup [grupo] --> retorna usuarios do grupo

## Adicionar Usuario
net user [usuario] [senha] /add 
net user [grupo] [usuario] /add --> Add usuario em grupo

whoami /priv
whoami /user --> retorna o SID
whoami /groups
```


##### 03. Diretorios
```
dir /s [diretorio] --> lista dir recursivo
dir /r  --> lista dir mostrando arquivos com ADS

## Acessar arquivos ADS
more < a.txt:b.txt
```


##### 04. Rede
```
ipconfig /all

arp -a

netstat -na
netstat -nao       --> Retorna coluna PID
	netstat -nao 1 --> Atualiza a cada 1 seg
netstat -naob      --> Só alto privilegio, retorna com nome do serviço
netstat -nr        --> Retorna rotas, similar a route print

route print
```