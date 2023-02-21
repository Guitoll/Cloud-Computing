# Cloud-Computing
Its a repository from Cloud Computing Course from University of Duke

* First of all, we're gonna post a [simple code](https://github.com/Guitoll/Cloud-Computing/blob/main/Cloud_computing.ipynb)
* [Create an AWS Cloud Development Environment](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#create-an-aws-cloud-development-environment)
  * [Comunicación con AWS (Comunicación encriptada bidireccional con Github)](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#comunicaci%C3%B3n-con-aws-comunicaci%C3%B3n-encriptada-bidireccional-con-github)
  * [Creación ambiente y archivos de seteo del ambiente en la nube](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#creaci%C3%B3n-ambiente-y-archivos-de-seteo-del-ambiente-en-la-nube)


# Create an AWS Cloud Development Environment
## Comunicación con AWS (Comunicación encriptada bidireccional con Github)
* En primer lugar, en AWS Cloud9 se debe genear la comunicación con SSH Keys
```
ssh-keygen -t rsa
```
* Luego, se obtiene la SSH Key de la siguiente manera (key de ejemplo, no operativo):

```
>>> Your public key has been saved in path/path.pub

>>> cat path/path.pub

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAABABAQCjWenfxmbeo//f75be6l+F5OaQoXaSdvHGpxHVR4R9kShiNIZUwlIQE2+MjcBBn0uIAHjcfnGAs5wXa5d/
UJIvXbXjl0jyYMIRFQvmlhzvpUVw0rqLXulbH+cLYE8/e6LA39UowsE//vYxujC7ZdDI7eK8mKVGa9gJLMO5xCKwiyjrnuq5FVRAv4poQPhgy8vqZ5c9CKjX
Wu/GuIH2S9dGVyVa14wL0lvsOxHJnCxee4HplYCSlamOo+QGKGVW8MYQXSGdMrotYpU1zg+8he0hVGVPg7T+P7/4+vwrF6jtE+rBUDWmHIpa5DOOR2NelMaWm
cxhRj2lUHldIajhGGDXsjpn ec2-user@ip-172-31-70-177.ec2.internal

```
* Luego en Github, ir a Settings -> Keys -> [Add SSH Key](https://github.com/settings/keys), copiar el texto de arriba y correr el código (en AWS):
```
git clone git@github.com:Guitoll/Repository-Name.git
```
* Finalmente, en AWS, cambiar el directorio con:

```
cd Repository-Name
```

## Creación ambiente y archivos de seteo del ambiente en la nube
* Se generan los siguientes archivos con touch:
  * Makefile
  * Programa_python.py
  * test_Programa.py
  * requirements.txt

```
ec2-user:~/environment/Cloud-Computing (main) $ touch Makefile
ec2-user:~/environment/Cloud-Computing (main) $ touch hello.py
ec2-user:~/environment/Cloud-Computing (main) $ touch test_hello.py
ec2-user:~/environment/Cloud-Computing (main) $ touch requirements
ec2-user:~/environment/Cloud-Computing (main) $ touch requirements.txt
```

* Se crea el ambiente y se accede:


```
ec2-user:~/environment/Cloud-Computing (main) $ python3 -m venv ~/.Cloud-Computing
ec2-user:~/environment/Cloud-Computing (main) $ source ~/.Cloud-Computing/bin/activate

```
