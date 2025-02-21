#### Setup for kubectl alias

```bash
alias k='kubectl'
alias kn='kubectl config set-context --current --namespace'
alias kgp='kubectl get pod'
alias kgs='kubectl get service'
alias kl='kubectl logs'
alias ke='kubectl exec -it'
complete -F __start_kubectl k
export GPG_TTY=$(tty)
```



#### Setup for colorful bash

Add this line at the end of ~/.bashrc

```bash
PS1='\[\033[1;36m\]\u\[\033[1;31m\]@\[\033[1;32m\]\h:\[\033[1;35m\]\w\[\033[1;31m\]\$\[\033[0m\] '
```

Save the file and:

```bash
source ~/.bashrc
```

