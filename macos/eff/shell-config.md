### shell配置文件(bashrc|zshrc)
```shell
# 色彩配置
#color{{{
autoload colors
colors

for color in RED GREEN YELLOW BLUE MAGENTA CYAN WHITE; do
eval _$color='%{$terminfo[bold]$fg[${(L)color}]%}'
eval $color='%{$fg[${(L)color}]%}'
(( count = $count + 1 ))
done
FINISH="%{$terminfo[sgr0]%}"
#}}}

# 提示符配置
RPROMPT=$(echo "$RED%D %T$FINISH")
PROMPT=$(echo "$CYAN%n@$GREEN%/$_YELLOW>$FINISH ")

# 常用命令简化
alias g='git'
alias gs='git status'
alias ga='git add'
alias gc='git commit'
alias gb='git branch'
alias gco='git checkout'
alias grb='git rebase'

alias ll='ls -al'

# 环境变量设置
export PATH=$PATH:~/.bin

# 命令执行
source ~/.nvm/nvm.sh
nvm use v5.4.1 > /dev/null
```
