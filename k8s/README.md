# K8S

## Alias
[Enable Shell Autocompletion](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#enable-shell-autocompletion)
```
sudo apt update -y
sudo apt install bash-completion -y
echo 'source <(kubectl completion bash)' >>~/.bashrc
echo 'alias k=kubectl' >>~/.bashrc
echo 'complete -o default -F __start_kubectl k' >>~/.bashrc

echo 'alias ks=kubectl -n kube-system' >>~/.bashrc
echo 'alias kdesc=kubectl describe' >>~/.bashrc
```