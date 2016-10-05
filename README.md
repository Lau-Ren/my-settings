# my-shortcuts


##Windows
  **Bash**
  
    `
       #!/bin/bash

     # change to directory that contains arg
     gto() {
       RED='\033[0;31m'
       NC='\033[0m'
       GREEN='\033[0;32m'

       myDir=$1
       theDir=$(find -maxdepth 1 -type d -name "viz-"${myDir} | awk 'NR==1')
       if [ -d "${theDir}" ]
       then
           echo -e "${GREEN}${theDir} is a dir${NC}"
           cd ${theDir}
       else
           echo -e "${RED}$1 is not a dir${NC}"
       fi



     }

     # open current dir in webstorm
     wst() {
         /c/Program\ Files\ \(x86\)/JetBrains/WebStorm\ 2016.2.2/bin/WebStorm.exe $PWD/$1
     }

     # create and save new alias for last command. Alias name = first arg
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
     alias gcm="git commit -m"
     alias gco="git checkout"
     alias push="git push"


     alias ws='cd ~/LaurenProjects/Storm/'
     alias cl='clear'

     alias build= 'grunt build'
     alias serve='grunt serve'
     alias gbs='grunt build && grunt serve'

     alias demo='grunt build && grunt serve'

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
