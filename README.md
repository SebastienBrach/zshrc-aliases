```
##### ZSH CONFIG (iTerm2) #####
ZSH_DISABLE_COMPFIX="true"
ZSH_THEME="af-magic"  # See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
plugins=(git)  # Example format: plugins=(rails git textmate ruby lighthouse)
source $ZSH/oh-my-zsh.sh
##### ZSH CONFIG (iTerm2) #####


##### PATH #####
export PATH=/Applications/MAMP/bin/php/php7.4.21/bin:$PATH
export ZSH="$HOME/.oh-my-zsh"
##### PATH #####


##### ALIASES #####

### DOCKER ###
alias dockervolumesmac="docker run -it --privileged --rm --name MAC_VOLUMES --pid=host debian nsenter -t 1 -m -u -n -i sh"
alias composebuildup="docker-compose build && docker-compose up -d --remove-orphans"
alias composeup="docker-compose up -d --remove-orphans"
alias prune="docker builder prune -f"
alias hardprune="docker-compose down && docker system prune -af --volumes && docker builder prune -f"
dockerexec () {docker exec -it -u root "$@" bash;}
containergitpull () {docker exec -it -u root "$@" bash -c "git pull";}
### DOCKER ###

### ZSHRC FILE ###
alias nanozshrc="nano ~/.zshrc"
alias sourcezshrc="source ~/.zshrc"
### ZSHRC FILE ###

alias myip="curl http://ipecho.net/plain; echo"

##### ALIASES #####
```
