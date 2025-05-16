root@Debian:~# sudo apt update && sudo apt upgrade -y
Atteint :1 http://deb.debian.org/debian bookworm InRelease
Atteint :2 http://deb.debian.org/debian bookworm-updates InRelease             
Atteint :3 http://repo.mysql.com/apt/debian bookworm InRelease                 
Atteint :4 http://security.debian.org/debian-security bookworm-security InRelease
Atteint :5 https://download.docker.com/linux/debian bookworm InRelease         
Atteint :6 https://apt.releases.hashicorp.com bookworm InRelease               
Atteint :7 https://prod-cdn.packages.k8s.io/repositories/isv:/kubernetes:/core:/stable:/v1.30/deb  InRelease
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
1 paquet peut être mis à jour. Exécutez « apt list --upgradable » pour le voir.
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
Calcul de la mise à jour... Fait
Les paquets suivants ont été installés automatiquement et ne sont plus nécessaires :
  libdaxctl1 libdbus-glib-1-2 libndctl6 libpmem1 linux-image-6.1.0-25-amd64
Veuillez utiliser « sudo apt autoremove » pour les supprimer.
Les paquets suivants seront mis à jour :
  mysql-common
1 mis à jour, 0 nouvellement installés, 0 à enlever et 0 non mis à jour.
Il est nécessaire de prendre 72,4 ko dans les archives.
Après cette opération, 59,4 ko d'espace disque supplémentaires seront utilisés.
Réception de :1 http://repo.mysql.com/apt/debian bookworm/mysql-cluster-8.0 amd64 mysql-common amd64 8.0.42-1debian12 [72,4 kB]
72,4 ko réceptionnés en 0s (199 ko/s)   
apt-listchanges : Lecture des fichiers de modifications (« changelog »)...
(Lecture de la base de données... 186013 fichiers et répertoires déjà installés.
)
Préparation du dépaquetage de .../mysql-common_8.0.42-1debian12_amd64.deb ...
Dépaquetage de mysql-common (8.0.42-1debian12) sur (5.8+1.1.0) ...
Paramétrage de mysql-common (8.0.42-1debian12) ...
Installation de la nouvelle version du fichier de configuration /etc/mysql/conf.
d/mysql.cnf ...
Installation de la nouvelle version du fichier de configuration /etc/mysql/my.cn
f.fallback ...
Traitement des actions différées (« triggers ») pour mariadb-server (1:10.11.11-
0+deb12u1) ...
root@Debian:~# 

root@Debian:~# sudo apt install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo tee /etc/apt/keyrings/docker.gpg > /dev/null
echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
ca-certificates est déjà la version la plus récente (20230311).
curl est déjà la version la plus récente (7.88.1-10+deb12u12).
gnupg est déjà la version la plus récente (2.2.40-1.1).
gnupg passé en « installé manuellement ».
Les paquets suivants ont été installés automatiquement et ne sont plus nécessaires :
  libdaxctl1 libdbus-glib-1-2 libndctl6 libpmem1 linux-image-6.1.0-25-amd64
Veuillez utiliser « sudo apt autoremove » pour les supprimer.
0 mis à jour, 0 nouvellement installés, 0 à enlever et 0 non mis à jour.
root@Debian:~# ^C
root@Debian:~# 

root@Debian:~# sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io
Atteint :1 http://deb.debian.org/debian bookworm InRelease
Atteint :2 http://repo.mysql.com/apt/debian bookworm InRelease
Atteint :3 http://deb.debian.org/debian bookworm-updates InRelease             
Atteint :4 http://security.debian.org/debian-security bookworm-security InRelease
Atteint :5 https://download.docker.com/linux/debian bookworm InRelease         
Atteint :6 https://apt.releases.hashicorp.com bookworm InRelease               
Atteint :7 https://prod-cdn.packages.k8s.io/repositories/isv:/kubernetes:/core:/stable:/v1.30/deb  InRelease
Err :5 https://download.docker.com/linux/debian bookworm InRelease
  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
Tous les paquets sont à jour.
W: Une erreur s'est produite lors du contrôle de la signature. Le dépôt n'est pas mis à jour et les fichiers d'index précédents seront utilisés. Erreur de GPG : https://download.docker.com/linux/debian bookworm InRelease : Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Impossible de récupérer https://download.docker.com/linux/debian/dists/bookworm/InRelease  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Le téléchargement de quelques fichiers d'index a échoué, ils ont été ignorés, ou les anciens ont été utilisés à la place.
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
docker-ce est déjà la version la plus récente (5:28.1.1-1~debian.12~bookworm).
docker-ce-cli est déjà la version la plus récente (5:28.1.1-1~debian.12~bookworm).
containerd.io est déjà la version la plus récente (1.7.27-1).
Les paquets suivants ont été installés automatiquement et ne sont plus nécessaires :
  libdaxctl1 libdbus-glib-1-2 libndctl6 libpmem1 linux-image-6.1.0-25-amd64
Veuillez utiliser « sudo apt autoremove » pour les supprimer.
0 mis à jour, 0 nouvellement installés, 0 à enlever et 0 non mis à jour.
root@Debian:~# 

root@Debian:~# sudo systemctl start docker
sudo systemctl enable docker
sudo docker run hello-world
Synchronizing state of docker.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable docker

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

root@Debian:~# 

root@Debian:~# curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.30/deb/Release.key | sudo gpg --dearmor -o /usr/share/keyrings/kubernetes-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /" | sudo tee /etc/apt/sources.list.d/kubernetes.list
Le fichier « /usr/share/keyrings/kubernetes-archive-keyring.gpg » existe. Faut-il réécrire par-dessus ? (o/N) o
deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /
root@Debian:~# 

root@Debian:~# sudo apt update
sudo apt install -y kubelet kubeadm kubectl
Atteint :1 http://security.debian.org/debian-security bookworm-security InRelease
Atteint :2 http://deb.debian.org/debian bookworm InRelease                     
Atteint :3 http://deb.debian.org/debian bookworm-updates InRelease             
Atteint :4 http://repo.mysql.com/apt/debian bookworm InRelease                 
Atteint :5 https://apt.releases.hashicorp.com bookworm InRelease               
Atteint :6 https://download.docker.com/linux/debian bookworm InRelease         
Atteint :7 https://prod-cdn.packages.k8s.io/repositories/isv:/kubernetes:/core:/stable:/v1.30/deb  InRelease
Err :6 https://download.docker.com/linux/debian bookworm InRelease
  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
Tous les paquets sont à jour.
W: Une erreur s'est produite lors du contrôle de la signature. Le dépôt n'est pas mis à jour et les fichiers d'index précédents seront utilisés. Erreur de GPG : https://download.docker.com/linux/debian bookworm InRelease : Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Impossible de récupérer https://download.docker.com/linux/debian/dists/bookworm/InRelease  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Le téléchargement de quelques fichiers d'index a échoué, ils ont été ignorés, ou les anciens ont été utilisés à la place.
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
kubelet est déjà la version la plus récente (1.30.12-1.1).
kubeadm est déjà la version la plus récente (1.30.12-1.1).
kubectl est déjà la version la plus récente (1.30.12-1.1).
Les paquets suivants ont été installés automatiquement et ne sont plus nécessaires :
  libdaxctl1 libdbus-glib-1-2 libndctl6 libpmem1 linux-image-6.1.0-25-amd64
Veuillez utiliser « sudo apt autoremove » pour les supprimer.
0 mis à jour, 0 nouvellement installés, 0 à enlever et 0 non mis à jour.
root@Debian:~# 

root@Debian:~# sudo systemctl enable --now kubelet
root@Debian:~# 

root@Debian:~# kubectl version --client
Client Version: v1.33.0
Kustomize Version: v5.6.0
root@Debian:~# 

root@Debian:~# ls -l Dockerfile
-rw-r--r-- 1 root root 189 15 mai   17:56 Dockerfile
root@Debian:~# 

root@Debian:~# docker build -t ic-webapp:1.0 .
docker run --name test-ic-webapp -p 8080:8080 ic-webapp:1.0
[+] Building 35.3s (10/10) FINISHED                              docker:default
 => [internal] load build definition from Dockerfile                       0.1s
 => => transferring dockerfile: 228B                                       0.0s
 => [internal] load metadata for docker.io/library/python:3.6-alpine       2.0s
 => [auth] library/python:pull token for registry-1.docker.io              0.0s
 => [internal] load .dockerignore                                          0.0s
 => => transferring context: 2B                                            0.0s
 => [1/4] FROM docker.io/library/python:3.6-alpine@sha256:579978dec460264  0.0s
 => [internal] load build context                                          2.9s
 => => transferring context: 841.00kB                                      2.6s
 => CACHED [2/4] WORKDIR /opt                                              0.0s
 => [3/4] COPY . .                                                        10.5s
 => [4/4] RUN pip install flask                                           14.2s
 => exporting to image                                                     5.5s 
 => => exporting layers                                                    5.4s 
 => => writing image sha256:f0e3fe429fd3d2dc94922f32f5f6df79a99c48aab11a3  0.0s 
 => => naming to docker.io/library/ic-webapp:1.0                           0.0s 
docker: Error response from daemon: Conflict. The container name "/test-ic-webapp" is already in use by container "c8d4df12e6a9cf6271d74be2156621c3899b52d7035941495b3ebfcc461f3417". You have to remove (or rename) that container to be able to reuse that name.

Run 'docker run --help' for more information
root@Debian:~# 
root@Debian:~# docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED        STATUS                      PORTS                                         NAMES
be738c8a65b5   hello-world    "/hello"                 16 hours ago   Exited (0) 16 hours ago                                                   happy_almeida
c8d4df12e6a9   b89ff653e536   "python app.py"          2 days ago     Exited (137) 2 days ago                                                   test-ic-webapp
6d6a1aeb2ebe   registry       "/entrypoint.sh /etc…"   6 months ago   Exited (255) 6 months ago   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp   REGISTRYLOCAL
ccdac7e25ce6   centos         "bash"                   6 months ago   Exited (0) 6 months ago                                                   centos3
411f6f64df62   centos         "bash"                   6 months ago   Created                                                                   centos2
f09fc55268cb   centos         "bash"                   6 months ago   Exited (1) 6 months ago                                                   centos1
de8611afdc3b   centos         "bash"                   6 months ago   Exited (0) 6 months ago                                                   testdata
ae7e5aaa3c71   busybox        "true"                   6 months ago   Exited (0) 6 months ago                                                   donnees 
 
root@Debian:~# docker tag ic-webapp:1.0 <Ebankoli-Ulrick>/ic-webapp:1.0
docker push <username>/ic-webapp:1.0
-bash: Ebankoli-Ulrick: Aucun fichier ou dossier de ce type
-bash: username: Aucun fichier ou dossier de ce type
root@Debian:~# docker tag ic-webapp:1.0 Ebankoli-Ulrick/ic-webapp:1.0
root@Debian:~# 

root@Debian:~# docker tag ic-webapp:1.0 Ebankoli-Ulrick/ic-webapp:1.0
docker push Ebankoli-ulrick/ic-webapp:1.0
The push refers to repository [Ebankoli-ulrick/ic-webapp]
An image does not exist locally with the tag: Ebankoli-ulrick/ic-webapp
 
root@Debian:~# 
root@Debian:~# docker tag ic-webapp:1.0 Ebankoli-Ulrick/ic-webapp:1.0
docker push Dockerfile/ic-webapp:1.0
The push refers to repository [Dockerfile/ic-webapp]
An image does not exist locally with the tag: Dockerfile/ic-webapp

root@Debian:~# 
root@Debian:~# docker images
REPOSITORY                    TAG       IMAGE ID       CREATED         SIZE
Ebankoli-Ulrick/ic-webapp     1.0       f0e3fe429fd3   9 minutes ago   293MB
ic-webapp                     1.0       f0e3fe429fd3   9 minutes ago   293MB
ebankoli/ic-webapp            1.0       b89ff653e536   2 days ago      53.6MB
yourdockerhub/ic-webapp       1.0       b89ff653e536   2 days ago      53.6MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   4 months ago    1.31GB
debian                        latest    617f2e89852e   7 months ago    117MB
nginx                         latest    3b25b682ea82   7 months ago    192MB
busybox                       latest    27a71e19c956   7 months ago    4.27MB
alpine                        latest    91ef0af61f39   8 months ago    7.8MB
registry                      latest    75ef5b734af4   19 months ago   25.4MB
hello-world                   latest    d2c94e258dcb   2 years ago     13.3kB
centos                        latest    5d0da3dc9764   3 years ago     231MB
root@Debian:~# docker push ebankoli-ulrick/ic-webapp:1.0
The push refers to repository [docker.io/ebankoli-ulrick/ic-webapp]
An image does not exist locally with the tag: ebankoli-ulrick/ic-webapp
root@Debian:~# docker push ebankoli/ic-webapp:1.0
The push refers to repository [docker.io/ebankoli/ic-webapp]
94cf8d2cca1f: Layer already exists 
dcc132f21c86: Layer already exists 
5f70bf18a086: Layer already exists 
3156423bd38f: Layer already exists 
efa76becf38b: Layer already exists 
671e3248113c: Layer already exists 
1965cfbef2ab: Layer already exists 
8d3ac3489996: Layer already exists 
1.0: digest: sha256:149ab28a104c0d122c04bb18d25ef43417deda8de5d4c362e265e0bc4a81b9e2 size: 1996
 
root@Debian:~# 
root@Debian:~# ^[[200~docker search ebankoli/ic-webapp
-bash: $'\E[200~docker' : commande introuvable
root@Debian:~# ~
-bash: /root : est un dossier
 
root@Debian:~# docker search ebankoli/ic-webapp
NAME                                                          DESCRIPTION                                     STARS     OFFICIAL
ebankoli/ic-webapp                                                                                            0         
airbyte/webapp                                                                                                13        
hashicorp/demo-webapp-lb-guide                                                                                1         
hashicorp/demo-webapp                                         Sample web app used during Nomad 101 trainin…   1         
camunda/web-modeler-webapp                                                                                    0         
nypl/circ-webapp                                              Library Simplified Circulation Manager Web A…   0         
climatemind/webapp                                                                                            0         
elestio/bigcapital-webapp                                     Bigcapital-webapp, verified and packaged by …   0         
airbyte/airbyte-webapp                                                                                        0         
apache/sdap-nexus-webapp                                                                                      0         
apache/incubator-kie-sandbox-webapp                                                                           0         
webapp7/webapp7                                               Our english academy                             0         
osuosl/python_webapp                                                                                          0         
apache/incubator-kie-sandbox-dev-deployment-dmn-form-webapp                                                   0         
webappappapp/webappweblinux88                                                                                 0         
webappappapp/webappweb8888                                                                                    0         
inseefrlab/satellite-images-webapp                                                                            0         
training/webapp                                                                                               91        
beatboxapp/webapp                                                                                             0         
adeq2019/webapp                                                                                               0         
careapp/webapp-admin                                          The admin web app in ReactJS                    2         
adeqsports/webapp                                                                                             0         
itherz/webapp-full                                            PHP-FPM + nginx + ssh image for full develop…   0         
blackducksoftware/hub-webapp                                  Please contact your CSM or Support Team repr…   0         
envirocar/webapp                                                                                              0         
root@Debian:~# 

root@Debian:~# kubectl create namespace icgroup
kubectl label namespace icgroup env=prod
The connection to the server localhost:8080 was refused - did you specify the right host or port?
E0516 09:57:21.923532   42954 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:57:21.925828   42954 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:57:21.928248   42954 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:57:21.930098   42954 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:57:21.931767   42954 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
The connection to the server localhost:8080 was refused - did you specify the right host or port?
 
root@Debian:~# 
root@Debian:~# kubectl cluster-info
E0516 09:58:30.041607   43005 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:58:30.044281   43005 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:58:30.046010   43005 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:58:30.047909   43005 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"
E0516 09:58:30.050056   43005 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"http://localhost:8080/api?timeout=32s\": dial tcp [::1]:8080: connect: connection refused"

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
The connection to the server localhost:8080 was refused - did you specify the right host or port?
 
root@Debian:~# 
root@Debian:~# systemctl status kubelet
● kubelet.service - kubelet: The Kubernetes Node Agent
     Loaded: loaded (/lib/systemd/system/kubelet.service; enabled; preset: enab>
    Drop-In: /usr/lib/systemd/system/kubelet.service.d
             └─10-kubeadm.conf
     Active: activating (auto-restart) (Result: exit-code) since Fri 2025-05-16>
       Docs: https://kubernetes.io/docs/
    Process: 43045 ExecStart=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET>
   Main PID: 43045 (code=exited, status=1/FAILURE)
        CPU: 88ms
lines 1-9/9 (END)

 
root@Debian:~# 
root@Debian:~# journalctl -u kubelet --no-pager | tail -20
mai 16 10:00:05 Debian systemd[1]: kubelet.service: Main process exited, code=exited, status=1/FAILURE
mai 16 10:00:05 Debian systemd[1]: kubelet.service: Failed with result 'exit-code'.
mai 16 10:00:16 Debian systemd[1]: kubelet.service: Scheduled restart job, restart counter is at 5798.
mai 16 10:00:16 Debian systemd[1]: Stopped kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:16 Debian systemd[1]: Started kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:16 Debian kubelet[43080]: E0516 10:00:16.239395   43080 run.go:74] "command failed" err="failed to load kubelet config file, path: /var/lib/kubelet/config.yaml, error: failed to load Kubelet config file /var/lib/kubelet/config.yaml, error failed to read kubelet config file \"/var/lib/kubelet/config.yaml\", error: open /var/lib/kubelet/config.yaml: no such file or directory"
mai 16 10:00:16 Debian systemd[1]: kubelet.service: Main process exited, code=exited, status=1/FAILURE
mai 16 10:00:16 Debian systemd[1]: kubelet.service: Failed with result 'exit-code'.
mai 16 10:00:26 Debian systemd[1]: kubelet.service: Scheduled restart job, restart counter is at 5799.
mai 16 10:00:26 Debian systemd[1]: Stopped kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:26 Debian systemd[1]: Started kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:26 Debian kubelet[43087]: E0516 10:00:26.479964   43087 run.go:74] "command failed" err="failed to load kubelet config file, path: /var/lib/kubelet/config.yaml, error: failed to load Kubelet config file /var/lib/kubelet/config.yaml, error failed to read kubelet config file \"/var/lib/kubelet/config.yaml\", error: open /var/lib/kubelet/config.yaml: no such file or directory"
mai 16 10:00:26 Debian systemd[1]: kubelet.service: Main process exited, code=exited, status=1/FAILURE
mai 16 10:00:26 Debian systemd[1]: kubelet.service: Failed with result 'exit-code'.
mai 16 10:00:36 Debian systemd[1]: kubelet.service: Scheduled restart job, restart counter is at 5800.
mai 16 10:00:36 Debian systemd[1]: Stopped kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:36 Debian systemd[1]: Started kubelet.service - kubelet: The Kubernetes Node Agent.
mai 16 10:00:36 Debian kubelet[43094]: E0516 10:00:36.743008   43094 run.go:74] "command failed" err="failed to load kubelet config file, path: /var/lib/kubelet/config.yaml, error: failed to load Kubelet config file /var/lib/kubelet/config.yaml, error failed to read kubelet config file \"/var/lib/kubelet/config.yaml\", error: open /var/lib/kubelet/config.yaml: no such file or directory"
mai 16 10:00:36 Debian systemd[1]: kubelet.service: Main process exited, code=exited, status=1/FAILURE
mai 16 10:00:36 Debian systemd[1]: kubelet.service: Failed with result 'exit-code'.
 
root@Debian:~# 
root@Debian:~# ls -l /var/lib/kubelet/config.yaml
ls: impossible d'accéder à '/var/lib/kubelet/config.yaml': Aucun fichier ou dossier de ce type
 
root@Debian:~# sudo kubeadm init
I0516 10:02:22.532278   43176 version.go:256] remote version is much newer: v1.33.1; falling back to: stable-1.30
[init] Using Kubernetes version: v1.30.13
[preflight] Running pre-flight checks
	[WARNING Swap]: swap is supported for cgroup v2 only; the NodeSwap feature gate of the kubelet is beta but disabled by default
error execution phase preflight: [preflight] Some fatal errors occurred:
	[ERROR CRI]: container runtime is not running: output: time="2025-05-16T10:02:23+02:00" level=fatal msg="validate service connection: validate CRI v1 runtime API for endpoint \"unix:///var/run/containerd/containerd.sock\": rpc error: code = Unimplemented desc = unknown service runtime.v1.RuntimeService"
, error: exit status 1
[preflight] If you know what you are doing, you can make a check non-fatal with `--ignore-preflight-errors=...`
To see the stack trace of this error execute with --v=5 or higher

root@Debian:~# 
root@Debian:~# systemctl status containerd
● containerd.service - containerd container runtime
     Loaded: loaded (/lib/systemd/system/containerd.service; enabled; preset: e>
     Active: active (running) since Thu 2025-05-15 17:29:36 CEST; 16h ago
       Docs: https://containerd.io
   Main PID: 563 (containerd)
      Tasks: 8
     Memory: 33.3M
        CPU: 36.319s
     CGroup: /system.slice/containerd.service
             └─563 /usr/bin/containerd

mai 15 17:29:36 Debian containerd[563]: time="2025-05-15T17:29:36.436744446+02:>
mai 15 17:29:36 Debian containerd[563]: time="2025-05-15T17:29:36.436919905+02:>
mai 15 17:29:36 Debian containerd[563]: time="2025-05-15T17:29:36.438680055+02:>
mai 15 17:29:36 Debian containerd[563]: time="2025-05-15T17:29:36.438849436+02:>
mai 15 17:29:36 Debian systemd[1]: Started containerd.service - containerd cont>
mai 15 17:29:36 Debian containerd[563]: time="2025-05-15T17:29:36.501333170+02:>
mai 15 17:37:32 Debian containerd[563]: time="2025-05-15T17:37:32.552151334+02:>
mai 15 17:37:32 Debian containerd[563]: time="2025-05-15T17:37:32.589755890+02:>
mai 15 17:37:32 Debian containerd[563]: time="2025-05-15T17:37:32.589979696+02:>
mai 15 17:37:32 Debian containerd[563]: time="2025-05-15T17:37:32.590782059+02:>

 
root@Debian:~# ^M
-bash: $'\r' : commande introuvable

root@Debian:~# 
root@Debian:~# sudo crictl info
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///run/containerd/containerd.sock": rpc error: code = Unimplemented desc = unknown service runtime.v1.RuntimeService 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///run/crio/crio.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /run/crio/crio.sock: connect: no such file or directory" 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/cri-dockerd.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/cri-dockerd.sock: connect: connection refused" 
FATA[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/cri-dockerd.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/cri-dockerd.sock: connect: connection refused" 
 
root@Debian:~# 
root@Debian:~# sudo nano /etc/containerd/config.toml
root@Debian:~# sudo nano /etc/containerd/config.toml
root@Debian:~# sudo nano /etc/containerd/config.toml
 
root@Debian:~# 
root@Debian:~# sudo systemctl restart containerd
 
root@Debian:~# sudo crictl info
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
{
  "status": {
    "conditions": [
      {
        "type": "RuntimeReady",
        "status": true,
        "reason": "",
        "message": ""
      },
      {
        "type": "NetworkReady",
        "status": false,
        "reason": "NetworkPluginNotReady",
        "message": "Network plugin returns error: cni plugin not initialized"
      },
      {
        "type": "ContainerdHasNoDeprecationWarnings",
        "status": true,
        "reason": "",
        "message": ""
      }
    ]
  },
  "cniconfig": {
    "PluginDirs": [
      "/opt/cni/bin"
    ],
    "PluginConfDir": "/etc/cni/net.d",
    "PluginMaxConfNum": 1,
    "Prefix": "eth",
    "Networks": [
      {
        "Config": {
          "Name": "cni-loopback",
          "CNIVersion": "0.3.1",
          "Plugins": [
            {
              "Network": {
                "type": "loopback",
                "ipam": {},
                "dns": {}
              },
              "Source": "{\"type\":\"loopback\"}"
            }
          ],
          "Source": "{\n\"cniVersion\": \"0.3.1\",\n\"name\": \"cni-loopback\",\n\"plugins\": [{\n  \"type\": \"loopback\"\n}]\n}"
        },
        "IFName": "lo"
      }
    ]
  },
  "config": {
    "containerd": {
      "snapshotter": "overlayfs",
      "defaultRuntimeName": "runc",
      "defaultRuntime": {
        "runtimeType": "",
        "runtimePath": "",
        "runtimeEngine": "",
        "PodAnnotations": null,
        "ContainerAnnotations": null,
        "runtimeRoot": "",
        "options": null,
        "privileged_without_host_devices": false,
        "privileged_without_host_devices_all_devices_allowed": false,
        "baseRuntimeSpec": "",
        "cniConfDir": "",
        "cniMaxConfNum": 0,
        "snapshotter": "",
        "sandboxMode": ""
      },
      "untrustedWorkloadRuntime": {
        "runtimeType": "",
        "runtimePath": "",
        "runtimeEngine": "",
        "PodAnnotations": null,
        "ContainerAnnotations": null,
        "runtimeRoot": "",
        "options": null,
        "privileged_without_host_devices": false,
        "privileged_without_host_devices_all_devices_allowed": false,
        "baseRuntimeSpec": "",
        "cniConfDir": "",
        "cniMaxConfNum": 0,
        "snapshotter": "",
        "sandboxMode": ""
      },
      "runtimes": {
        "runc": {
          "runtimeType": "io.containerd.runc.v2",
          "runtimePath": "",
          "runtimeEngine": "",
          "PodAnnotations": null,
          "ContainerAnnotations": null,
          "runtimeRoot": "",
          "options": {
            "BinaryName": "",
            "CriuImagePath": "",
            "CriuPath": "",
            "CriuWorkPath": "",
            "IoGid": 0,
            "IoUid": 0,
            "NoNewKeyring": false,
            "NoPivotRoot": false,
            "Root": "",
            "ShimCgroup": "",
            "SystemdCgroup": false
          },
          "privileged_without_host_devices": false,
          "privileged_without_host_devices_all_devices_allowed": false,
          "baseRuntimeSpec": "",
          "cniConfDir": "",
          "cniMaxConfNum": 0,
          "snapshotter": "",
          "sandboxMode": "podsandbox"
        }
      },
      "noPivot": false,
      "disableSnapshotAnnotations": true,
      "discardUnpackedLayers": false,
      "ignoreBlockIONotEnabledErrors": false,
      "ignoreRdtNotEnabledErrors": false
    },
    "cni": {
      "binDir": "/opt/cni/bin",
      "confDir": "/etc/cni/net.d",
      "maxConfNum": 1,
      "setupSerially": false,
      "confTemplate": "",
      "ipPref": ""
    },
    "registry": {
      "configPath": "",
      "mirrors": null,
      "configs": null,
      "auths": null,
      "headers": null
    },
    "imageDecryption": {
      "keyModel": "node"
    },
    "disableTCPService": true,
    "streamServerAddress": "127.0.0.1",
    "streamServerPort": "0",
    "streamIdleTimeout": "4h0m0s",
    "enableSelinux": false,
    "selinuxCategoryRange": 1024,
    "sandboxImage": "registry.k8s.io/pause:3.8",
    "statsCollectPeriod": 10,
    "systemdCgroup": false,
    "enableTLSStreaming": false,
    "x509KeyPairStreaming": {
      "tlsCertFile": "",
      "tlsKeyFile": ""
    },
    "maxContainerLogSize": 16384,
    "disableCgroup": false,
    "disableApparmor": false,
    "restrictOOMScoreAdj": false,
    "maxConcurrentDownloads": 3,
    "disableProcMount": false,
    "unsetSeccompProfile": "",
    "tolerateMissingHugetlbController": true,
    "disableHugetlbController": true,
    "device_ownership_from_security_context": false,
    "ignoreImageDefinedVolumes": false,
    "netnsMountsUnderStateDir": false,
    "enableUnprivilegedPorts": false,
    "enableUnprivilegedICMP": false,
    "enableCDI": false,
    "cdiSpecDirs": [
      "/etc/cdi",
      "/var/run/cdi"
    ],
    "imagePullProgressTimeout": "5m0s",
    "drainExecSyncIOTimeout": "0s",
    "imagePullWithSyncFs": false,
    "ignoreDeprecationWarnings": null,
    "containerdRootDir": "/var/lib/containerd",
    "containerdEndpoint": "/run/containerd/containerd.sock",
    "rootDir": "/var/lib/containerd/io.containerd.grpc.v1.cri",
    "stateDir": "/run/containerd/io.containerd.grpc.v1.cri"
  },
  "golang": "go1.23.7",
  "lastCNILoadStatus": "cni config load failed: no network config found in /etc/cni/net.d: cni plugin not initialized: failed to load cni config",
  "lastCNILoadStatus.default": "cni config load failed: no network config found in /etc/cni/net.d: cni plugin not initialized: failed to load cni config"
}
root@Debian:~# 

root@Debian:~# sudo apt update
sudo apt install -y containernetworking-plugins
Atteint :1 http://deb.debian.org/debian bookworm InRelease
Atteint :2 http://repo.mysql.com/apt/debian bookworm InRelease                 
Atteint :3 http://deb.debian.org/debian bookworm-updates InRelease             
Atteint :4 http://security.debian.org/debian-security bookworm-security InRelease
Atteint :5 https://download.docker.com/linux/debian bookworm InRelease         
Réception de :6 https://apt.releases.hashicorp.com bookworm InRelease [12,9 kB]
Atteint :7 https://prod-cdn.packages.k8s.io/repositories/isv:/kubernetes:/core:/stable:/v1.30/deb  InRelease
Err :5 https://download.docker.com/linux/debian bookworm InRelease
  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
Réception de :8 https://apt.releases.hashicorp.com bookworm/main amd64 Packages [182 kB]
195 ko réceptionnés en 1s (132 ko/s)
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
3 paquets peuvent être mis à jour. Exécutez « apt list --upgradable » pour les voir.
W: Une erreur s'est produite lors du contrôle de la signature. Le dépôt n'est pas mis à jour et les fichiers d'index précédents seront utilisés. Erreur de GPG : https://download.docker.com/linux/debian bookworm InRelease : Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Impossible de récupérer https://download.docker.com/linux/debian/dists/bookworm/InRelease  Les signatures suivantes n'ont pas pu être vérifiées car la clé publique n'est pas disponible : NO_PUBKEY 7EA0A9C3F273FCD8
W: Le téléchargement de quelques fichiers d'index a échoué, ils ont été ignorés, ou les anciens ont été utilisés à la place.
Lecture des listes de paquets... Fait
Construction de l'arbre des dépendances... Fait
Lecture des informations d'état... Fait      
Les paquets suivants ont été installés automatiquement et ne sont plus nécessaires :
  libdaxctl1 libdbus-glib-1-2 libndctl6 libpmem1 linux-image-6.1.0-25-amd64
Veuillez utiliser « sudo apt autoremove » pour les supprimer.
Les NOUVEAUX paquets suivants seront installés :
  containernetworking-plugins
0 mis à jour, 1 nouvellement installés, 0 à enlever et 3 non mis à jour.
Il est nécessaire de prendre 6 769 ko dans les archives.
Après cette opération, 45,8 Mo d'espace disque supplémentaires seront utilisés.
Réception de :1 http://deb.debian.org/debian bookworm/main amd64 containernetworking-plugins amd64 1.1.1+ds1-3+b5 [6 769 kB]
6 769 ko réceptionnés en 2s (4 386 ko/s)                     
Sélection du paquet containernetworking-plugins précédemment désélectionné.
(Lecture de la base de données... 186010 fichiers et répertoires déjà installés.
)
Préparation du dépaquetage de .../containernetworking-plugins_1.1.1+ds1-3+b5_amd
64.deb ...
Dépaquetage de containernetworking-plugins (1.1.1+ds1-3+b5) ...
Paramétrage de containernetworking-plugins (1.1.1+ds1-3+b5) ...
root@Debian:~# 

root@Debian:~# sudo systemctl restart containerd
sudo systemctl restart kubelet
 
root@Debian:~# systemctl status kubelet
● kubelet.service - kubelet: The Kubernetes Node Agent
     Loaded: loaded (/lib/systemd/system/kubelet.service; enabled; preset: enab>
    Drop-In: /usr/lib/systemd/system/kubelet.service.d
             └─10-kubeadm.conf
     Active: activating (auto-restart) (Result: exit-code) since Fri 2025-05-16>
       Docs: https://kubernetes.io/docs/
    Process: 44281 ExecStart=/usr/bin/kubelet $KUBELET_KUBECONFIG_ARGS $KUBELET>
   Main PID: 44281 (code=exited, status=1/FAILURE)
        CPU: 78ms
lines 1-9/9 (END)
^C
root@Debian:~# ^C

root@Debian:~# sudo kubeadm init
I0516 10:19:33.832431   44424 version.go:256] remote version is much newer: v1.33.1; falling back to: stable-1.30
[init] Using Kubernetes version: v1.30.13
[preflight] Running pre-flight checks
	[WARNING Swap]: swap is supported for cgroup v2 only; the NodeSwap feature gate of the kubelet is beta but disabled by default
[preflight] Pulling images required for setting up a Kubernetes cluster
[preflight] This might take a minute or two, depending on the speed of your internet connection
[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'
W0516 10:19:34.685899   44424 checks.go:844] detected that the sandbox image "registry.k8s.io/pause:3.8" of the container runtime is inconsistent with that used by kubeadm.It is recommended to use "registry.k8s.io/pause:3.9" as the CRI sandbox image.

[certs] Using certificateDir folder "/etc/kubernetes/pki"
[certs] Generating "ca" certificate and key
[certs] Generating "apiserver" certificate and key
[certs] apiserver serving cert is signed for DNS names [debian kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 192.168.72.148]
[certs] Generating "apiserver-kubelet-client" certificate and key
[certs] Generating "front-proxy-ca" certificate and key
[certs] Generating "front-proxy-client" certificate and key
[certs] Generating "etcd/ca" certificate and key
[certs] Generating "etcd/server" certificate and key
[certs] etcd/server serving cert is signed for DNS names [debian localhost] and IPs [192.168.72.148 127.0.0.1 ::1]
[certs] Generating "etcd/peer" certificate and key
[certs] etcd/peer serving cert is signed for DNS names [debian localhost] and IPs [192.168.72.148 127.0.0.1 ::1]
[certs] Generating "etcd/healthcheck-client" certificate and key
[certs] Generating "apiserver-etcd-client" certificate and key
[certs] Generating "sa" key and public key
[kubeconfig] Using kubeconfig folder "/etc/kubernetes"
[kubeconfig] Writing "admin.conf" kubeconfig file
[kubeconfig] Writing "super-admin.conf" kubeconfig file
[kubeconfig] Writing "kubelet.conf" kubeconfig file
[kubeconfig] Writing "controller-manager.conf" kubeconfig file
[kubeconfig] Writing "scheduler.conf" kubeconfig file
[etcd] Creating static Pod manifest for local etcd in "/etc/kubernetes/manifests"
[control-plane] Using manifest folder "/etc/kubernetes/manifests"
[control-plane] Creating static Pod manifest for "kube-apiserver"
[control-plane] Creating static Pod manifest for "kube-controller-manager"
[control-plane] Creating static Pod manifest for "kube-scheduler"
[kubelet-start] Writing kubelet environment file with flags to file "/var/lib/kubelet/kubeadm-flags.env"
[kubelet-start] Writing kubelet configuration to file "/var/lib/kubelet/config.yaml"
[kubelet-start] Starting the kubelet
[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory "/etc/kubernetes/manifests"
[kubelet-check] Waiting for a healthy kubelet at http://127.0.0.1:10248/healthz. This can take up to 4m0s
[kubelet-check] The kubelet is not healthy after 4m0.002309002s

Unfortunately, an error has occurred:
	The HTTP call equal to 'curl -sSL http://127.0.0.1:10248/healthz' returned error: Get "http://127.0.0.1:10248/healthz": context deadline exceeded


This error is likely caused by:
	- The kubelet is not running
	- The kubelet is unhealthy due to a misconfiguration of the node in some way (required cgroups disabled)

If you are on a systemd-powered system, you can try to troubleshoot the error with the following commands:
	- 'systemctl status kubelet'
	- 'journalctl -xeu kubelet'

Additionally, a control plane component may have crashed or exited when started by the container runtime.
To troubleshoot, list all containers using your preferred container runtimes CLI.
Here is one example how you may list all running Kubernetes containers by using crictl:
	- 'crictl --runtime-endpoint unix:///var/run/containerd/containerd.sock ps -a | grep kube | grep -v pause'
	Once you have found the failing container, you can inspect its logs with:
	- 'crictl --runtime-endpoint unix:///var/run/containerd/containerd.sock logs CONTAINERID'
error execution phase wait-control-plane: could not initialize a Kubernetes cluster
To see the stack trace of this error execute with --v=5 or higher
root@Debian:~# 

root@Debian:~# sudo nano /etc/fstab
 
root@Debian:~# sudo nano /etc/fstab
root@Debian:~# sudo nano /etc/fstab
 
root@Debian:~# 
root@Debian:~# sudo systemctl daemon-reload
root@Debian:~# free -h
swapon --summary
               total       utilisé      libre     partagé tamp/cache   disponible
Mem:           1,9Gi       1,2Gi       101Mi        13Mi       773Mi       707Mi
Échange:       974Mi        90Mi       884Mi
Nom fichier				Type		Taille		UtiliséPriorité
/dev/sda5                               partition	998396		93076	-2
root@Debian:~# ^C
root@Debian:~# sudo swapoff -a
root@Debian:~# free -h
swapon --summary
               total       utilisé      libre     partagé tamp/cache   disponible
Mem:           1,9Gi       1,5Gi        79Mi        14Mi       552Mi       464Mi
Échange:          0B          0B          0B

root@Debian:~# 
root@Debian:~# sudo systemctl restart kubelet
systemctl status kubelet
● kubelet.service - kubelet: The Kubernetes Node Agent
     Loaded: loaded (/lib/systemd/system/kubelet.service; enabled; preset: enab>
    Drop-In: /usr/lib/systemd/system/kubelet.service.d
             └─10-kubeadm.conf
     Active: active (running) since Fri 2025-05-16 10:42:52 CEST; 39ms ago
       Docs: https://kubernetes.io/docs/
   Main PID: 3976 (kubelet)
      Tasks: 6 (limit: 2282)
     Memory: 4.4M
        CPU: 17ms
     CGroup: /system.slice/kubelet.service
             └─3976 /usr/bin/kubelet --bootstrap-kubeconfig=/etc/kubernetes/boo>

mai 16 10:42:52 Debian systemd[1]: Started kubelet.service - kubelet: The Kuber>
lines 1-14/14 (END)

root@Debian:~# 
root@Debian:~# sudo kubeadm init
I0516 10:43:35.591039    4640 version.go:256] remote version is much newer: v1.33.1; falling back to: stable-1.30
[init] Using Kubernetes version: v1.30.13
[preflight] Running pre-flight checks
error execution phase preflight: [preflight] Some fatal errors occurred:
	[ERROR Port-6443]: Port 6443 is in use
	[ERROR Port-10259]: Port 10259 is in use
	[ERROR Port-10257]: Port 10257 is in use
	[ERROR FileAvailable--etc-kubernetes-manifests-kube-apiserver.yaml]: /etc/kubernetes/manifests/kube-apiserver.yaml already exists
	[ERROR FileAvailable--etc-kubernetes-manifests-kube-controller-manager.yaml]: /etc/kubernetes/manifests/kube-controller-manager.yaml already exists
	[ERROR FileAvailable--etc-kubernetes-manifests-kube-scheduler.yaml]: /etc/kubernetes/manifests/kube-scheduler.yaml already exists
	[ERROR FileAvailable--etc-kubernetes-manifests-etcd.yaml]: /etc/kubernetes/manifests/etcd.yaml already exists
	[ERROR Port-10250]: Port 10250 is in use
	[ERROR Port-2379]: Port 2379 is in use
	[ERROR Port-2380]: Port 2380 is in use
	[ERROR DirAvailable--var-lib-etcd]: /var/lib/etcd is not empty
[preflight] If you know what you are doing, you can make a check non-fatal with `--ignore-preflight-errors=...`
To see the stack trace of this error execute with --v=5 or higher
 
root@Debian:~# 
root@Debian:~# sudo netstat -tulnp | grep -E "6443|10259|10257|10250|2379|2380"
tcp        0      0 127.0.0.1:10257         0.0.0.0:*               LISTEN      4277/kube-controlle 
tcp        0      0 127.0.0.1:10259         0.0.0.0:*               LISTEN      4452/kube-scheduler 
tcp        0      0 192.168.72.148:2379     0.0.0.0:*               LISTEN      4290/etcd           
tcp        0      0 192.168.72.148:2380     0.0.0.0:*               LISTEN      4290/etcd           
tcp        0      0 127.0.0.1:2379          0.0.0.0:*               LISTEN      4290/etcd           
tcp6       0      0 :::6443                 :::*                    LISTEN      4616/kube-apiserver 
tcp6       0      0 :::10250                :::*                    LISTEN      3976/kubelet        

root@Debian:~# 
root@Debian:~# sudo systemctl stop kubelet
sudo systemctl stop etcd
sudo systemctl stop kube-apiserver
sudo systemctl stop kube-controller-manager
sudo systemctl stop kube-scheduler
Failed to stop etcd.service: Unit etcd.service not loaded.
Failed to stop kube-apiserver.service: Unit kube-apiserver.service not loaded.
Failed to stop kube-controller-manager.service: Unit kube-controller-manager.service not loaded.
Failed to stop kube-scheduler.service: Unit kube-scheduler.service not loaded.
 
root@Debian:~# sudo rm -rf /etc/kubernetes/manifests/*.yaml
root@Debian:~# sudo systemctl stop kubelet
root@Debian:~# ps aux | grep kube
root        4290  2.1  2.6 11737724 53528 ?      Ssl  10:42   0:04 etcd --advertise-client-urls=https://192.168.72.148:2379 --cert-file=/etc/kubernetes/pki/etcd/server.crt --client-cert-auth=true --data-dir=/var/lib/etcd --experimental-initial-corrupt-check=true --experimental-watch-progress-notify-interval=5s --initial-advertise-peer-urls=https://192.168.72.148:2380 --initial-cluster=debian=https://192.168.72.148:2380 --key-file=/etc/kubernetes/pki/etcd/server.key --listen-client-urls=https://127.0.0.1:2379,https://192.168.72.148:2379 --listen-metrics-urls=http://127.0.0.1:2381 --listen-peer-urls=https://192.168.72.148:2380 --name=debian --peer-cert-file=/etc/kubernetes/pki/etcd/peer.crt --peer-client-cert-auth=true --peer-key-file=/etc/kubernetes/pki/etcd/peer.key --peer-trusted-ca-file=/etc/kubernetes/pki/etcd/ca.crt --snapshot-count=10000 --trusted-ca-file=/etc/kubernetes/pki/etcd/ca.crt
root        4452  0.6  2.4 1285392 49920 ?       Ssl  10:42   0:01 kube-scheduler --authentication-kubeconfig=/etc/kubernetes/scheduler.conf --authorization-kubeconfig=/etc/kubernetes/scheduler.conf --bind-address=127.0.0.1 --kubeconfig=/etc/kubernetes/scheduler.conf --leader-elect=true
root        4616  6.0 11.6 1473700 234528 ?      Ssl  10:43   0:10 kube-apiserver --advertise-address=192.168.72.148 --allow-privileged=true --authorization-mode=Node,RBAC --client-ca-file=/etc/kubernetes/pki/ca.crt --enable-admission-plugins=NodeRestriction --enable-bootstrap-token-auth=true --etcd-cafile=/etc/kubernetes/pki/etcd/ca.crt --etcd-certfile=/etc/kubernetes/pki/apiserver-etcd-client.crt --etcd-keyfile=/etc/kubernetes/pki/apiserver-etcd-client.key --etcd-servers=https://127.0.0.1:2379 --kubelet-client-certificate=/etc/kubernetes/pki/apiserver-kubelet-client.crt --kubelet-client-key=/etc/kubernetes/pki/apiserver-kubelet-client.key --kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname --proxy-client-cert-file=/etc/kubernetes/pki/front-proxy-client.crt --proxy-client-key-file=/etc/kubernetes/pki/front-proxy-client.key --requestheader-allowed-names=front-proxy-client --requestheader-client-ca-file=/etc/kubernetes/pki/front-proxy-ca.crt --requestheader-extra-headers-prefix=X-Remote-Extra- --requestheader-group-headers=X-Remote-Group --requestheader-username-headers=X-Remote-User --secure-port=6443 --service-account-issuer=https://kubernetes.default.svc.cluster.local --service-account-key-file=/etc/kubernetes/pki/sa.pub --service-account-signing-key-file=/etc/kubernetes/pki/sa.key --service-cluster-ip-range=10.96.0.0/12 --tls-cert-file=/etc/kubernetes/pki/apiserver.crt --tls-private-key-file=/etc/kubernetes/pki/apiserver.key
root        4807  2.6  4.9 1333764 100328 ?      Ssl  10:45   0:01 kube-controller-manager --authentication-kubeconfig=/etc/kubernetes/controller-manager.conf --authorization-kubeconfig=/etc/kubernetes/controller-manager.conf --bind-address=127.0.0.1 --client-ca-file=/etc/kubernetes/pki/ca.crt --cluster-name=kubernetes --cluster-signing-cert-file=/etc/kubernetes/pki/ca.crt --cluster-signing-key-file=/etc/kubernetes/pki/ca.key --controllers=*,bootstrapsigner,tokencleaner --kubeconfig=/etc/kubernetes/controller-manager.conf --leader-elect=true --requestheader-client-ca-file=/etc/kubernetes/pki/front-proxy-ca.crt --root-ca-file=/etc/kubernetes/pki/ca.crt --service-account-private-key-file=/etc/kubernetes/pki/sa.key --use-service-account-credentials=true
root        4859  0.0  0.1   6356  2280 pts/0    S+   10:46   0:00 grep kube

root@Debian:~# 
root@Debian:~# sudo kill -9 4290 4452 4616 4807
root@Debian:~# ps aux | grep kube
root        4968  0.0  0.1   6356  2184 pts/0    S+   10:47   0:00 grep kube
root@Debian:~# 
root@Debian:~# sudo rm -rf /etc/kubernetes/manifests/*.yaml
sudo rm -rf /var/lib/etcd
sudo kubeadm reset
[reset] Reading configuration from the cluster...
[reset] FYI: You can look at this config file with 'kubectl -n kube-system get cm kubeadm-config -o yaml'
W0516 10:47:44.850431    4978 reset.go:124] [reset] Unable to fetch the kubeadm-config ConfigMap from cluster: failed to get config map: Get "https://192.168.72.148:6443/api/v1/namespaces/kube-system/configmaps/kubeadm-config?timeout=10s": dial tcp 192.168.72.148:6443: connect: connection refused
W0516 10:47:44.851152    4978 preflight.go:56] [reset] WARNING: Changes made to this host by 'kubeadm init' or 'kubeadm join' will be reverted.
[reset] Are you sure you want to proceed? [y/N]: y
[preflight] Running pre-flight checks
W0516 10:47:50.241614    4978 removeetcdmember.go:106] [reset] No kubeadm config, using etcd pod spec to get data directory
[reset] Deleted contents of the etcd data directory: /var/lib/etcd
[reset] Stopping the kubelet service
[reset] Unmounting mounted directories in "/var/lib/kubelet"
[reset] Deleting contents of directories: [/etc/kubernetes/manifests /var/lib/kubelet /etc/kubernetes/pki]
[reset] Deleting files: [/etc/kubernetes/admin.conf /etc/kubernetes/super-admin.conf /etc/kubernetes/kubelet.conf /etc/kubernetes/bootstrap-kubelet.conf /etc/kubernetes/controller-manager.conf /etc/kubernetes/scheduler.conf]

The reset process does not clean CNI configuration. To do so, you must remove /etc/cni/net.d

The reset process does not reset or clean up iptables rules or IPVS tables.
If you wish to reset iptables, you must do so manually by using the "iptables" command.

If your cluster was setup to utilize IPVS, run ipvsadm --clear (or similar)
to reset your system's IPVS tables.

The reset process does not clean your kubeconfig files and you must remove them manually.
Please, check the contents of the $HOME/.kube/config file.
root@Debian:~# 

root@Debian:~# sudo rm -rf /etc/cni/net.d
root@Debian:~# ls -l /etc/cni/net.d
ls: impossible d'accéder à '/etc/cni/net.d': Aucun fichier ou dossier de ce type
 
root@Debian:~# 
root@Debian:~# sudo kubeadm init
I0516 10:51:17.074764    5213 version.go:256] remote version is much newer: v1.33.1; falling back to: stable-1.30
[init] Using Kubernetes version: v1.30.13
[preflight] Running pre-flight checks
[preflight] Pulling images required for setting up a Kubernetes cluster
[preflight] This might take a minute or two, depending on the speed of your internet connection
[preflight] You can also perform this action in beforehand using 'kubeadm config images pull'
W0516 10:51:17.935235    5213 checks.go:844] detected that the sandbox image "registry.k8s.io/pause:3.8" of the container runtime is inconsistent with that used by kubeadm.It is recommended to use "registry.k8s.io/pause:3.9" as the CRI sandbox image.
[certs] Using certificateDir folder "/etc/kubernetes/pki"
[certs] Generating "ca" certificate and key
[certs] Generating "apiserver" certificate and key
[certs] apiserver serving cert is signed for DNS names [debian kubernetes kubernetes.default kubernetes.default.svc kubernetes.default.svc.cluster.local] and IPs [10.96.0.1 192.168.72.148]
[certs] Generating "apiserver-kubelet-client" certificate and key
[certs] Generating "front-proxy-ca" certificate and key
[certs] Generating "front-proxy-client" certificate and key
[certs] Generating "etcd/ca" certificate and key
[certs] Generating "etcd/server" certificate and key
[certs] etcd/server serving cert is signed for DNS names [debian localhost] and IPs [192.168.72.148 127.0.0.1 ::1]
[certs] Generating "etcd/peer" certificate and key
[certs] etcd/peer serving cert is signed for DNS names [debian localhost] and IPs [192.168.72.148 127.0.0.1 ::1]
[certs] Generating "etcd/healthcheck-client" certificate and key
[certs] Generating "apiserver-etcd-client" certificate and key
[certs] Generating "sa" key and public key
[kubeconfig] Using kubeconfig folder "/etc/kubernetes"
[kubeconfig] Writing "admin.conf" kubeconfig file
[kubeconfig] Writing "super-admin.conf" kubeconfig file
[kubeconfig] Writing "kubelet.conf" kubeconfig file
[kubeconfig] Writing "controller-manager.conf" kubeconfig file
[kubeconfig] Writing "scheduler.conf" kubeconfig file
[etcd] Creating static Pod manifest for local etcd in "/etc/kubernetes/manifests"
[control-plane] Using manifest folder "/etc/kubernetes/manifests"
[control-plane] Creating static Pod manifest for "kube-apiserver"
[control-plane] Creating static Pod manifest for "kube-controller-manager"
[control-plane] Creating static Pod manifest for "kube-scheduler"
[kubelet-start] Writing kubelet environment file with flags to file "/var/lib/kubelet/kubeadm-flags.env"
[kubelet-start] Writing kubelet configuration to file "/var/lib/kubelet/config.yaml"
[kubelet-start] Starting the kubelet
[wait-control-plane] Waiting for the kubelet to boot up the control plane as static Pods from directory "/etc/kubernetes/manifests"
[kubelet-check] Waiting for a healthy kubelet at http://127.0.0.1:10248/healthz. This can take up to 4m0s
[kubelet-check] The kubelet is healthy after 1.008539069s
[api-check] Waiting for a healthy API server. This can take up to 4m0s
[api-check] The API server is healthy after 5.002075818s
[upload-config] Storing the configuration used in ConfigMap "kubeadm-config" in the "kube-system" Namespace
[kubelet] Creating a ConfigMap "kubelet-config" in namespace kube-system with the configuration for the kubelets in the cluster
[upload-certs] Skipping phase. Please see --upload-certs
[mark-control-plane] Marking the node debian as control-plane by adding the labels: [node-role.kubernetes.io/control-plane node.kubernetes.io/exclude-from-external-load-balancers]
[mark-control-plane] Marking the node debian as control-plane by adding the taints [node-role.kubernetes.io/control-plane:NoSchedule]
[bootstrap-token] Using token: qfj776.3mykic4ojhp0c1rg
[bootstrap-token] Configuring bootstrap tokens, cluster-info ConfigMap, RBAC Roles
[bootstrap-token] Configured RBAC rules to allow Node Bootstrap tokens to get nodes
[bootstrap-token] Configured RBAC rules to allow Node Bootstrap tokens to post CSRs in order for nodes to get long term certificate credentials
[bootstrap-token] Configured RBAC rules to allow the csrapprover controller automatically approve CSRs from a Node Bootstrap Token
[bootstrap-token] Configured RBAC rules to allow certificate rotation for all node client certificates in the cluster
[bootstrap-token] Creating the "cluster-info" ConfigMap in the "kube-public" namespace
[kubelet-finalize] Updating "/etc/kubernetes/kubelet.conf" to point to a rotatable kubelet client certificate and key
[addons] Applied essential addon: CoreDNS
[addons] Applied essential addon: kube-proxy

Your Kubernetes control-plane has initialized successfully!

To start using your cluster, you need to run the following as a regular user:

  mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config

Alternatively, if you are the root user, you can run:

  export KUBECONFIG=/etc/kubernetes/admin.conf

You should now deploy a pod network to the cluster.
Run "kubectl apply -f [podnetwork].yaml" with one of the options listed at:
  https://kubernetes.io/docs/concepts/cluster-administration/addons/

Then you can join any number of worker nodes by running the following on each as root:

kubeadm join 192.168.72.148:6443 --token qfj776.3mykic4ojhp0c1rg \
	--discovery-token-ca-cert-hash sha256:db952fe7fb2300f70a4449a62e2a570343e4f374ba9507181dc32ab4179d427b 

root@Debian:~# 
root@Debian:~# export KUBECONFIG=/etc/kubernetes/admin.conf
root@Debian:~# mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
root@Debian:~# kubectl apply -f [podnetwork].yaml
error: the path "[podnetwork].yaml" does not exist
root@Debian:~# 

root@Debian:~# kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
error: error validating "https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml": error validating data: failed to download openapi: Get "https://192.168.72.148:6443/openapi/v2?timeout=32s": dial tcp 192.168.72.148:6443: connect: connection refused; if you choose to ignore these errors, turn validation off with --validate=false
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# kubectl get pods -n kube-system
E0516 10:57:18.733219    7171 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:57:18.735324    7171 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:57:18.737594    7171 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:57:18.739350    7171 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:57:18.741443    7171 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
The connection to the server 192.168.72.148:6443 was refused - did you specify the right host or port?
root@Debian:~# 
root@Debian:~# 
root@Debian:~# sudo crictl --runtime-endpoint unix:///run/containerd/containerd.sock ps -a | grep kube | grep -v pause
4dadb4d9ea1c3       e60416bd78b65       28 seconds ago      Running             kube-apiserver            8                   4691de9bf5bb8       kube-apiserver-debian
d3add000518e4       e60416bd78b65       2 minutes ago       Exited              kube-apiserver            7                   fc3601949d133       kube-apiserver-debian
df4c04858bf62       c32cfb72baccb       2 minutes ago       Running             kube-controller-manager   10                  e004208ae6715       kube-controller-manager-debian
e9507440c0204       c32cfb72baccb       4 minutes ago       Exited              kube-controller-manager   9                   e004208ae6715       kube-controller-manager-debian
0986b75774695       12675fc0a409d       5 minutes ago       Running             kube-scheduler            7                   ecd62e9a857d5       kube-scheduler-debian
668b7c09a52d4       12675fc0a409d       6 minutes ago       Exited              kube-scheduler            6                   6c0a4368c362b       kube-scheduler-debian
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# sudo crictl logs d3add000518e4  # kube-apiserver (Exited)
sudo crictl logs e9507440c0204  # kube-controller-manager (Exited)
sudo crictl logs 668b7c09a52d4  # kube-scheduler (Exited)
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
I0516 08:55:47.945003       1 options.go:221] external host was not specified, using 192.168.72.148
I0516 08:55:47.945953       1 server.go:148] Version: v1.30.13
I0516 08:55:47.946091       1 server.go:150] "Golang settings" GOGC="" GOMAXPROCS="" GOTRACEBACK=""
I0516 08:55:48.455888       1 shared_informer.go:313] Waiting for caches to sync for node_authorizer
I0516 08:55:48.462903       1 shared_informer.go:313] Waiting for caches to sync for *generic.policySource[*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicy,*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicyBinding,k8s.io/apiserver/pkg/admission/plugin/policy/validating.Validator]
I0516 08:55:48.470619       1 plugins.go:157] Loaded 12 mutating admission controller(s) successfully in the following order: NamespaceLifecycle,LimitRanger,ServiceAccount,NodeRestriction,TaintNodesByCondition,Priority,DefaultTolerationSeconds,DefaultStorageClass,StorageObjectInUseProtection,RuntimeClass,DefaultIngressClass,MutatingAdmissionWebhook.
I0516 08:55:48.471539       1 plugins.go:160] Loaded 13 validating admission controller(s) successfully in the following order: LimitRanger,ServiceAccount,PodSecurity,Priority,PersistentVolumeClaimResize,RuntimeClass,CertificateApproval,CertificateSigning,ClusterTrustBundleAttest,CertificateSubjectRestriction,ValidatingAdmissionPolicy,ValidatingAdmissionWebhook,ResourceQuota.
I0516 08:55:48.471933       1 instance.go:299] Using reconciler: lease
I0516 08:55:48.496880       1 handler.go:286] Adding GroupVersion apiextensions.k8s.io v1 to ResourceManager
W0516 08:55:48.497029       1 genericapiserver.go:733] Skipping API apiextensions.k8s.io/v1beta1 because it has no resources.
I0516 08:55:48.685595       1 handler.go:286] Adding GroupVersion  v1 to ResourceManager
I0516 08:55:48.687979       1 instance.go:696] API group "internal.apiserver.k8s.io" is not enabled, skipping.
I0516 08:55:48.890456       1 instance.go:696] API group "storagemigration.k8s.io" is not enabled, skipping.
I0516 08:55:49.020324       1 instance.go:696] API group "resource.k8s.io" is not enabled, skipping.
I0516 08:55:49.047379       1 handler.go:286] Adding GroupVersion authentication.k8s.io v1 to ResourceManager
W0516 08:55:49.047433       1 genericapiserver.go:733] Skipping API authentication.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.047445       1 genericapiserver.go:733] Skipping API authentication.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.048072       1 handler.go:286] Adding GroupVersion authorization.k8s.io v1 to ResourceManager
W0516 08:55:49.048113       1 genericapiserver.go:733] Skipping API authorization.k8s.io/v1beta1 because it has no resources.
I0516 08:55:49.048849       1 handler.go:286] Adding GroupVersion autoscaling v2 to ResourceManager
I0516 08:55:49.049780       1 handler.go:286] Adding GroupVersion autoscaling v1 to ResourceManager
W0516 08:55:49.049822       1 genericapiserver.go:733] Skipping API autoscaling/v2beta1 because it has no resources.
W0516 08:55:49.049832       1 genericapiserver.go:733] Skipping API autoscaling/v2beta2 because it has no resources.
I0516 08:55:49.051276       1 handler.go:286] Adding GroupVersion batch v1 to ResourceManager
W0516 08:55:49.051319       1 genericapiserver.go:733] Skipping API batch/v1beta1 because it has no resources.
I0516 08:55:49.052033       1 handler.go:286] Adding GroupVersion certificates.k8s.io v1 to ResourceManager
W0516 08:55:49.052075       1 genericapiserver.go:733] Skipping API certificates.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.052085       1 genericapiserver.go:733] Skipping API certificates.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.052609       1 handler.go:286] Adding GroupVersion coordination.k8s.io v1 to ResourceManager
W0516 08:55:49.052651       1 genericapiserver.go:733] Skipping API coordination.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.052788       1 genericapiserver.go:733] Skipping API discovery.k8s.io/v1beta1 because it has no resources.
I0516 08:55:49.053287       1 handler.go:286] Adding GroupVersion discovery.k8s.io v1 to ResourceManager
I0516 08:55:49.054523       1 handler.go:286] Adding GroupVersion networking.k8s.io v1 to ResourceManager
W0516 08:55:49.054571       1 genericapiserver.go:733] Skipping API networking.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.054585       1 genericapiserver.go:733] Skipping API networking.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.055067       1 handler.go:286] Adding GroupVersion node.k8s.io v1 to ResourceManager
W0516 08:55:49.055112       1 genericapiserver.go:733] Skipping API node.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.055122       1 genericapiserver.go:733] Skipping API node.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.055888       1 handler.go:286] Adding GroupVersion policy v1 to ResourceManager
W0516 08:55:49.055933       1 genericapiserver.go:733] Skipping API policy/v1beta1 because it has no resources.
I0516 08:55:49.057169       1 handler.go:286] Adding GroupVersion rbac.authorization.k8s.io v1 to ResourceManager
W0516 08:55:49.057203       1 genericapiserver.go:733] Skipping API rbac.authorization.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.057213       1 genericapiserver.go:733] Skipping API rbac.authorization.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.057894       1 handler.go:286] Adding GroupVersion scheduling.k8s.io v1 to ResourceManager
W0516 08:55:49.057943       1 genericapiserver.go:733] Skipping API scheduling.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.057953       1 genericapiserver.go:733] Skipping API scheduling.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.059548       1 handler.go:286] Adding GroupVersion storage.k8s.io v1 to ResourceManager
W0516 08:55:49.059606       1 genericapiserver.go:733] Skipping API storage.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.059616       1 genericapiserver.go:733] Skipping API storage.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.060503       1 handler.go:286] Adding GroupVersion flowcontrol.apiserver.k8s.io v1 to ResourceManager
I0516 08:55:49.061340       1 handler.go:286] Adding GroupVersion flowcontrol.apiserver.k8s.io v1beta3 to ResourceManager
W0516 08:55:49.061385       1 genericapiserver.go:733] Skipping API flowcontrol.apiserver.k8s.io/v1beta2 because it has no resources.
W0516 08:55:49.061397       1 genericapiserver.go:733] Skipping API flowcontrol.apiserver.k8s.io/v1beta1 because it has no resources.
I0516 08:55:49.064994       1 handler.go:286] Adding GroupVersion apps v1 to ResourceManager
W0516 08:55:49.065043       1 genericapiserver.go:733] Skipping API apps/v1beta2 because it has no resources.
W0516 08:55:49.065053       1 genericapiserver.go:733] Skipping API apps/v1beta1 because it has no resources.
I0516 08:55:49.066385       1 handler.go:286] Adding GroupVersion admissionregistration.k8s.io v1 to ResourceManager
W0516 08:55:49.066428       1 genericapiserver.go:733] Skipping API admissionregistration.k8s.io/v1beta1 because it has no resources.
W0516 08:55:49.066438       1 genericapiserver.go:733] Skipping API admissionregistration.k8s.io/v1alpha1 because it has no resources.
I0516 08:55:49.066918       1 handler.go:286] Adding GroupVersion events.k8s.io v1 to ResourceManager
W0516 08:55:49.066960       1 genericapiserver.go:733] Skipping API events.k8s.io/v1beta1 because it has no resources.
I0516 08:55:49.076463       1 handler.go:286] Adding GroupVersion apiregistration.k8s.io v1 to ResourceManager
W0516 08:55:49.076494       1 genericapiserver.go:733] Skipping API apiregistration.k8s.io/v1beta1 because it has no resources.
I0516 08:55:49.564700       1 dynamic_cafile_content.go:157] "Starting controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:55:49.565036       1 dynamic_cafile_content.go:157] "Starting controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:55:49.565176       1 secure_serving.go:213] Serving securely on [::]:6443
I0516 08:55:49.565271       1 controller.go:128] Shutting down kubernetes service endpoint reconciler
I0516 08:55:49.565387       1 apiservice_controller.go:97] Starting APIServiceRegistrationController
I0516 08:55:49.565462       1 cache.go:32] Waiting for caches to sync for APIServiceRegistrationController controller
I0516 08:55:49.565536       1 dynamic_serving_content.go:132] "Starting controller" name="serving-cert::/etc/kubernetes/pki/apiserver.crt::/etc/kubernetes/pki/apiserver.key"
I0516 08:55:49.565660       1 tlsconfig.go:240] "Starting DynamicServingCertificateController"
I0516 08:55:49.566149       1 gc_controller.go:78] Starting apiserver lease garbage collector
I0516 08:55:49.566271       1 apf_controller.go:374] Starting API Priority and Fairness config controller
I0516 08:55:49.566933       1 cluster_authentication_trust_controller.go:440] Starting cluster_authentication_trust_controller controller
I0516 08:55:49.566946       1 shared_informer.go:313] Waiting for caches to sync for cluster_authentication_trust_controller
I0516 08:55:49.567055       1 customresource_discovery_controller.go:289] Starting DiscoveryController
I0516 08:55:49.567079       1 crdregistration_controller.go:111] Starting crd-autoregister controller
I0516 08:55:49.567126       1 shared_informer.go:313] Waiting for caches to sync for crd-autoregister
I0516 08:55:49.568133       1 dynamic_cafile_content.go:157] "Starting controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:55:49.568422       1 controller.go:116] Starting legacy_token_tracking_controller
I0516 08:55:49.568500       1 shared_informer.go:313] Waiting for caches to sync for configmaps
I0516 08:55:49.569005       1 available_controller.go:423] Starting AvailableConditionController
I0516 08:55:49.569082       1 cache.go:32] Waiting for caches to sync for AvailableConditionController controller
I0516 08:55:49.569166       1 controller.go:80] Starting OpenAPI V3 AggregationController
I0516 08:55:49.569231       1 dynamic_cafile_content.go:157] "Starting controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:55:49.569353       1 system_namespaces_controller.go:67] Starting system namespaces controller
I0516 08:55:49.565472       1 dynamic_serving_content.go:132] "Starting controller" name="aggregator-proxy-cert::/etc/kubernetes/pki/front-proxy-client.crt::/etc/kubernetes/pki/front-proxy-client.key"
I0516 08:55:49.565487       1 aggregator.go:163] waiting for initial CRD sync...
I0516 08:55:49.565497       1 controller.go:78] Starting OpenAPI AggregationController
I0516 08:55:49.569743       1 controller.go:139] Starting OpenAPI controller
I0516 08:55:49.569768       1 controller.go:87] Starting OpenAPI V3 controller
I0516 08:55:49.569789       1 naming_controller.go:291] Starting NamingConditionController
I0516 08:55:49.569937       1 establishing_controller.go:76] Starting EstablishingController
I0516 08:55:49.569959       1 nonstructuralschema_controller.go:192] Starting NonStructuralSchemaConditionController
I0516 08:55:49.569968       1 apiapproval_controller.go:186] Starting KubernetesAPIApprovalPolicyConformantConditionController
I0516 08:55:49.569979       1 crd_finalizer.go:266] Starting CRDFinalizer
E0516 08:55:49.574477       1 controller.go:131] Unable to remove endpoints from kubernetes service: StorageError: key not found, Code: 1, Key: /registry/masterleases/192.168.72.148, ResourceVersion: 0, AdditionalErrorMsg: 
I0516 08:55:49.575096       1 crd_finalizer.go:270] Shutting down CRDFinalizer
I0516 08:55:49.575177       1 apiapproval_controller.go:190] Shutting down KubernetesAPIApprovalPolicyConformantConditionController
I0516 08:55:49.575260       1 nonstructuralschema_controller.go:196] Shutting down NonStructuralSchemaConditionController
I0516 08:55:49.575322       1 establishing_controller.go:80] Shutting down EstablishingController
I0516 08:55:49.575378       1 naming_controller.go:295] Shutting down NamingConditionController
E0516 08:55:49.575871       1 controller.go:92] timed out waiting for caches to sync
I0516 08:55:49.575963       1 controller.go:93] Shutting down OpenAPI V3 controller
E0516 08:55:49.576060       1 controller.go:145] timed out waiting for caches to sync
I0516 08:55:49.576139       1 controller.go:84] Shutting down OpenAPI AggregationController
E0516 08:55:49.576260       1 system_namespaces_controller.go:70] timed out waiting for caches to sync
F0516 08:55:49.576337       1 hooks.go:203] PostStartHook "crd-informer-synced" failed: timed out waiting for the condition
I0516 08:55:49.647598       1 dynamic_cafile_content.go:171] "Shutting down controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:55:49.647862       1 controller.go:86] Shutting down OpenAPI V3 AggregationController
E0516 08:55:49.647960       1 cache.go:35] Unable to sync caches for AvailableConditionController controller
I0516 08:55:49.648070       1 available_controller.go:431] Shutting down AvailableConditionController
E0516 08:55:49.648208       1 shared_informer.go:316] unable to sync caches for configmaps
E0516 08:55:49.648326       1 controller.go:89] timed out waiting for caches to sync
I0516 08:55:49.648489       1 dynamic_cafile_content.go:171] "Shutting down controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:55:49.648620       1 dynamic_cafile_content.go:171] "Shutting down controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
E0516 08:55:49.648853       1 controller.go:145] "Failed to ensure lease exists, will retry" err="Get \"https://[::1]:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/apiserver-by3nylsstkokpui7jmjtdpfjei\": context canceled" interval="200ms"
F0516 08:55:49.648972       1 hooks.go:203] PostStartHook "priority-and-fairness-config-producer" failed: APF bootstrap ensurer timed out waiting for cache sync
E0516 08:55:49.702881       1 shared_informer.go:316] unable to sync caches for crd-autoregister
I0516 08:55:49.703018       1 crdregistration_controller.go:116] Shutting down crd-autoregister controller
I0516 08:55:49.703119       1 dynamic_serving_content.go:146] "Shutting down controller" name="aggregator-proxy-cert::/etc/kubernetes/pki/front-proxy-client.crt::/etc/kubernetes/pki/front-proxy-client.key"
E0516 08:55:49.703222       1 customresource_discovery_controller.go:292] timed out waiting for caches to sync
E0516 08:55:49.703308       1 shared_informer.go:316] unable to sync caches for cluster_authentication_trust_controller
E0516 08:55:49.703423       1 gc_controller.go:84] timed out waiting for caches to sync
I0516 08:55:49.703597       1 object_count_tracker.go:151] "StorageObjectCountTracker pruner is exiting"
E0516 08:55:49.703704       1 cache.go:35] Unable to sync caches for APIServiceRegistrationController controller
I0516 08:55:49.703836       1 controller.go:157] Shutting down quota evaluator
E0516 08:55:49.703949       1 shared_informer.go:316] unable to sync caches for *generic.policySource[*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicy,*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicyBinding,k8s.io/apiserver/pkg/admission/plugin/policy/validating.Validator]
I0516 08:55:49.704025       1 customresource_discovery_controller.go:293] Shutting down DiscoveryController
I0516 08:55:49.704305       1 cluster_authentication_trust_controller.go:448] Shutting down cluster_authentication_trust_controller controller
I0516 08:55:49.704428       1 gc_controller.go:85] Shutting down apiserver lease garbage collector
I0516 08:55:49.704505       1 apiservice_controller.go:101] Shutting down APIServiceRegistrationController
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
I0516 08:53:31.343995       1 serving.go:380] Generated self-signed cert in-memory
I0516 08:53:31.586299       1 controllermanager.go:189] "Starting" version="v1.30.13"
I0516 08:53:31.586401       1 controllermanager.go:191] "Golang settings" GOGC="" GOMAXPROCS="" GOTRACEBACK=""
I0516 08:53:31.589040       1 dynamic_cafile_content.go:157] "Starting controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:53:31.589198       1 secure_serving.go:213] Serving securely on 127.0.0.1:10257
I0516 08:53:31.589376       1 dynamic_cafile_content.go:157] "Starting controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:53:31.589588       1 leaderelection.go:250] attempting to acquire leader lease kube-system/kube-controller-manager...
I0516 08:53:31.590044       1 tlsconfig.go:240] "Starting DynamicServingCertificateController"
E0516 08:53:31.590357       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:53:35.207924       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:53:37.566721       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:53:40.877968       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: leases.coordination.k8s.io "kube-controller-manager" is forbidden: User "system:kube-controller-manager" cannot get resource "leases" in API group "coordination.k8s.io" in the namespace "kube-system"
E0516 08:53:51.693284       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:53:53.954897       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:53:58.346154       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:01.764448       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:04.901532       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:07.367596       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:10.217745       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:12.302492       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:15.502311       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:18.028997       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:21.700940       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:24.875945       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:27.041363       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:29.795195       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:33.684431       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:36.635109       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:41.339989       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: leases.coordination.k8s.io "kube-controller-manager" is forbidden: User "system:kube-controller-manager" cannot get resource "leases" in API group "coordination.k8s.io" in the namespace "kube-system"
I0516 08:54:45.627823       1 leaderelection.go:260] successfully acquired lease kube-system/kube-controller-manager
I0516 08:54:45.632351       1 event.go:389] "Event occurred" object="kube-system/kube-controller-manager" fieldPath="" kind="Lease" apiVersion="coordination.k8s.io/v1" type="Normal" reason="LeaderElection" message="Debian_9df4c1ff-7935-44e2-9aec-215082296491 became leader"
I0516 08:54:45.643031       1 controllermanager.go:761] "Started controller" controller="serviceaccount-token-controller"
I0516 08:54:45.643732       1 shared_informer.go:313] Waiting for caches to sync for tokens
I0516 08:54:45.650421       1 controllermanager.go:761] "Started controller" controller="persistentvolume-protection-controller"
I0516 08:54:45.653538       1 pv_protection_controller.go:78] "Starting PV protection controller" logger="persistentvolume-protection-controller"
I0516 08:54:45.653821       1 shared_informer.go:313] Waiting for caches to sync for PV protection
I0516 08:54:45.654695       1 controllermanager.go:761] "Started controller" controller="daemonset-controller"
I0516 08:54:45.655329       1 daemon_controller.go:289] "Starting daemon sets controller" logger="daemonset-controller"
I0516 08:54:45.655577       1 shared_informer.go:313] Waiting for caches to sync for daemon sets
I0516 08:54:45.657976       1 controllermanager.go:761] "Started controller" controller="certificatesigningrequest-cleaner-controller"
I0516 08:54:45.658255       1 controllermanager.go:739] "Warning: skipping controller" controller="node-ipam-controller"
I0516 08:54:45.658226       1 cleaner.go:83] "Starting CSR cleaner controller" logger="certificatesigningrequest-cleaner-controller"
I0516 08:54:45.661737       1 controllermanager.go:761] "Started controller" controller="persistentvolumeclaim-protection-controller"
I0516 08:54:45.661937       1 core.go:294] "Will not configure cloud provider routes for allocate-node-cidrs" logger="node-route-controller" CIDRs=false routes=true
I0516 08:54:45.662138       1 controllermanager.go:739] "Warning: skipping controller" controller="node-route-controller"
I0516 08:54:45.661903       1 pvc_protection_controller.go:102] "Starting PVC protection controller" logger="persistentvolumeclaim-protection-controller"
I0516 08:54:45.663323       1 shared_informer.go:313] Waiting for caches to sync for PVC protection
I0516 08:54:45.665719       1 controllermanager.go:761] "Started controller" controller="ttl-after-finished-controller"
I0516 08:54:45.666184       1 ttlafterfinished_controller.go:109] "Starting TTL after finished controller" logger="ttl-after-finished-controller"
I0516 08:54:45.667514       1 shared_informer.go:313] Waiting for caches to sync for TTL after finished
I0516 08:54:45.669187       1 controllermanager.go:761] "Started controller" controller="legacy-serviceaccount-token-cleaner-controller"
I0516 08:54:45.670166       1 legacy_serviceaccount_token_cleaner.go:103] "Starting legacy service account token cleaner controller" logger="legacy-serviceaccount-token-cleaner-controller"
I0516 08:54:45.670323       1 shared_informer.go:313] Waiting for caches to sync for legacy-service-account-token-cleaner
I0516 08:54:45.672658       1 controllermanager.go:761] "Started controller" controller="endpointslice-mirroring-controller"
I0516 08:54:45.673052       1 endpointslicemirroring_controller.go:223] "Starting EndpointSliceMirroring controller" logger="endpointslice-mirroring-controller"
I0516 08:54:45.673158       1 shared_informer.go:313] Waiting for caches to sync for endpoint_slice_mirroring
I0516 08:54:45.675948       1 controllermanager.go:761] "Started controller" controller="pod-garbage-collector-controller"
I0516 08:54:45.676677       1 gc_controller.go:101] "Starting GC controller" logger="pod-garbage-collector-controller"
I0516 08:54:45.676877       1 shared_informer.go:313] Waiting for caches to sync for GC
I0516 08:54:45.679325       1 controllermanager.go:761] "Started controller" controller="replicaset-controller"
I0516 08:54:45.679589       1 replica_set.go:214] "Starting controller" logger="replicaset-controller" name="replicaset"
I0516 08:54:45.679608       1 shared_informer.go:313] Waiting for caches to sync for ReplicaSet
I0516 08:54:45.686984       1 controllermanager.go:761] "Started controller" controller="horizontal-pod-autoscaler-controller"
I0516 08:54:45.687407       1 horizontal.go:196] "Starting HPA controller" logger="horizontal-pod-autoscaler-controller"
I0516 08:54:45.687459       1 shared_informer.go:313] Waiting for caches to sync for HPA
I0516 08:54:45.690366       1 controllermanager.go:761] "Started controller" controller="ephemeral-volume-controller"
I0516 08:54:45.690445       1 controllermanager.go:713] "Controller is disabled by a feature gate" controller="resourceclaim-controller" requiredFeatureGates=["DynamicResourceAllocation"]
I0516 08:54:45.691452       1 controller.go:170] "Starting ephemeral volume controller" logger="ephemeral-volume-controller"
I0516 08:54:45.691474       1 shared_informer.go:313] Waiting for caches to sync for ephemeral
I0516 08:54:45.711696       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="horizontalpodautoscalers.autoscaling"
I0516 08:54:45.712676       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="jobs.batch"
W0516 08:54:45.712842       1 shared_informer.go:597] resyncPeriod 16h32m51.80267775s is smaller than resyncCheckPeriod 17h15m53.52923148s and the informer has already started. Changing it to 17h15m53.52923148s
I0516 08:54:45.713088       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="serviceaccounts"
I0516 08:54:45.713327       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="networkpolicies.networking.k8s.io"
W0516 08:54:45.713452       1 shared_informer.go:597] resyncPeriod 16h18m44.561399076s is smaller than resyncCheckPeriod 17h15m53.52923148s and the informer has already started. Changing it to 17h15m53.52923148s
I0516 08:54:45.713668       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="endpoints"
I0516 08:54:45.713871       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="roles.rbac.authorization.k8s.io"
I0516 08:54:45.714119       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="rolebindings.rbac.authorization.k8s.io"
I0516 08:54:45.714357       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="csistoragecapacities.storage.k8s.io"
I0516 08:54:45.714488       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="leases.coordination.k8s.io"
I0516 08:54:45.714715       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="endpointslices.discovery.k8s.io"
I0516 08:54:45.714863       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="statefulsets.apps"
I0516 08:54:45.714980       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="controllerrevisions.apps"
I0516 08:54:45.715118       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="poddisruptionbudgets.policy"
I0516 08:54:45.715236       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="cronjobs.batch"
I0516 08:54:45.715376       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="podtemplates"
I0516 08:54:45.715493       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="daemonsets.apps"
I0516 08:54:45.715642       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="deployments.apps"
I0516 08:54:45.715764       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="replicasets.apps"
I0516 08:54:45.715934       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="ingresses.networking.k8s.io"
I0516 08:54:45.716170       1 resource_quota_monitor.go:224] "QuotaMonitor created object count evaluator" logger="resourcequota-controller" resource="limitranges"
I0516 08:54:45.716356       1 controllermanager.go:761] "Started controller" controller="resourcequota-controller"
I0516 08:54:45.716407       1 resource_quota_controller.go:294] "Starting resource quota controller" logger="resourcequota-controller"
I0516 08:54:45.716909       1 shared_informer.go:313] Waiting for caches to sync for resource quota
I0516 08:54:45.717443       1 resource_quota_monitor.go:305] "QuotaMonitor running" logger="resourcequota-controller"
I0516 08:54:45.721264       1 controllermanager.go:761] "Started controller" controller="token-cleaner-controller"
I0516 08:54:45.721715       1 tokencleaner.go:112] "Starting token cleaner controller" logger="token-cleaner-controller"
I0516 08:54:45.721965       1 shared_informer.go:313] Waiting for caches to sync for token_cleaner
I0516 08:54:45.722095       1 shared_informer.go:320] Caches are synced for token_cleaner
E0516 08:54:45.724586       1 core.go:274] "Failed to start cloud node lifecycle controller" err="no cloud provider provided" logger="cloud-node-lifecycle-controller"
I0516 08:54:45.724918       1 controllermanager.go:739] "Warning: skipping controller" controller="cloud-node-lifecycle-controller"
I0516 08:54:45.728462       1 controllermanager.go:761] "Started controller" controller="persistentvolume-attach-detach-controller"
I0516 08:54:45.728824       1 attach_detach_controller.go:342] "Starting attach detach controller" logger="persistentvolume-attach-detach-controller"
I0516 08:54:45.729024       1 shared_informer.go:313] Waiting for caches to sync for attach detach
I0516 08:54:45.731457       1 controllermanager.go:761] "Started controller" controller="replicationcontroller-controller"
I0516 08:54:45.731804       1 replica_set.go:214] "Starting controller" logger="replicationcontroller-controller" name="replicationcontroller"
I0516 08:54:45.732139       1 shared_informer.go:313] Waiting for caches to sync for ReplicationController
I0516 08:54:45.734988       1 controllermanager.go:761] "Started controller" controller="job-controller"
I0516 08:54:45.735169       1 job_controller.go:224] "Starting job controller" logger="job-controller"
I0516 08:54:45.735362       1 shared_informer.go:313] Waiting for caches to sync for job
I0516 08:54:45.739278       1 controllermanager.go:761] "Started controller" controller="taint-eviction-controller"
I0516 08:54:45.740049       1 taint_eviction.go:285] "Starting" logger="taint-eviction-controller" controller="taint-eviction-controller"
I0516 08:54:45.744222       1 taint_eviction.go:291] "Sending events to api server" logger="taint-eviction-controller"
I0516 08:54:45.743882       1 shared_informer.go:320] Caches are synced for tokens
I0516 08:54:45.744283       1 shared_informer.go:313] Waiting for caches to sync for taint-eviction-controller
I0516 08:54:45.748771       1 controllermanager.go:761] "Started controller" controller="persistentvolume-expander-controller"
I0516 08:54:45.748943       1 expand_controller.go:330] "Starting expand controller" logger="persistentvolume-expander-controller"
I0516 08:54:45.749283       1 shared_informer.go:313] Waiting for caches to sync for expand
I0516 08:54:45.752030       1 controllermanager.go:761] "Started controller" controller="serviceaccount-controller"
I0516 08:54:45.752170       1 serviceaccounts_controller.go:111] "Starting service account controller" logger="serviceaccount-controller"
I0516 08:54:45.752366       1 shared_informer.go:313] Waiting for caches to sync for service account
I0516 08:54:45.755216       1 controllermanager.go:761] "Started controller" controller="statefulset-controller"
I0516 08:54:45.755433       1 stateful_set.go:163] "Starting stateful set controller" logger="statefulset-controller"
I0516 08:54:45.755649       1 shared_informer.go:313] Waiting for caches to sync for stateful set
I0516 08:54:45.758341       1 controllermanager.go:761] "Started controller" controller="certificatesigningrequest-approving-controller"
I0516 08:54:45.758605       1 certificate_controller.go:115] "Starting certificate controller" logger="certificatesigningrequest-approving-controller" name="csrapproving"
I0516 08:54:45.758636       1 shared_informer.go:313] Waiting for caches to sync for certificate-csrapproving
I0516 08:54:45.761280       1 controllermanager.go:761] "Started controller" controller="ttl-controller"
I0516 08:54:45.764881       1 ttl_controller.go:124] "Starting TTL controller" logger="ttl-controller"
I0516 08:54:45.765091       1 shared_informer.go:313] Waiting for caches to sync for TTL
I0516 08:54:45.779278       1 controllermanager.go:761] "Started controller" controller="validatingadmissionpolicy-status-controller"
I0516 08:54:45.779305       1 controllermanager.go:713] "Controller is disabled by a feature gate" controller="service-cidr-controller" requiredFeatureGates=["MultiCIDRServiceAllocator"]
I0516 08:54:45.779390       1 shared_informer.go:313] Waiting for caches to sync for validatingadmissionpolicy-status
I0516 08:54:45.786263       1 controllermanager.go:761] "Started controller" controller="endpoints-controller"
I0516 08:54:45.786593       1 endpoints_controller.go:177] "Starting endpoint controller" logger="endpoints-controller"
I0516 08:54:45.786609       1 shared_informer.go:313] Waiting for caches to sync for endpoint
I0516 08:54:45.842792       1 controllermanager.go:761] "Started controller" controller="endpointslice-controller"
I0516 08:54:45.843405       1 endpointslice_controller.go:274] "Starting endpoint slice controller" logger="endpointslice-controller"
I0516 08:54:45.843471       1 shared_informer.go:313] Waiting for caches to sync for endpoint_slice
I0516 08:54:45.934475       1 controllermanager.go:761] "Started controller" controller="disruption-controller"
I0516 08:54:45.935399       1 disruption.go:433] "Sending events to api server." logger="disruption-controller"
I0516 08:54:45.935665       1 disruption.go:444] "Starting disruption controller" logger="disruption-controller"
I0516 08:54:45.935825       1 shared_informer.go:313] Waiting for caches to sync for disruption
E0516 08:54:45.985465       1 core.go:105] "Failed to start service controller" err="WARNING: no cloud provider provided, services of type LoadBalancer will fail" logger="service-lb-controller"
I0516 08:54:45.985683       1 controllermanager.go:739] "Warning: skipping controller" controller="service-lb-controller"
I0516 08:54:45.985893       1 controllermanager.go:739] "Warning: skipping controller" controller="storage-version-migrator-controller"
I0516 08:54:46.035416       1 controllermanager.go:761] "Started controller" controller="persistentvolume-binder-controller"
I0516 08:54:46.035739       1 pv_controller_base.go:313] "Starting persistent volume controller" logger="persistentvolume-binder-controller"
I0516 08:54:46.036079       1 shared_informer.go:313] Waiting for caches to sync for persistent volume
I0516 08:54:46.084406       1 controllermanager.go:761] "Started controller" controller="root-ca-certificate-publisher-controller"
I0516 08:54:46.084686       1 controllermanager.go:713] "Controller is disabled by a feature gate" controller="storageversion-garbage-collector-controller" requiredFeatureGates=["APIServerIdentity","StorageVersionAPI"]
I0516 08:54:46.084871       1 publisher.go:102] "Starting root CA cert publisher controller" logger="root-ca-certificate-publisher-controller"
I0516 08:54:46.085027       1 shared_informer.go:313] Waiting for caches to sync for crt configmap
I0516 08:54:46.136750       1 controllermanager.go:761] "Started controller" controller="certificatesigningrequest-signing-controller"
I0516 08:54:46.137059       1 certificate_controller.go:115] "Starting certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kubelet-serving"
I0516 08:54:46.137171       1 shared_informer.go:313] Waiting for caches to sync for certificate-csrsigning-kubelet-serving
I0516 08:54:46.137337       1 certificate_controller.go:115] "Starting certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kubelet-client"
I0516 08:54:46.137505       1 shared_informer.go:313] Waiting for caches to sync for certificate-csrsigning-kubelet-client
I0516 08:54:46.137623       1 certificate_controller.go:115] "Starting certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kube-apiserver-client"
I0516 08:54:46.137783       1 shared_informer.go:313] Waiting for caches to sync for certificate-csrsigning-kube-apiserver-client
I0516 08:54:46.137950       1 certificate_controller.go:115] "Starting certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-legacy-unknown"
I0516 08:54:46.138013       1 shared_informer.go:313] Waiting for caches to sync for certificate-csrsigning-legacy-unknown
I0516 08:54:46.138136       1 dynamic_serving_content.go:132] "Starting controller" name="csr-controller::/etc/kubernetes/pki/ca.crt::/etc/kubernetes/pki/ca.key"
I0516 08:54:46.138465       1 dynamic_serving_content.go:132] "Starting controller" name="csr-controller::/etc/kubernetes/pki/ca.crt::/etc/kubernetes/pki/ca.key"
I0516 08:54:46.138740       1 dynamic_serving_content.go:132] "Starting controller" name="csr-controller::/etc/kubernetes/pki/ca.crt::/etc/kubernetes/pki/ca.key"
I0516 08:54:46.139090       1 dynamic_serving_content.go:132] "Starting controller" name="csr-controller::/etc/kubernetes/pki/ca.crt::/etc/kubernetes/pki/ca.key"
I0516 08:54:46.185536       1 controllermanager.go:761] "Started controller" controller="bootstrap-signer-controller"
I0516 08:54:46.185644       1 shared_informer.go:313] Waiting for caches to sync for bootstrap_signer
I0516 08:54:46.235600       1 node_lifecycle_controller.go:425] "Controller will reconcile labels" logger="node-lifecycle-controller"
I0516 08:54:46.235828       1 controllermanager.go:761] "Started controller" controller="node-lifecycle-controller"
I0516 08:54:46.236001       1 node_lifecycle_controller.go:459] "Sending events to api server" logger="node-lifecycle-controller"
I0516 08:54:46.236174       1 node_lifecycle_controller.go:470] "Starting node controller" logger="node-lifecycle-controller"
I0516 08:54:46.236244       1 shared_informer.go:313] Waiting for caches to sync for taint
I0516 08:54:46.285634       1 controllermanager.go:761] "Started controller" controller="clusterrole-aggregation-controller"
I0516 08:54:46.285798       1 clusterroleaggregation_controller.go:189] "Starting ClusterRoleAggregator controller" logger="clusterrole-aggregation-controller"
I0516 08:54:46.285881       1 shared_informer.go:313] Waiting for caches to sync for ClusterRoleAggregator
I0516 08:54:46.442055       1 controllermanager.go:761] "Started controller" controller="namespace-controller"
I0516 08:54:46.442153       1 namespace_controller.go:197] "Starting namespace controller" logger="namespace-controller"
I0516 08:54:46.442172       1 shared_informer.go:313] Waiting for caches to sync for namespace
I0516 08:54:46.585020       1 controllermanager.go:761] "Started controller" controller="garbage-collector-controller"
I0516 08:54:46.585292       1 garbagecollector.go:146] "Starting controller" logger="garbage-collector-controller" controller="garbagecollector"
I0516 08:54:46.585314       1 shared_informer.go:313] Waiting for caches to sync for garbage collector
I0516 08:54:46.585465       1 graph_builder.go:336] "Running" logger="garbage-collector-controller" component="GraphBuilder"
I0516 08:54:46.635534       1 controllermanager.go:761] "Started controller" controller="deployment-controller"
I0516 08:54:46.635745       1 deployment_controller.go:168] "Starting controller" logger="deployment-controller" controller="deployment"
I0516 08:54:46.635882       1 shared_informer.go:313] Waiting for caches to sync for deployment
I0516 08:54:46.734796       1 controllermanager.go:761] "Started controller" controller="cronjob-controller"
I0516 08:54:46.737324       1 cronjob_controllerv2.go:139] "Starting cronjob controller v2" logger="cronjob-controller"
I0516 08:54:46.737542       1 shared_informer.go:313] Waiting for caches to sync for cronjob
I0516 08:54:46.743582       1 shared_informer.go:313] Waiting for caches to sync for resource quota
I0516 08:54:46.756909       1 shared_informer.go:320] Caches are synced for PV protection
I0516 08:54:46.759864       1 actual_state_of_world.go:544] "Failed to update statusUpdateNeeded field in actual state of world" logger="persistentvolume-attach-detach-controller" err="Failed to set statusUpdateNeeded to needed true, because nodeName=\"debian\" does not exist"
I0516 08:54:46.767153       1 shared_informer.go:320] Caches are synced for TTL
I0516 08:54:46.778557       1 shared_informer.go:320] Caches are synced for GC
I0516 08:54:46.778957       1 shared_informer.go:320] Caches are synced for legacy-service-account-token-cleaner
I0516 08:54:46.779488       1 shared_informer.go:320] Caches are synced for validatingadmissionpolicy-status
I0516 08:54:46.785236       1 shared_informer.go:320] Caches are synced for crt configmap
I0516 08:54:46.788181       1 shared_informer.go:320] Caches are synced for HPA
I0516 08:54:46.788464       1 shared_informer.go:320] Caches are synced for ClusterRoleAggregator
I0516 08:54:46.788805       1 shared_informer.go:320] Caches are synced for bootstrap_signer
I0516 08:54:46.792059       1 shared_informer.go:320] Caches are synced for ephemeral
I0516 08:54:46.806785       1 shared_informer.go:313] Waiting for caches to sync for garbage collector
I0516 08:54:46.829791       1 shared_informer.go:320] Caches are synced for attach detach
I0516 08:54:46.832422       1 shared_informer.go:320] Caches are synced for ReplicationController
I0516 08:54:46.837107       1 shared_informer.go:320] Caches are synced for taint
I0516 08:54:46.837215       1 node_lifecycle_controller.go:1227] "Initializing eviction metric for zone" logger="node-lifecycle-controller" zone=""
I0516 08:54:46.837284       1 node_lifecycle_controller.go:879] "Missing timestamp for Node. Assuming now as a timestamp" logger="node-lifecycle-controller" node="debian"
I0516 08:54:46.837334       1 node_lifecycle_controller.go:1031] "Controller detected that all Nodes are not-Ready. Entering master disruption mode" logger="node-lifecycle-controller"
I0516 08:54:46.837746       1 shared_informer.go:320] Caches are synced for cronjob
I0516 08:54:46.837818       1 shared_informer.go:320] Caches are synced for certificate-csrsigning-kubelet-client
I0516 08:54:46.837909       1 shared_informer.go:320] Caches are synced for persistent volume
I0516 08:54:46.837942       1 shared_informer.go:320] Caches are synced for certificate-csrsigning-kube-apiserver-client
I0516 08:54:46.837992       1 shared_informer.go:320] Caches are synced for job
I0516 08:54:46.838040       1 shared_informer.go:320] Caches are synced for certificate-csrsigning-kubelet-serving
I0516 08:54:46.838167       1 shared_informer.go:320] Caches are synced for certificate-csrsigning-legacy-unknown
I0516 08:54:46.842534       1 shared_informer.go:320] Caches are synced for namespace
I0516 08:54:46.843904       1 shared_informer.go:320] Caches are synced for endpoint_slice
I0516 08:54:46.844931       1 shared_informer.go:320] Caches are synced for taint-eviction-controller
I0516 08:54:46.849544       1 shared_informer.go:320] Caches are synced for expand
I0516 08:54:46.853042       1 shared_informer.go:320] Caches are synced for service account
I0516 08:54:46.856564       1 shared_informer.go:320] Caches are synced for daemon sets
I0516 08:54:46.859179       1 shared_informer.go:320] Caches are synced for certificate-csrapproving
I0516 08:54:46.863799       1 shared_informer.go:320] Caches are synced for PVC protection
I0516 08:54:46.868538       1 shared_informer.go:320] Caches are synced for TTL after finished
I0516 08:54:46.873391       1 shared_informer.go:320] Caches are synced for endpoint_slice_mirroring
I0516 08:54:46.886937       1 shared_informer.go:320] Caches are synced for endpoint
I0516 08:54:46.936839       1 shared_informer.go:320] Caches are synced for deployment
I0516 08:54:46.956806       1 shared_informer.go:320] Caches are synced for stateful set
I0516 08:54:46.981696       1 shared_informer.go:320] Caches are synced for ReplicaSet
I0516 08:54:46.981880       1 replica_set.go:676] "Finished syncing" logger="replicaset-controller" kind="ReplicaSet" key="kube-system/coredns-55cb58b774" duration="96.446µs"
I0516 08:54:47.017512       1 shared_informer.go:320] Caches are synced for resource quota
I0516 08:54:47.036426       1 shared_informer.go:320] Caches are synced for disruption
I0516 08:54:47.045583       1 shared_informer.go:320] Caches are synced for resource quota
I0516 08:54:47.486096       1 shared_informer.go:320] Caches are synced for garbage collector
I0516 08:54:47.486134       1 garbagecollector.go:157] "All resource monitors have synced. Proceeding to collect garbage" logger="garbage-collector-controller"
I0516 08:54:47.508029       1 shared_informer.go:320] Caches are synced for garbage collector
E0516 08:54:49.645041       1 leaderelection.go:340] Failed to update lock optimitically: Put "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused, falling back to slow path
E0516 08:54:49.645458       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:51.646407       1 leaderelection.go:340] Failed to update lock optimitically: Put "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused, falling back to slow path
E0516 08:54:51.647129       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:53.646331       1 leaderelection.go:340] Failed to update lock optimitically: Put "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused, falling back to slow path
E0516 08:54:53.647035       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:55.647674       1 leaderelection.go:340] Failed to update lock optimitically: Put "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused, falling back to slow path
E0516 08:54:55.648902       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
E0516 08:54:57.646219       1 leaderelection.go:340] Failed to update lock optimitically: Put "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused, falling back to slow path
E0516 08:54:57.646797       1 leaderelection.go:347] error retrieving resource lock kube-system/kube-controller-manager: Get "https://192.168.72.148:6443/apis/coordination.k8s.io/v1/namespaces/kube-system/leases/kube-controller-manager?timeout=5s": dial tcp 192.168.72.148:6443: connect: connection refused
I0516 08:54:59.645189       1 leaderelection.go:285] failed to renew lease kube-system/kube-controller-manager: timed out waiting for the condition
E0516 08:54:59.645407       1 controllermanager.go:304] "leaderelection lost"
I0516 08:54:59.645487       1 event.go:389] "Event occurred" object="kube-system/kube-controller-manager" fieldPath="" kind="Lease" apiVersion="coordination.k8s.io/v1" type="Normal" reason="LeaderElection" message="Debian_9df4c1ff-7935-44e2-9aec-215082296491 stopped leading"
I0516 08:54:59.645563       1 garbagecollector.go:166] "Shutting down controller" logger="garbage-collector-controller" controller="garbagecollector"
I0516 08:54:59.646215       1 disruption.go:456] "Shutting down disruption controller" logger="disruption-controller"
I0516 08:54:59.646266       1 resource_quota_controller.go:317] "Shutting down resource quota controller" logger="resourcequota-controller"
I0516 08:54:59.646296       1 replica_set.go:226] "Shutting down controller" logger="replicaset-controller" name="replicaset"
I0516 08:54:59.646332       1 stateful_set.go:175] "Shutting down statefulset controller" logger="statefulset-controller"
I0516 08:54:59.646366       1 deployment_controller.go:180] "Shutting down controller" logger="deployment-controller" controller="deployment"
I0516 08:54:59.646412       1 endpoints_controller.go:194] "Shutting down endpoint controller" logger="endpoints-controller"
I0516 08:54:59.646448       1 endpointslicemirroring_controller.go:236] "Shutting down EndpointSliceMirroring controller" logger="endpointslice-mirroring-controller"
I0516 08:54:59.646487       1 ttlafterfinished_controller.go:121] "Shutting down TTL after finished controller" logger="ttl-after-finished-controller"
I0516 08:54:59.646518       1 pvc_protection_controller.go:114] "Shutting down PVC protection controller" logger="persistentvolumeclaim-protection-controller"
I0516 08:54:59.646546       1 certificate_controller.go:127] "Shutting down certificate controller" logger="certificatesigningrequest-approving-controller" name="csrapproving"
I0516 08:54:59.646578       1 daemon_controller.go:303] "Shutting down daemon sets controller" logger="daemonset-controller"
I0516 08:54:59.646607       1 serviceaccounts_controller.go:123] "Shutting down service account controller" logger="serviceaccount-controller"
I0516 08:54:59.646631       1 expand_controller.go:342] "Shutting down expand controller" logger="persistentvolume-expander-controller"
I0516 08:54:59.646686       1 taint_eviction.go:359] "Shutting down controller" logger="taint-eviction-controller" controller="taint-eviction-controller"
I0516 08:54:59.646712       1 endpointslice_controller.go:289] "Shutting down endpoint slice controller" logger="endpointslice-controller"
I0516 08:54:59.646836       1 namespace_controller.go:209] "Shutting down namespace controller" logger="namespace-controller"
I0516 08:54:59.646873       1 pv_controller_base.go:329] "Shutting down persistent volume controller" logger="persistentvolume-binder-controller"
I0516 08:54:59.646901       1 pv_controller_base.go:601] "Claim worker queue shutting down" logger="persistentvolume-binder-controller"
I0516 08:54:59.646935       1 certificate_controller.go:127] "Shutting down certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-legacy-unknown"
I0516 08:54:59.646963       1 certificate_controller.go:127] "Shutting down certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kubelet-serving"
I0516 08:54:59.646993       1 job_controller.go:238] "Shutting down job controller" logger="job-controller"
I0516 08:54:59.647030       1 certificate_controller.go:127] "Shutting down certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kube-apiserver-client"
I0516 08:54:59.647061       1 certificate_controller.go:127] "Shutting down certificate controller" logger="certificatesigningrequest-signing-controller" name="csrsigning-kubelet-client"
I0516 08:54:59.647091       1 cronjob_controllerv2.go:151] "Shutting down cronjob controller v2" logger="cronjob-controller"
I0516 08:54:59.647160       1 node_lifecycle_controller.go:507] "Shutting down node controller" logger="node-lifecycle-controller"
I0516 08:54:59.647213       1 replica_set.go:226] "Shutting down controller" logger="replicationcontroller-controller" name="replicationcontroller"
I0516 08:54:59.647268       1 attach_detach_controller.go:372] "Shutting down attach detach controller" logger="persistentvolume-attach-detach-controller"
I0516 08:54:59.648106       1 graph_builder.go:364] "stopped monitors" logger="garbage-collector-controller" stopped=48 total=48
I0516 08:54:59.648202       1 graph_builder.go:365] "Stopping" logger="garbage-collector-controller" component="GraphBuilder"
I0516 08:54:59.648524       1 resource_quota_controller.go:279] "resource quota controller worker shutting down" logger="resourcequota-controller"
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
I0516 08:51:44.522535       1 serving.go:380] Generated self-signed cert in-memory
W0516 08:51:45.741490       1 requestheader_controller.go:193] Unable to get configmap/extension-apiserver-authentication in kube-system.  Usually fixed by 'kubectl create rolebinding -n kube-system ROLEBINDING_NAME --role=extension-apiserver-authentication-reader --serviceaccount=YOUR_NS:YOUR_SA'
W0516 08:51:45.742505       1 authentication.go:368] Error looking up in-cluster authentication configuration: configmaps "extension-apiserver-authentication" is forbidden: User "system:kube-scheduler" cannot get resource "configmaps" in API group "" in the namespace "kube-system"
W0516 08:51:45.744059       1 authentication.go:369] Continuing without authentication configuration. This may treat all requests as anonymous.
W0516 08:51:45.744139       1 authentication.go:370] To require authentication configuration lookup to succeed, set --authentication-tolerate-lookup-failure=false
I0516 08:51:45.788533       1 server.go:154] "Starting Kubernetes Scheduler" version="v1.30.13"
I0516 08:51:45.788783       1 server.go:156] "Golang settings" GOGC="" GOMAXPROCS="" GOTRACEBACK=""
I0516 08:51:45.798956       1 secure_serving.go:213] Serving securely on 127.0.0.1:10259
I0516 08:51:45.799757       1 configmap_cafile_content.go:202] "Starting controller" name="client-ca::kube-system::extension-apiserver-authentication::client-ca-file"
I0516 08:51:45.811663       1 shared_informer.go:313] Waiting for caches to sync for client-ca::kube-system::extension-apiserver-authentication::client-ca-file
I0516 08:51:45.799774       1 tlsconfig.go:240] "Starting DynamicServingCertificateController"
W0516 08:51:45.820670       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PersistentVolumeClaim: persistentvolumeclaims is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumeclaims" in API group "" at the cluster scope
E0516 08:51:45.820780       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PersistentVolumeClaim: failed to list *v1.PersistentVolumeClaim: persistentvolumeclaims is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumeclaims" in API group "" at the cluster scope
W0516 08:51:45.821061       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Node: nodes is forbidden: User "system:kube-scheduler" cannot list resource "nodes" in API group "" at the cluster scope
E0516 08:51:45.821111       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Node: failed to list *v1.Node: nodes is forbidden: User "system:kube-scheduler" cannot list resource "nodes" in API group "" at the cluster scope
W0516 08:51:45.821223       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.CSIDriver: csidrivers.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csidrivers" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:45.821454       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.CSIDriver: failed to list *v1.CSIDriver: csidrivers.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csidrivers" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:45.821767       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Pod: pods is forbidden: User "system:kube-scheduler" cannot list resource "pods" in API group "" at the cluster scope
E0516 08:51:45.822229       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Pod: failed to list *v1.Pod: pods is forbidden: User "system:kube-scheduler" cannot list resource "pods" in API group "" at the cluster scope
W0516 08:51:45.822604       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.ReplicationController: replicationcontrollers is forbidden: User "system:kube-scheduler" cannot list resource "replicationcontrollers" in API group "" at the cluster scope
E0516 08:51:45.822714       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.ReplicationController: failed to list *v1.ReplicationController: replicationcontrollers is forbidden: User "system:kube-scheduler" cannot list resource "replicationcontrollers" in API group "" at the cluster scope
W0516 08:51:45.827217       1 reflector.go:547] runtime/asm_amd64.s:1700: failed to list *v1.ConfigMap: configmaps "extension-apiserver-authentication" is forbidden: User "system:kube-scheduler" cannot list resource "configmaps" in API group "" in the namespace "kube-system"
E0516 08:51:45.827428       1 reflector.go:150] runtime/asm_amd64.s:1700: Failed to watch *v1.ConfigMap: failed to list *v1.ConfigMap: configmaps "extension-apiserver-authentication" is forbidden: User "system:kube-scheduler" cannot list resource "configmaps" in API group "" in the namespace "kube-system"
W0516 08:51:45.840192       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.ReplicaSet: replicasets.apps is forbidden: User "system:kube-scheduler" cannot list resource "replicasets" in API group "apps" at the cluster scope
E0516 08:51:45.840243       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.ReplicaSet: failed to list *v1.ReplicaSet: replicasets.apps is forbidden: User "system:kube-scheduler" cannot list resource "replicasets" in API group "apps" at the cluster scope
W0516 08:51:45.840418       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Service: services is forbidden: User "system:kube-scheduler" cannot list resource "services" in API group "" at the cluster scope
E0516 08:51:45.840444       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Service: failed to list *v1.Service: services is forbidden: User "system:kube-scheduler" cannot list resource "services" in API group "" at the cluster scope
W0516 08:51:45.840546       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Namespace: namespaces is forbidden: User "system:kube-scheduler" cannot list resource "namespaces" in API group "" at the cluster scope
E0516 08:51:45.840592       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Namespace: failed to list *v1.Namespace: namespaces is forbidden: User "system:kube-scheduler" cannot list resource "namespaces" in API group "" at the cluster scope
W0516 08:51:45.840655       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PersistentVolume: persistentvolumes is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumes" in API group "" at the cluster scope
E0516 08:51:45.840675       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PersistentVolume: failed to list *v1.PersistentVolume: persistentvolumes is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumes" in API group "" at the cluster scope
W0516 08:51:45.840730       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.CSINode: csinodes.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csinodes" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:45.840753       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.CSINode: failed to list *v1.CSINode: csinodes.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csinodes" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:45.840801       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PodDisruptionBudget: poddisruptionbudgets.policy is forbidden: User "system:kube-scheduler" cannot list resource "poddisruptionbudgets" in API group "policy" at the cluster scope
E0516 08:51:45.840825       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PodDisruptionBudget: failed to list *v1.PodDisruptionBudget: poddisruptionbudgets.policy is forbidden: User "system:kube-scheduler" cannot list resource "poddisruptionbudgets" in API group "policy" at the cluster scope
W0516 08:51:45.840893       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.StorageClass: storageclasses.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "storageclasses" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:45.840915       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.StorageClass: failed to list *v1.StorageClass: storageclasses.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "storageclasses" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:45.840953       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.CSIStorageCapacity: csistoragecapacities.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csistoragecapacities" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:45.840972       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.CSIStorageCapacity: failed to list *v1.CSIStorageCapacity: csistoragecapacities.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csistoragecapacities" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:45.841158       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.StatefulSet: statefulsets.apps is forbidden: User "system:kube-scheduler" cannot list resource "statefulsets" in API group "apps" at the cluster scope
E0516 08:51:45.841274       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.StatefulSet: failed to list *v1.StatefulSet: statefulsets.apps is forbidden: User "system:kube-scheduler" cannot list resource "statefulsets" in API group "apps" at the cluster scope
W0516 08:51:46.626590       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PersistentVolumeClaim: persistentvolumeclaims is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumeclaims" in API group "" at the cluster scope
E0516 08:51:46.626761       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PersistentVolumeClaim: failed to list *v1.PersistentVolumeClaim: persistentvolumeclaims is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumeclaims" in API group "" at the cluster scope
W0516 08:51:46.717347       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Service: services is forbidden: User "system:kube-scheduler" cannot list resource "services" in API group "" at the cluster scope
E0516 08:51:46.717557       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Service: failed to list *v1.Service: services is forbidden: User "system:kube-scheduler" cannot list resource "services" in API group "" at the cluster scope
W0516 08:51:46.745833       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PodDisruptionBudget: poddisruptionbudgets.policy is forbidden: User "system:kube-scheduler" cannot list resource "poddisruptionbudgets" in API group "policy" at the cluster scope
E0516 08:51:46.745874       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PodDisruptionBudget: failed to list *v1.PodDisruptionBudget: poddisruptionbudgets.policy is forbidden: User "system:kube-scheduler" cannot list resource "poddisruptionbudgets" in API group "policy" at the cluster scope
W0516 08:51:46.781808       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.StorageClass: storageclasses.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "storageclasses" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:46.782087       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.StorageClass: failed to list *v1.StorageClass: storageclasses.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "storageclasses" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:46.790865       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.CSIDriver: csidrivers.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csidrivers" in API group "storage.k8s.io" at the cluster scope
E0516 08:51:46.790901       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.CSIDriver: failed to list *v1.CSIDriver: csidrivers.storage.k8s.io is forbidden: User "system:kube-scheduler" cannot list resource "csidrivers" in API group "storage.k8s.io" at the cluster scope
W0516 08:51:46.801283       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.ReplicationController: replicationcontrollers is forbidden: User "system:kube-scheduler" cannot list resource "replicationcontrollers" in API group "" at the cluster scope
E0516 08:51:46.801573       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.ReplicationController: failed to list *v1.ReplicationController: replicationcontrollers is forbidden: User "system:kube-scheduler" cannot list resource "replicationcontrollers" in API group "" at the cluster scope
W0516 08:51:46.822184       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.PersistentVolume: persistentvolumes is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumes" in API group "" at the cluster scope
E0516 08:51:46.822284       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.PersistentVolume: failed to list *v1.PersistentVolume: persistentvolumes is forbidden: User "system:kube-scheduler" cannot list resource "persistentvolumes" in API group "" at the cluster scope
W0516 08:51:46.883644       1 reflector.go:547] runtime/asm_amd64.s:1700: failed to list *v1.ConfigMap: configmaps "extension-apiserver-authentication" is forbidden: User "system:kube-scheduler" cannot list resource "configmaps" in API group "" in the namespace "kube-system"
E0516 08:51:46.883682       1 reflector.go:150] runtime/asm_amd64.s:1700: Failed to watch *v1.ConfigMap: failed to list *v1.ConfigMap: configmaps "extension-apiserver-authentication" is forbidden: User "system:kube-scheduler" cannot list resource "configmaps" in API group "" in the namespace "kube-system"
W0516 08:51:46.884847       1 reflector.go:547] k8s.io/client-go/informers/factory.go:160: failed to list *v1.Namespace: namespaces is forbidden: User "system:kube-scheduler" cannot list resource "namespaces" in API group "" at the cluster scope
E0516 08:51:46.884879       1 reflector.go:150] k8s.io/client-go/informers/factory.go:160: Failed to watch *v1.Namespace: failed to list *v1.Namespace: namespaces is forbidden: User "system:kube-scheduler" cannot list resource "namespaces" in API group "" at the cluster scope
E0516 08:51:48.869125       1 server.go:214] "waiting for handlers to sync" err="context canceled"
I0516 08:51:48.877312       1 tlsconfig.go:255] "Shutting down DynamicServingCertificateController"
I0516 08:51:48.880353       1 secure_serving.go:258] Stopped listening on 127.0.0.1:10259
E0516 08:51:48.880559       1 shared_informer.go:316] unable to sync caches for client-ca::kube-system::extension-apiserver-authentication::client-ca-file
I0516 08:51:48.880706       1 configmap_cafile_content.go:210] "Shutting down controller" name="client-ca::kube-system::extension-apiserver-authentication::client-ca-file"
I0516 08:51:48.891024       1 leaderelection.go:250] attempting to acquire leader lease kube-system/kube-scheduler...
I0516 08:51:48.899706       1 server.go:238] "Requested to terminate, exiting"
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# kubectl get pods -n kube-system
E0516 10:59:35.135234    7927 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:59:35.137271    7927 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:59:35.138998    7927 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:59:35.140970    7927 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
E0516 10:59:35.142991    7927 memcache.go:265] "Unhandled Error" err="couldn't get current server API group list: Get \"https://192.168.72.148:6443/api?timeout=32s\": dial tcp 192.168.72.148:6443: connect: connection refused"
The connection to the server 192.168.72.148:6443 was refused - did you specify the right host or port?
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# 
root@Debian:~# sudo crictl --runtime-endpoint unix:///run/containerd/containerd.sock ps -a | grep kube | grep -v pause
09f91640808cf       a6946560b0b08       21 seconds ago       Running             kube-proxy                2                   d9b8b5396f2ea       kube-proxy-c7v7x
8c19e6f168770       c32cfb72baccb       35 seconds ago       Running             kube-controller-manager   11                  e004208ae6715       kube-controller-manager-debian
2edd89329ed1f       12675fc0a409d       59 seconds ago       Running             kube-scheduler            8                   44b2960de3175       kube-scheduler-debian
6050371dab3db       a6946560b0b08       About a minute ago   Exited              kube-proxy                1                   4ce0e39154f65       kube-proxy-c7v7x
4dadb4d9ea1c3       e60416bd78b65       2 minutes ago        Exited              kube-apiserver            8                   4691de9bf5bb8       kube-apiserver-debian
df4c04858bf62       c32cfb72baccb       4 minutes ago        Exited              kube-controller-manager   10                  e004208ae6715       kube-controller-manager-debian
0986b75774695       12675fc0a409d       8 minutes ago        Exited              kube-scheduler            7                   ecd62e9a857d5       kube-scheduler-debian
root@Debian:~# 
root@Debian:~# 
root@Debian:~# sudo crictl logs 4dadb4d9ea1c3  # ID de kube-apiserver (Exited)
WARN[0000] runtime connect using default endpoints: [unix:///var/run/dockershim.sock unix:///run/containerd/containerd.sock unix:///run/crio/crio.sock unix:///var/run/cri-dockerd.sock]. As the default settings are now deprecated, you should set the endpoint instead. 
ERRO[0000] validate service connection: validate CRI v1 runtime API for endpoint "unix:///var/run/dockershim.sock": rpc error: code = Unavailable desc = connection error: desc = "transport: Error while dialing: dial unix /var/run/dockershim.sock: connect: no such file or directory" 
I0516 08:57:19.958113       1 options.go:221] external host was not specified, using 192.168.72.148
I0516 08:57:19.959958       1 server.go:148] Version: v1.30.13
I0516 08:57:19.960093       1 server.go:150] "Golang settings" GOGC="" GOMAXPROCS="" GOTRACEBACK=""
I0516 08:57:20.585837       1 shared_informer.go:313] Waiting for caches to sync for node_authorizer
I0516 08:57:20.592425       1 shared_informer.go:313] Waiting for caches to sync for *generic.policySource[*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicy,*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicyBinding,k8s.io/apiserver/pkg/admission/plugin/policy/validating.Validator]
I0516 08:57:20.593842       1 plugins.go:157] Loaded 12 mutating admission controller(s) successfully in the following order: NamespaceLifecycle,LimitRanger,ServiceAccount,NodeRestriction,TaintNodesByCondition,Priority,DefaultTolerationSeconds,DefaultStorageClass,StorageObjectInUseProtection,RuntimeClass,DefaultIngressClass,MutatingAdmissionWebhook.
I0516 08:57:20.593987       1 plugins.go:160] Loaded 13 validating admission controller(s) successfully in the following order: LimitRanger,ServiceAccount,PodSecurity,Priority,PersistentVolumeClaimResize,RuntimeClass,CertificateApproval,CertificateSigning,ClusterTrustBundleAttest,CertificateSubjectRestriction,ValidatingAdmissionPolicy,ValidatingAdmissionWebhook,ResourceQuota.
I0516 08:57:20.594492       1 instance.go:299] Using reconciler: lease
I0516 08:57:20.623830       1 handler.go:286] Adding GroupVersion apiextensions.k8s.io v1 to ResourceManager
W0516 08:57:20.623927       1 genericapiserver.go:733] Skipping API apiextensions.k8s.io/v1beta1 because it has no resources.
I0516 08:57:20.800380       1 handler.go:286] Adding GroupVersion  v1 to ResourceManager
I0516 08:57:20.800790       1 instance.go:696] API group "internal.apiserver.k8s.io" is not enabled, skipping.
I0516 08:57:20.983826       1 instance.go:696] API group "storagemigration.k8s.io" is not enabled, skipping.
I0516 08:57:21.132060       1 instance.go:696] API group "resource.k8s.io" is not enabled, skipping.
I0516 08:57:21.140674       1 handler.go:286] Adding GroupVersion authentication.k8s.io v1 to ResourceManager
W0516 08:57:21.140731       1 genericapiserver.go:733] Skipping API authentication.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.140743       1 genericapiserver.go:733] Skipping API authentication.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.141293       1 handler.go:286] Adding GroupVersion authorization.k8s.io v1 to ResourceManager
W0516 08:57:21.141344       1 genericapiserver.go:733] Skipping API authorization.k8s.io/v1beta1 because it has no resources.
I0516 08:57:21.141967       1 handler.go:286] Adding GroupVersion autoscaling v2 to ResourceManager
I0516 08:57:21.142686       1 handler.go:286] Adding GroupVersion autoscaling v1 to ResourceManager
W0516 08:57:21.142732       1 genericapiserver.go:733] Skipping API autoscaling/v2beta1 because it has no resources.
W0516 08:57:21.142740       1 genericapiserver.go:733] Skipping API autoscaling/v2beta2 because it has no resources.
I0516 08:57:21.143734       1 handler.go:286] Adding GroupVersion batch v1 to ResourceManager
W0516 08:57:21.143785       1 genericapiserver.go:733] Skipping API batch/v1beta1 because it has no resources.
I0516 08:57:21.144989       1 handler.go:286] Adding GroupVersion certificates.k8s.io v1 to ResourceManager
W0516 08:57:21.145041       1 genericapiserver.go:733] Skipping API certificates.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.145051       1 genericapiserver.go:733] Skipping API certificates.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.145790       1 handler.go:286] Adding GroupVersion coordination.k8s.io v1 to ResourceManager
W0516 08:57:21.145841       1 genericapiserver.go:733] Skipping API coordination.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.146024       1 genericapiserver.go:733] Skipping API discovery.k8s.io/v1beta1 because it has no resources.
I0516 08:57:21.146669       1 handler.go:286] Adding GroupVersion discovery.k8s.io v1 to ResourceManager
I0516 08:57:21.149063       1 handler.go:286] Adding GroupVersion networking.k8s.io v1 to ResourceManager
W0516 08:57:21.149119       1 genericapiserver.go:733] Skipping API networking.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.149130       1 genericapiserver.go:733] Skipping API networking.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.149869       1 handler.go:286] Adding GroupVersion node.k8s.io v1 to ResourceManager
W0516 08:57:21.149895       1 genericapiserver.go:733] Skipping API node.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.149903       1 genericapiserver.go:733] Skipping API node.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.150951       1 handler.go:286] Adding GroupVersion policy v1 to ResourceManager
W0516 08:57:21.151007       1 genericapiserver.go:733] Skipping API policy/v1beta1 because it has no resources.
I0516 08:57:21.153019       1 handler.go:286] Adding GroupVersion rbac.authorization.k8s.io v1 to ResourceManager
W0516 08:57:21.153075       1 genericapiserver.go:733] Skipping API rbac.authorization.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.153087       1 genericapiserver.go:733] Skipping API rbac.authorization.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.153823       1 handler.go:286] Adding GroupVersion scheduling.k8s.io v1 to ResourceManager
W0516 08:57:21.153873       1 genericapiserver.go:733] Skipping API scheduling.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.153883       1 genericapiserver.go:733] Skipping API scheduling.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.156752       1 handler.go:286] Adding GroupVersion storage.k8s.io v1 to ResourceManager
W0516 08:57:21.156822       1 genericapiserver.go:733] Skipping API storage.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.156833       1 genericapiserver.go:733] Skipping API storage.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.158430       1 handler.go:286] Adding GroupVersion flowcontrol.apiserver.k8s.io v1 to ResourceManager
I0516 08:57:21.159795       1 handler.go:286] Adding GroupVersion flowcontrol.apiserver.k8s.io v1beta3 to ResourceManager
W0516 08:57:21.159849       1 genericapiserver.go:733] Skipping API flowcontrol.apiserver.k8s.io/v1beta2 because it has no resources.
W0516 08:57:21.159860       1 genericapiserver.go:733] Skipping API flowcontrol.apiserver.k8s.io/v1beta1 because it has no resources.
I0516 08:57:21.164310       1 handler.go:286] Adding GroupVersion apps v1 to ResourceManager
W0516 08:57:21.164367       1 genericapiserver.go:733] Skipping API apps/v1beta2 because it has no resources.
W0516 08:57:21.164376       1 genericapiserver.go:733] Skipping API apps/v1beta1 because it has no resources.
I0516 08:57:21.166539       1 handler.go:286] Adding GroupVersion admissionregistration.k8s.io v1 to ResourceManager
W0516 08:57:21.166593       1 genericapiserver.go:733] Skipping API admissionregistration.k8s.io/v1beta1 because it has no resources.
W0516 08:57:21.166605       1 genericapiserver.go:733] Skipping API admissionregistration.k8s.io/v1alpha1 because it has no resources.
I0516 08:57:21.167341       1 handler.go:286] Adding GroupVersion events.k8s.io v1 to ResourceManager
W0516 08:57:21.167399       1 genericapiserver.go:733] Skipping API events.k8s.io/v1beta1 because it has no resources.
I0516 08:57:21.192092       1 handler.go:286] Adding GroupVersion apiregistration.k8s.io v1 to ResourceManager
W0516 08:57:21.192117       1 genericapiserver.go:733] Skipping API apiregistration.k8s.io/v1beta1 because it has no resources.
I0516 08:57:21.603985       1 dynamic_cafile_content.go:157] "Starting controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:57:21.604364       1 dynamic_cafile_content.go:157] "Starting controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:57:21.604911       1 dynamic_serving_content.go:132] "Starting controller" name="serving-cert::/etc/kubernetes/pki/apiserver.crt::/etc/kubernetes/pki/apiserver.key"
I0516 08:57:21.604996       1 tlsconfig.go:240] "Starting DynamicServingCertificateController"
I0516 08:57:21.604937       1 secure_serving.go:213] Serving securely on [::]:6443
I0516 08:57:21.605804       1 controller.go:116] Starting legacy_token_tracking_controller
I0516 08:57:21.605904       1 shared_informer.go:313] Waiting for caches to sync for configmaps
I0516 08:57:21.606162       1 dynamic_serving_content.go:132] "Starting controller" name="aggregator-proxy-cert::/etc/kubernetes/pki/front-proxy-client.crt::/etc/kubernetes/pki/front-proxy-client.key"
I0516 08:57:21.606285       1 apiservice_controller.go:97] Starting APIServiceRegistrationController
I0516 08:57:21.606362       1 cache.go:32] Waiting for caches to sync for APIServiceRegistrationController controller
I0516 08:57:21.606591       1 customresource_discovery_controller.go:289] Starting DiscoveryController
I0516 08:57:21.606885       1 controller.go:78] Starting OpenAPI AggregationController
I0516 08:57:21.606990       1 gc_controller.go:78] Starting apiserver lease garbage collector
I0516 08:57:21.607485       1 controller.go:80] Starting OpenAPI V3 AggregationController
I0516 08:57:21.607788       1 system_namespaces_controller.go:67] Starting system namespaces controller
I0516 08:57:21.607976       1 cluster_authentication_trust_controller.go:440] Starting cluster_authentication_trust_controller controller
I0516 08:57:21.607983       1 shared_informer.go:313] Waiting for caches to sync for cluster_authentication_trust_controller
I0516 08:57:21.608060       1 available_controller.go:423] Starting AvailableConditionController
I0516 08:57:21.608067       1 cache.go:32] Waiting for caches to sync for AvailableConditionController controller
I0516 08:57:21.608088       1 aggregator.go:163] waiting for initial CRD sync...
I0516 08:57:21.608097       1 apf_controller.go:374] Starting API Priority and Fairness config controller
I0516 08:57:21.612194       1 controller.go:139] Starting OpenAPI controller
I0516 08:57:21.612340       1 controller.go:87] Starting OpenAPI V3 controller
I0516 08:57:21.612447       1 naming_controller.go:291] Starting NamingConditionController
I0516 08:57:21.612523       1 establishing_controller.go:76] Starting EstablishingController
I0516 08:57:21.612598       1 nonstructuralschema_controller.go:192] Starting NonStructuralSchemaConditionController
I0516 08:57:21.612696       1 apiapproval_controller.go:186] Starting KubernetesAPIApprovalPolicyConformantConditionController
I0516 08:57:21.612770       1 crd_finalizer.go:266] Starting CRDFinalizer
I0516 08:57:21.620803       1 dynamic_cafile_content.go:157] "Starting controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:57:21.621001       1 dynamic_cafile_content.go:157] "Starting controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:57:21.644941       1 crdregistration_controller.go:111] Starting crd-autoregister controller
I0516 08:57:21.645097       1 shared_informer.go:313] Waiting for caches to sync for crd-autoregister
I0516 08:57:21.685872       1 shared_informer.go:320] Caches are synced for node_authorizer
I0516 08:57:21.692973       1 shared_informer.go:320] Caches are synced for *generic.policySource[*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicy,*k8s.io/api/admissionregistration/v1.ValidatingAdmissionPolicyBinding,k8s.io/apiserver/pkg/admission/plugin/policy/validating.Validator]
I0516 08:57:21.693081       1 policy_source.go:224] refreshing policies
I0516 08:57:21.703537       1 controller.go:615] quota admission added evaluator for: leases.coordination.k8s.io
I0516 08:57:21.707004       1 shared_informer.go:320] Caches are synced for configmaps
I0516 08:57:21.707333       1 cache.go:39] Caches are synced for APIServiceRegistrationController controller
I0516 08:57:21.714609       1 apf_controller.go:379] Running API Priority and Fairness config worker
I0516 08:57:21.715003       1 apf_controller.go:382] Running API Priority and Fairness periodic rebalancing process
I0516 08:57:21.716060       1 shared_informer.go:320] Caches are synced for cluster_authentication_trust_controller
I0516 08:57:21.716072       1 handler_discovery.go:447] Starting ResourceDiscoveryManager
I0516 08:57:21.716093       1 cache.go:39] Caches are synced for AvailableConditionController controller
I0516 08:57:21.746328       1 shared_informer.go:320] Caches are synced for crd-autoregister
I0516 08:57:21.746402       1 aggregator.go:165] initial CRD sync complete...
I0516 08:57:21.746413       1 autoregister_controller.go:141] Starting autoregister controller
I0516 08:57:21.746422       1 cache.go:32] Waiting for caches to sync for autoregister controller
I0516 08:57:21.746430       1 cache.go:39] Caches are synced for autoregister controller
I0516 08:57:22.613178       1 storage_scheduling.go:111] all system priority classes are created successfully or already exist.
W0516 08:57:22.929680       1 lease.go:265] Resetting endpoints for master service "kubernetes" to [192.168.72.148]
I0516 08:57:22.930867       1 controller.go:615] quota admission added evaluator for: endpoints
I0516 08:57:22.936260       1 controller.go:615] quota admission added evaluator for: endpointslices.discovery.k8s.io
I0516 08:58:40.748153       1 controller.go:128] Shutting down kubernetes service endpoint reconciler
W0516 08:58:40.758482       1 lease.go:265] Resetting endpoints for master service "kubernetes" to []
I0516 08:58:40.774408       1 dynamic_cafile_content.go:171] "Shutting down controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:58:40.775814       1 dynamic_cafile_content.go:171] "Shutting down controller" name="request-header::/etc/kubernetes/pki/front-proxy-ca.crt"
I0516 08:58:40.776523       1 dynamic_cafile_content.go:171] "Shutting down controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:58:40.778065       1 dynamic_serving_content.go:146] "Shutting down controller" name="aggregator-proxy-cert::/etc/kubernetes/pki/front-proxy-client.crt::/etc/kubernetes/pki/front-proxy-client.key"
I0516 08:58:40.779276       1 object_count_tracker.go:151] "StorageObjectCountTracker pruner is exiting"
I0516 08:58:40.779797       1 storage_flowcontrol.go:187] APF bootstrap ensurer is exiting
I0516 08:58:40.779913       1 controller.go:86] Shutting down OpenAPI V3 AggregationController
I0516 08:58:40.780017       1 cluster_authentication_trust_controller.go:463] Shutting down cluster_authentication_trust_controller controller
I0516 08:58:40.780751       1 controller.go:84] Shutting down OpenAPI AggregationController
I0516 08:58:40.782642       1 secure_serving.go:258] Stopped listening on [::]:6443
I0516 08:58:40.783823       1 tlsconfig.go:255] "Shutting down DynamicServingCertificateController"
I0516 08:58:40.784822       1 dynamic_serving_content.go:146] "Shutting down controller" name="serving-cert::/etc/kubernetes/pki/apiserver.crt::/etc/kubernetes/pki/apiserver.key"
I0516 08:58:40.785048       1 autoregister_controller.go:165] Shutting down autoregister controller
I0516 08:58:40.785209       1 dynamic_cafile_content.go:171] "Shutting down controller" name="client-ca-bundle::/etc/kubernetes/pki/ca.crt"
I0516 08:58:40.791490       1 crdregistration_controller.go:142] Shutting down crd-autoregister controller
I0516 08:58:40.792226       1 available_controller.go:439] Shutting down AvailableConditionController
I0516 08:58:40.792283       1 system_namespaces_controller.go:77] Shutting down system namespaces controller
I0516 08:58:40.792354       1 apf_controller.go:386] Shutting down API Priority and Fairness config worker
I0516 08:58:40.792501       1 apiservice_controller.go:131] Shutting down APIServiceRegistrationController
I0516 08:58:40.795188       1 apiapproval_controller.go:198] Shutting down KubernetesAPIApprovalPolicyConformantConditionController
I0516 08:58:40.796734       1 nonstructuralschema_controller.go:204] Shutting down NonStructuralSchemaConditionController
I0516 08:58:40.796764       1 establishing_controller.go:87] Shutting down EstablishingController
I0516 08:58:40.797220       1 naming_controller.go:302] Shutting down NamingConditionController
I0516 08:58:40.798712       1 controller.go:167] Shutting down OpenAPI controller
I0516 08:58:40.798739       1 crd_finalizer.go:278] Shutting down CRDFinalizer
I0516 08:58:40.798835       1 controller.go:117] Shutting down OpenAPI V3 controller
I0516 08:58:40.799018       1 gc_controller.go:91] Shutting down apiserver lease garbage collector
I0516 08:58:40.799663       1 controller.go:129] Ending legacy_token_tracking_controller
I0516 08:58:40.799699       1 controller.go:130] Shutting down legacy_token_tracking_controller
I0516 08:58:40.799729       1 customresource_discovery_controller.go:325] Shutting down DiscoveryController
I0516 08:58:40.799790       1 controller.go:157] Shutting down quota evaluator
I0516 08:58:40.799805       1 controller.go:176] quota evaluator worker shutdown
I0516 08:58:40.800423       1 controller.go:176] quota evaluator worker shutdown
I0516 08:58:40.800748       1 controller.go:176] quota evaluator worker shutdown
I0516 08:58:40.800811       1 controller.go:176] quota evaluator worker shutdown
I0516 08:58:40.800876       1 controller.go:176] quota evaluator worker shutdown
 
root@Debian:~# 
root@Debian:~# sudo journalctl -u etcd --no-pager | tail -30
-- No entries --

root@Debian:~# 
root@Debian:~# sudo systemctl status etcd
Unit etcd.service could not be found.

root@Debian:~# 
root@Debian:~# sudo crictl --runtime-endpoint unix:///run/containerd/containerd.sock ps -a | grep etcd
8d6286a86534d       2e96e5913fc06       2 minutes ago        Running             etcd                      7                   2a215b02be2b7       etcd-debian
9153c00f1f522       2e96e5913fc06       11 minutes ago       Exited              etcd                      6                   7a2d031a9484f       etcd-debian

root@Debian:~# 
root@Debian:~# sudo crictl --runtime-endpoint unix:///run/containerd/containerd.sock ps -a | grep kube | grep -v pause
8627e2b70644d       a6946560b0b08       11 seconds ago       Running             kube-proxy                4                   6a1eb84f47393       kube-proxy-c7v7x
94e1cfa8a3e83       12675fc0a409d       About a minute ago   Exited              kube-scheduler            9                   27406bf414887       kube-scheduler-debian
173008d86faab       e60416bd78b65       About a minute ago   Running             kube-apiserver            9                   54564cc35a5b9       kube-apiserver-debian
5d0b65ad8a934       a6946560b0b08       2 minutes ago        Exited              kube-proxy                3                   f153d74ddc7e1       kube-proxy-c7v7x
8c19e6f168770       c32cfb72baccb       4 minutes ago        Exited              kube-controller-manager   11                  e004208ae6715       kube-controller-manager-debian
4dadb4d9ea1c3       e60416bd78b65       6 minutes ago        Exited              kube-apiserver            8                   4691de9bf5bb8       kube-apiserver-debian
 
root@Debian:~# 
root@Debian:~# sudo netstat -tulnp | grep 6443
tcp6       0      0 :::6443                 :::*                    LISTEN      8630/kube-apiserver 
root@Debian:~# 




















