## install openebs and start cStor
### install by helm
```bash
helm repo add openebs https://openebs.github.io/charts
helm repo update
helm install openebs --namespace openebs openebs/openebs --set cstor.enabled=true --create-namespace
```
### Prerequisites
the host of store storage location must install `iscsid` service before you use openebs
```bash
sudo apt install open-iscsi

sudo systemctl start iscsid
sudo systemctl enable iscsid

```
