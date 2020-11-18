# Installation
## install homebrew(software manager on mac)
```sh
cd ~
#install homebrew to your mac
mkdir homebrew && 
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
#test your homebrew
brew --help
```
![Screen Shot 2020-11-19 at 1.52.52 AM](https://github.com/JY29/some_thing/raw/main/Screen%20Shot%202020-11-19%20at%201.52.52%20AM.png)

### solution for problem your may meet
curl: (7) Failed to connect to raw.githubusercontent.com port 443: Connection refused
```sh
# add them into the end of /etc/hosts
199.232.68.133 raw.githubusercontent.com
199.232.68.133 user-images.githubusercontent.com
199.232.68.133 avatars2.githubusercontent.com
199.232.68.133 avatars1.githubusercontent.com
```

## acceleration for home brew in the mainland
```sh
#1. 替换 / 还原 brew.git 仓库地址
# 替换成阿里巴巴的 brew.git 仓库地址: 

cd "$(brew --repo)" 
git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git 

#======================================================= # 
#还原为官方提供的 brew.git 仓库地址 
#cd "$(brew --repo)" 
#git remote set-url origin https://github.com/Homebrew/brew.git
 
#2. 替换 / 还原 homebrew-core.git 仓库地址
# 替换成阿里巴巴的 homebrew-core.git 仓库地址: 
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core" 
git remote set-url origin https://mirrors.aliyun.com/homebrew/homebrew-core.git 
#======================================================= # 
#还原为官方提供的 homebrew-core.git 仓库地址 
#cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core" 
#git remote set-url origin https://github.com/Homebrew/homebrew-#core.git
 
#3. 替换 / 还原 homebrew-bottles 访问地址
#判断自己正在使用的shell
echo $SHELL
#BASH 终端操作方式
# 替换 homebrew-bottles 访问 URL: 
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.aliyun.com/homebrew/homebrew-bottles' >> ~/.bash_profile 
source ~/.bash_profile 
#ZSH 终端操作方式
# 替换 homebrew-bottles 访问 URL: 
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.aliyun.com/homebrew/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc
#======================================================= # 
#还原为官方提供的 homebrew-bottles 
#访问地址 vi ~/.bash_profile 
# 然后，删除 HOMEBREW_BOTTLE_DOMAIN 这一行配置 
#source ~/.bash_profile
#访问地址 vi ~/.zshrc 
# 然后，删除 HOMEBREW_BOTTLE_DOMAIN 这一行配置 
#source ~/.zshrc
```

## install python3
```sh
brew install python3
```
![Screen%20Shot%202020-11-19%20at%205.44.39%20AM](https://github.com/JY29/some_thing/raw/main/Screen%20Shot%202020-11-19%20at%205.44.39%20AM.png)
