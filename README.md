# InstalacionDocker
Instalación de *Docker* siguienda la guia de [docker docs](https://docs.docker.com/engine/install/ubuntu/)

# 1 Verificar que no haya ninguna version anterior
```
fran@Fran:~$ sudo apt-get remove docker docker-engine docker.io containerd runc
Leyendo lista de paquetes... Hecho
Creando árbol de dependencias       
Leyendo la información de estado... Hecho
E: No se ha podido localizar el paquete docker-engine
```

# 2 Preparar el repositorio
```
$  sudo apt-get update
...
$  sudo apt-get install \
>     ca-certificates \
>     curl \
>     gnupg \
>     lsb-release
...
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
...
$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

```

# 3 Instalación última version de Docker
```
$ sudo apt-get update
...
$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

# 4 Probar Docker
```
$  sudo docker run hello-world
```

![image](https://user-images.githubusercontent.com/91600940/167697224-9f2afc12-f9b6-4bab-b9d8-3b4558001361.png)
