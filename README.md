# my-shortcuts

## Other

 rdesktop.sh

```

#!/bin/bash
#open rdesktop with dimensions speficied, and create shared dir 
/usr/bin/rdesktop -a 16 -g 1366x708  -r disk:linux=/home/lauren/workspace/rdesk -u BIS2\\collsl 172.16.2.128

exit 0

```

## Windows
  **Bash**

  .bash_profile
  
```
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

   alias gs="git status"
   alias ga="git add"
   alias gb="git checkout -b"
   alias gd="git diff"
   alias gc="git commit"
   alias gcm="git commit -m"
   alias gco="git checkout"
   alias push="git push"
   alias pull="git pull"

   #change to alias ws='cd ~/workspace/'
   alias ws='cd ~/LaurenProjects/'
   alias storm="cd ~/LaurenProjects/storm/"
   alias cl='clear'

```

**Webstorm**


##Linux
 **Zsh**
 
 `
 ZSH_THEME="af-magic"
 `

**Sublime**


##Mac

 **Bash**
 
 **Sublime**
