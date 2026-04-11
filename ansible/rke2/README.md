Role: https://github.com/lablabs/ansible-role-rke2
```sh
ansible-galaxy role install lablabs.rke2
```


```sh
ansible-playbook -i hosts.ini deploy-rke2.yml -Ku koax --ask-become-pass
```

Inital ARGOCD PW
```sh
kubectl get secret argocd-initial-admin-secret -n argocd -o jsonpath="{.data.password}" | base64 --decode && echo
```


```sh
kubectl run -it --rm --image=massenz/dnsutils:2.4.0 dnsutils -- /bin/bash
```