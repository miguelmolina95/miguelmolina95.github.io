Here is part of my .bash_profile

```bash
export PS1="\[\033[1;32m\]\u\[\033[0m\]:\[\033[1;34m\]\W\[\033[0m\]$ "

# Full look at the directory
alias ll="ls -lhaG"

# Changing dirs
alias ..="cd .."
alias ...="cd ../.."
alias ....="cd ../../.."
alias .....="cd ../../../.."

# Some handy stuff
alias c="clear"
alias numFiles="echo $(ls -1 | wc -l)"
alias copypath='pwd|pbcopy'

# Process
alias ps="ps -ax"

# lock computer
alias lock='/System/Library/CoreServices/"Menu Extras"/User.menu/Contents/Resources/CGSession -suspend'

# refresh shell
alias reload_bash='source ~/.bash_profile'

# Directories made easy
function mkd() {
    mkdir -p "$@" && cd "$@"
}

# One command to git them all
function gmit() {
	git pull && git add -A && git commit -m "$@" && git push
}

```
