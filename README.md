# Elasticsearch

### Instalar o Elasticsearch no Kubernetes:

- `git clone git@github.com:diegofnunesbr/elasticsearch.git`
- `cd elasticsearch`
- `helm install --create-namespace elasticsearch -n elasticsearch .`

### Configurar o Elasticsearch no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') elasticsearch.local"`

### Remover o Elasticsearch no Kubernetes:

- `helm uninstall elasticsearch -n elasticsearch`
