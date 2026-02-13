`python3 -m http.server 8000` -  запуск простого HTTP-сервера на Python, которые обслуживает файлы из текущей директории через порт 8000
1) `curl -I http://localhost:8000/`- запрос к серверу через curl
2) `sudo lsof -i :8000` - проверка того, слушает ли кто то уже порт 8000 
	- выводится PID процесса, чаще всего необходимо либо убить его, чтобы заменить другим процессом, или заменить сам порт, совершаем проверку того, слушает ли порт кто-то еще до сих пор `netstat -tulpn | grep :8000`
	![[Pasted image 20260211130553.png]]
3) `curl -w "\n= ТАЙМИНГ =\n\==`
	`DNS: %{time_namelookup}s\n\==`
	`Connect: %{time_connect}s\n\==`
	`TLS/SSL: %{time_appconnect}s\n\==`
	`TTFB: %{time_starttransfer}s\n\==`
	`Total: %{time_total}s\n\==`
	`Speed: %{speed_download} B/s\n" \==`
	`-o /dev/null -s https://example.com====` - полная проверка скорости работы сайта example.com ![[Pasted image 20260211132604.png]]

4) 
