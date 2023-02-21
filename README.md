# Cloud-Computing
Its a repository from Cloud Computing Course from University of Duke

* First of all, we're gonna post a [simple code](https://github.com/Guitoll/Cloud-Computing/blob/main/Cloud_computing.ipynb)

## Se realizará un listado con apuntes en Github

* [Create an AWS Cloud Development Environment](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#create-an-aws-cloud-development-environment)
  * [Comunicación con AWS](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#comunicaci%C3%B3n-con-aws-comunicaci%C3%B3n-encriptada-bidireccional-con-github)
  * [Creación de ambiente y archivos base](https://github.com/Guitoll/Cloud-Computing/edit/main/README.md#creaci%C3%B3n-de-ambiente-y-archivos-base)
  
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
* Por último en Github, Settings -> Keys -> Add SSH Key, copiar el texto de arriba y correr el código (en AWS):
```
git clone git@github.com:Guitoll/Repository-Name.git
cd Repository-Name/
```
## Creación de ambiente y archivos base
En primer lugar, se crea un ambiente virtual donde se trabajará:
```
python3 -m venv ~/.Repository-Name
source ~/.Repository-Name/bin/activate
```

Se crean los siguientes archivos:
* [Makefile](https://github.com/Guitoll/Cloud-Computing/blob/main/Makefile): Template con instrucciones para instalar, testear, depurar y formatear el código.
   * install: se puede instalar librerias de requirements.text necesarias corriendo `make install, make format, make lint, make test` 
* [Programa_python.py](https://github.com/Guitoll/Cloud-Computing/blob/main/hello.py): Programa de python
* [test_programa.py](https://github.com/Guitoll/Cloud-Computing/blob/main/test_hello.py): Programa que testea el programa principal
* [requirements.txt](https://github.com/Guitoll/Cloud-Computing/blob/main/requirements.txt): Archivo de texto que contiene las librerias importantes
```
touch Makefile
touch Programa_python.py
touch test_programa.py
touch requirements.txt
```
