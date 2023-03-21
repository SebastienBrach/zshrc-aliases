```
##### PATH #####
export PATH=/Applications/MAMP/bin/php/php8.0.8/bin:$PATH
export ZSH="$HOME/.oh-my-zsh"
##### PATH #####


##### ZSH CONFIG (iTerm2) #####
ZSH_DISABLE_COMPFIX="true"
ZSH_THEME="af-magic"  # See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
plugins=(git)  # Example format: plugins=(rails git textmate ruby lighthouse)
source $ZSH/oh-my-zsh.sh
##### ZSH CONFIG (iTerm2) #####


##### ALIASES #####

### DOCKER ###
alias ps="docker ps -a"
alias volumemac="docker run -it --privileged --rm --name MAC_VOLUMES --pid=host debian nsenter -t 1 -m -u -n -i sh"
alias composebuildup="docker compose build && docker compose up -d --remove-orphans"
alias composeup="docker compose up -d --remove-orphans"
alias composedown="docker compose down"
alias prune="docker builder prune -f"
alias hardprune="docker compose down && docker system prune -af --volumes && docker builder prune -f"
alias rmcontainer="docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)"
dockerexec () {docker exec -it -u root "$@" bash;}
dockerexecpull () {docker exec -it -u root "$@" bash -c "git pull";}
dockerstats () {docker stats --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}\t{{.MemPerc}}\t{{.PIDs}}" "$@";}
### DOCKER ###

### USEFULL ###
alias htmldir="cd /var/www/html/"
alias desktopdir="/Users/$USER/Desktop"
diskusage () {du -shc "$@"| sort -h;}
### USEFULL ###

### ZSHRC FILE ###
alias nanozshrc="nano ~/.zshrc"
alias sourcezshrc="source ~/.zshrc"
alias catzshrc="cat ~/.zshrc"
### ZSHRC FILE ###

### IP ###
alias myip="curl http://ipecho.net/plain; echo"
alias mylocalip="ifconfig | grep 192"
### IP ###
