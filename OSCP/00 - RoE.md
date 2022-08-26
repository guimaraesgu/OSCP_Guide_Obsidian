### Rules of Engagement

#### During Exam
- Screenshot 
	- Windows
```
type proof.txt && whoami && hostname && ipconfig
```

	- Linux
```
cat proof.txt && whoami && hostname && ip addr
```

- Flags estão nos arquivos 
	- local.txt --> Low Privilege
	- proof.txt --> High Privilege (root, admin, system)
		- Linux --> /root
		- Windows --> Admin Desktop


#### Report
- Exploit Code
	- Se público e não alterado, somente registrar a URL onde foi encontrado
	- Se público e alterado: 
		- A URL do original
		- O código modificado
		- Marcar a alteração feita, no código
		- O comando usado para gerar o shellcode ( se aplicável )
		- Explicação do porque a alteração foi realizada
- Criar .7z dentro do Kali
	- Padrão de nome do .pdf e do .7z : OSCP-OS-XXXXX-Exam-Report
		- XXXXX é o OSID do candidato.
		- Comando
		```
		7z a OSCP-OS-XXXXXX-Exam-Report.7z OSCP-OS-XXXXXX-Exam-Report.pdf
		```



#### Prohibited Tools
- Metasploit --> Tem uma observação
	- Pode ser usado, porém somente em uma máquina. Depois de usar nela, não pode usar em outra, mesmo se a utilização não tiver sido efetiva.
	- Outro detalhe, não pode usar no AD, por ser um set de máquinas, usar em uma, estaria usando nas outras, quebrando a regra acima. 
- Vuln Scanners: Nessus, OpenVAS, NeXpose, Canvas, Core Impact, SAINT, etc... 
	- NSE pode
- Automatic Exploitation: db_autopwn, browser_autopwn, SQLMap, SQLninja, etc...
- Metasploit Pro, Burp Pro
- Spoofing de qualquer forma é proibido. 


#### Allowed Tools
- NMap e NSE
- Nikto
- Burp Free
- DirBuster
- Msfvenom
- Pattern_create.rb
- Pattern_offset.rb
- Multi handler ( aka /exploit/multi/handler )