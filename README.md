#### Note
1. Thêm các setup bên dưới vào /etc/profile để áp dụng với tất cả các user
Còn chỉ muốn áp dụng với user hiện tại thì ~/.bashrc
=> Sau khi thêm các lệnh setup chỉ cần `source ~/.bashrc` vì trong ~/.bashrc đã có phần tải các setup trong /etc/profile

2. File `profile` trong repo này đã có hết các setup bên dưới 

3. File `settings.json` là file JSON setting của powershell7, thêm các shortcut keys.

#### Setup for colorful bash

```bash
PS1='\[\033[1;36m\]\u\[\033[1;31m\]@\[\033[1;32m\]\h:\[\033[1;35m\]\w\[\033[1;31m\]\$\[\033[0m\] '
```

#### Setup alias for colorful kubectl

```bash
apt install kubecolor 
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

#### Setup alias for non-colorful kubectl 

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


#### Other Setup
```bash	
alias l='ls -lh'
alias find='find . -name '
alias ..='cd ..'
alias ...='cd ../..'
```
