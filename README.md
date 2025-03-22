# Kafka Certification Bootcamp

Create a container to perform the activities in the cours

Create sealed secret to store in source control

```bash
~/Desktop/odysseyvc/repos/tools/sealsecret.sh keep/kafka-certification-aws-creds.yaml bastion-host

kubectl create secret generic kafka-certification-ssh-key --from-file=/Users/godfreytutu/.ssh/ubuntu-vm-local-user2 --dry-run=client -o yaml > keep/kafka-certification-ssh-key.yaml

# Open the secret file and change the key to "id_rsa"

~/Desktop/odysseyvc/repos/tools/sealsecret.sh keep/kafka-certification-ssh-key.yaml bastion-host
```

```bash
kubectl -n dev-tutug apply -f bastion-host
```

# Clean up

```bash
kubectl -n dev-tutug delete -f bastion-host
```
