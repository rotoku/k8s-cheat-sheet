# K8S

## Instalando o kubectl

```
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version --client
```

## Alias
[Enable Shell Autocompletion](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#enable-shell-autocompletion)
```
sudo apt update -y
sudo apt install bash-completion -y
echo 'source <(kubectl completion bash)' >>~/.bashrc

## General Aliases
alias k="kubectl"
alias ks="kubectl -n kube-system"
alias kdesc="kubectl describe"

echo 'complete -o default -F __start_kubectl k' >>~/.bashrc

## Create Resources
alias kcf="kubectl create -f"
alias kaf="kubectl apply -f"

## Get Resources
alias kgn="kubectl get nodes"
alias kgp="kubectl get pods"
alias kgpa="kubectl get pods --all-namespaces"
alias kgs="kubectl get services"
alias kgd="kubectl get deployments"

## Delete Resources
alias kd="kubectl delete"
alias kdp="kubectl delete pods"
alias kds="kubectl delete services"
alias kdd="kubectl delete deployments"
alias kdn="kubectl delete namespaces"
```