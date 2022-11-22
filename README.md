################ colored for bash ###############

#\u - user name
#\h - short hostname
#\W - current working dir
#\? - exit status of the command

_YELLOW=$(tput setaf 3)
_CYAN=$(tput setaf 6)
_GREEN=$(tput setaf 2)
_BLUE=$(tput setaf 4)
_RED=$(tput setaf 1)
_RESET=$(tput sgr0)
_BOLD=$(tput bold)
export PS1="${_YELLOW}[\d \t] ${_RESET}${_BOLD}<${_RESET}${_RED}\u${_BLUE}@${_GREEN}\h${_RESET}:${_CYAN}${_BOLD}\w${_RESET}${_BOLD} />${_RESET}${_GREEN}\$ ${_RESET}"

