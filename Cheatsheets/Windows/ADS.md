##### Criar ADS
```
type \windows\System32\calc.exe > a.txt:calc.exe
```

##### Listar ADS
```
dir /r
```

##### Criar ADS Oculto
Para criar um ADS que o "dir" não lista, é necessário criar um arquivo principal com nome reservado (COM1..2..3, CON, PRN, AUX, LPT1..2..3..4, naturalmente proibido pelo Windows.
Obrigatório usar caminho completo
```
echo AAAAAA > \\?\c:\teste\COM1.txt
echo CCCCCC > \\?\c:\teste\COM1.txt:c.txt
```

##### Ler ADS
Somente algumas ferramentas são capazes de ler fluxos alternativos
```
more < a.txt:b.txt


## Ocultos
more < \\?\c:\teste\COM1.txt:c.txt
sort \\?\c:\teste\COM1.txt:c.txt
```

##### Executar dentro do ADS
```
wmic process call create [caminho completo do arquivo/a.txt:calc.exe]
```