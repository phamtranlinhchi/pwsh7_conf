#### Setup for kubectl alias

Thêm vào /etc/profile để áp dụng với tất cả các user

Còn áp dụng với mỗi user hiện tại thì ~/.bashrc

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

```bash
source /etc/profile # (hoặc ~/.bashrc)
```



#### Setup for colorful bash

Add this line at the end of ~/.bashrc (/etc/profile)

```bash
PS1='\[\033[1;36m\]\u\[\033[1;31m\]@\[\033[1;32m\]\h:\[\033[1;35m\]\w\[\033[1;31m\]\$\[\033[0m\] '
```

Save the file and:

```bash
source ~/.bashrc # (/etc/profile)
```



#### Setup for colorful kubectl

Need brew for installation

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

test -d ~/.linuxbrew && eval "$(~/.linuxbrew/bin/brew shellenv)"
test -d /home/linuxbrew/.linuxbrew && eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.bashrc
```



Install kubecolor as alternative for kubectl

```bas
brew install hidetatz/tap/kubecolor
```

```bash	
alias k='kubecolor'
alias kn='kubecolor config set-context --current --namespace'
alias kgp='kubecolor get pod'
alias kgs='kubecolor get service'
alias kl='kubecolor logs'
alias ke='kubecolor exec -it'
complete -F __start_kubectl k
export GPG_TTY=$(tty)
```

Thêm vào /etc/profile để áp dụng với tất cả các user

Còn áp dụng với mỗi user hiện tại thì ~/.bashrc

```bash
source /etc/profile # (hoặc ~/.bashrc)
```

