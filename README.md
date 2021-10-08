```shell
git clone  ssh://git@bitbucket.alfa.local:29418/hitk8s/kubespray.git
cd ./kubespray
git checkout 7a033a1d555e18f04c8dde7b75a0270c5289eeda
docker build -t kubespray .
```

```shell
git clone ssh://git@bitbucket.alfa.local:29418/hitk8s/kubespray_inventory.git
cd ./kubespray_inventory
docker run -ti -v $HOME/.ssh/id_rsa:/root/.ssh/id_rsa -v $HOME/projects/kubespray-inventory:/kubespray/inventory quay.io/kubespray/kubespray:v2.17.0 bash
```

```shell
ansible all -i inventory/k8s-test3/hosts.yaml --user=mesos --become --become-user=root -m ping
ansible-playbook -i inventory/k8s-test3/hosts.yaml --user=mesos --become --become-user=root cluster.yml
```
# kubespray-inventory
# kubespray-inventory
