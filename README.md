################ colored for bash ###############

#\u - user name
#\h - short hostname
#\W - current working dir
#\? - exit status of the command

#Stable
_BASE_HEAD_STYLE='\[\033[0;'
_BASE_HEAD_BOLD_STYLE='\[\033[1;'
_BASE_TAIL_STYLE='m\]'
_YELLOW="${_BASE_HEAD_STYLE}33${_BASE_TAIL_STYLE}"
_BLUE="${_BASE_HEAD_STYLE}94${_BASE_TAIL_STYLE}"
_GREEN="${_BASE_HEAD_STYLE}32${_BASE_TAIL_STYLE}"
_CYAN="${_BASE_HEAD_BOLD_STYLE}36${_BASE_TAIL_STYLE}"
_MAGENTA="${_BASE_HEAD_BOLD_STYLE}35${_BASE_TAIL_STYLE}"
_RESET="\[\033[00m\]"
PS1="${_YELLOW}[\d \t] ${debian_chroot:+($debian_chroot)}${_MAGENTA}\u${_BLUE}@${_GREEN}\h${_RESET}:${_CYAN}\w${_GREEN}\$ ${_RESET}"

#In-trouble in breakline
_YELLOW=$(tput setaf 3)
_CYAN=$(tput setaf 6)
_GREEN=$(tput setaf 2)
_BLUE=$(tput setaf 4)
_RED=$(tput setaf 1)
_RESET=$(tput sgr0)
_BOLD=$(tput bold)
export PS1="${_YELLOW}[\d \t] ${_RESET}${_BOLD}<${_RESET}${_RED}\u${_BLUE}@${_GREEN}\h${_RESET}:${_CYAN}${_BOLD}\w${_RESET}${_BOLD} />${_RESET}${_GREEN}\$ ${_RESET}"

