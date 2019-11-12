# auto-deploy
## Examples

Check availabile options:
```
$ python deploy.py --help
usage: deploy.py [-h] [--add_host ADD_HOST] [--add_package ADD_PACKAGE]

optional arguments:
  -h, --help            show this help message and exit
  --add_host ADD_HOST   Add new host
  --add_package ADD_PACKAGE
                        Add new package
```
Check current status of template:
```
$ cat template.json
{"hosts": ["206.189.29.37", "206.189.29.35", "192.168.1.101"], "packages": ["apache2", "sshd"]}
```

Add both new host and package for installation (this is example of both, it works separately, too):
```
python deploy.py --add_host 192.168.1.100 --add_package nginx
```
Verify the template:
```
cat template.json
{"hosts": ["206.189.29.37", "206.189.29.35", "192.168.1.101", "192.168.1.100"], "packages": ["apache2", "sshd", "nginx"]}
```
