## Ubuntu Terminal (Tmux+Powerline+Vim)

##### 1. Powerline configuration
```bash
sudo apt install python-pip -y
sudo pip install powerline-status
sudo apt install vim -y
vim ~/.bashrc 
vim ~/.vimrc
```

###### 1.1 Install powerline fonts
```bash
sudo apt install fonts-powerline -y
```

###### 1.2 Append this to your ~/.bashrc file
```bash
#PowerLine
if [ -f /usr/local/lib/python2.7/dist-packages/powerline/bindings/bash/powerline.sh ]; then
        source /usr/local/lib/python2.7/dist-packages/powerline/bindings/bash/powerline.sh
fi
```
###### 1.3 Append this to your ~/.vimrc file
```bash
" PowerLine
set rtp+=/usr/local/lib/python2.7/dist-packages/powerline/bindings/vim/
set laststatus=2
set t_Co=256
```

###### 1.4 Append this to your ~/.tmux.conf file
```bash
set -g default-terminal "screen-256color"
run-shell 'powerline-config tmux setup'
```
