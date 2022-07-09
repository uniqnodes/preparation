# Install required software packages  
`sudo apt-get install git curl build-essential make jq -y`  

# Setup Go  
`curl https://dl.google.com/go/go1.18.3.linux-amd64.tar.gz | sudo tar -C/usr/local -zxvf -`  
```
cat <<'EOF' >>$HOME/.profile
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GO111MODULE=on
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
EOF
```
`source $HOME/.profile`  
`go version`    
