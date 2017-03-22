## Exportar historial de Google Chrome en MacOs

### En la terminal escribir:

`cd /Library/Application Support/Google/Chrome/Default`

### Realizar una copia del archivo History en el mismo directorio [1] (21/mar/17)

`cp History History2`

### Exportar historial a archive.txt [2] (21/mar/17)

`sqlite3 History2 "select datetime(last_visit_time/1000000-11644473600,'unixepoch','localtime'),url from  urls order by last_visit_time desc" > ~/history_export.txt`

### Abrir Excel e importar archive history_export, seleccionar | como comodín para separar celdas.

[1]: http://www.computerhope.com/unix/ucp.htm 
[2]: https://superuser.com/questions/602252/can-chrome-browser-history-be-exported-to-an-html-file

