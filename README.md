# Cloud-Computing
Its a repository from Cloud Computing Course from University of Duke

* First of all, we're gonna post a [simple code](https://github.com/Guitoll/Cloud-Computing/blob/main/Cloud_computing.ipynb)
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
```
