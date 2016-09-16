# my-shortcuts


##Windows
  **Bash**
  
    `
    #!/bin/bash
    
    wst() {
        /c/Program\ Files\ \(x86\)/JetBrains/WebStorm\ 2016.2.2/bin/WebStorm.exe $PWD/$1
    }
    
    new-alias() {
      local last_command=$(echo `history |tail -n2 |head -n1` | sed 's/[0-9]* //')
      echo alias $1="'""$last_command""'" >> ~/.bash_profile
      . ~/.bash_profile
    }
    
    export PATH="$PATH:/c/Python27"
    
    alias ws="cd LaurenProjects/Storm/"
    alias gs="git status"
    alias ga="git add"
    alias gb="git branch"
    alias gd="git diff"
    alias gc="git commit"
    alias gco="git checkout"
  
  alias ws='cd ~/LaurenProjects/Storm/'
  `
*Webstorm**




##Linux
 **Zsh**
 `
 ZSH_THEME="af-magic"
 `
 **Sublime**


##Mac
 **Bash**
 **Sublime**
