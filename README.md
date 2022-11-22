################ colored for bash ###############

#\u - user name
#\h - short hostname
#\W - current working dir
#\? - exit status of the command

_GREEN=$(tput setaf 2)
_BLUE=$(tput setaf 4)
_RED=$(tput setaf 1)
_RESET=$(tput sgr0)
_BOLD=$(tput bold)
export PS1="[${_RED}\u${_BLUE}@${_GREEN}\h${_RESET}:\w${_BOLD}]\$ ${_RESET}"
