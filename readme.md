
## Introduction  
  
Valet+ is a development environment for macOS. No Vagrant, no Docker, no `/etc/hosts` file.  
  
## Installation  

Install Homebrew:  
```bash  
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update && brew upgrade
```  
  
Install prerequisits:
```  
brew tap henkrehorst/php  
brew install composer  
brew install  
brew install valet-php@7.2  
brew link --force --overwrite valet-php@7.2  
```

Install valet-plus
```
composer global require techdivision/valet-plus   
grep -q 'export PATH="$PATH:$HOME/.composer/vendor/bin"' ~/.zshrc || echo 'export PATH="$PATH:$HOME/.composer/vendor/bin"' >> ~/.zshrc
```
> Reopen your terminal and go ahead with:
```
valet install  
valet elasticsearch install  
/usr/local/opt/elasticsearch@2.4/libexec/bin/plugin install analysis-phonetic  
/usr/local/opt/elasticsearch@2.4/libexec/bin/plugin install analysis-icu  
grep -q 'script.inline: on' /usr/local/opt/elasticsearch@2.4/libexec/config/elasticsearch.yml || echo "script.inline: on" >> /usr/local/opt/elasticsearch@2.4/libexec/config/elasticsearch.yml  
grep -q 'script.indexed: on' /usr/local/opt/elasticsearch@2.4/libexec/config/elasticsearch.yml || echo "script.indexed: on" >> /usr/local/opt/elasticsearch@2.4/libexec/config/elasticsearch.yml  
valet restart elasticsearch
```
## Usage
For further documentation goto [https://github.com/weprovide/valet-plus/blob/master/readme.md](https://github.com/weprovide/valet-plus/blob/master/readme.md)
