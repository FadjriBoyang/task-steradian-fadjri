# task-challenge
1. Challenge Docker
   * Disini saya men deploy container postgresql, apache php, nginx, dan golang menggunakan docker compose.
   * Untuk deploy golang saya melakukan clone dari https://github.com/olliefr/docker-gs-ping-roach, lalu build image melalui dockerfile pada directory golang/docker-gs-ping
     dan membuat image dengan tag goexamplev1 dan expose port 8081:8080 yang digunakan pada file docker-compose.yml.
   * Untuk menghubungkan konfigurasi apache php pada port 8080 agar dapat diakses melalui nginx pada port 80 saya menggunakan reverse proxy dengan file default.conf pada
     directory nginx-conf.
2. Challenge Kubernetes
   * Disini saya menggunakan minikube sebagai cluster kubernetes
   * File untuk membuat pod berada pada directory kubernetes/pods file berbentuk yaml
   * File Nginx deployment terdapat pada directory kubernetes/deployment, dengan 3 replicaset
   * File Nginx service terdapat pada directory kubernetes/service, service digunakan sebagai routing trrafic untuk pods dengan label app: nginx
   * File Nginx ingress terdapat pada directory kubernetes/ingress, nginx-ingress mengarahkan lalu lintas HTTP dengan host "localhost" dan path "/" ke layanan backend nginx-service pada port 80
3. Challenge ELK (elastic logstash kibana)
   * Deploy ELK diatas docker menggunakan docker-compose.yml pada folder ELK_docker, dan submit data pada folder logstash_ingest_data
   * referensi: https://www.elastic.co/blog/getting-started-with-the-elastic-stack-and-docker-compose
   * Disini saya membuat cluster minikube baru dengan profile elk, dan deploy ELK diatas kubernetes dengan file yaml pada folder ELK_kubernetes
   * Submit data samples
   * referensi: https://dev.to/sagary2j/elk-stack-deployment-using-minikube-single-node-architecture-16cl

