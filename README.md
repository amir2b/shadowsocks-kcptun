# shadowsocks-kcptun
shadowsocks with kcptun by docker

## Setup
> git clone https://github.com/amir2b/shadowsocks-kcptun.git .  
> make env  
> make build  
> make start  
> make logs

## Config
shadowsocks:  
password=xxxxxxxxxx  
method=aes-256-gcm  
port=00000

Kcptun:  
key=xxxxxxxxxx  
mode=fast3  
sockbuf=16777217  
dscp=46  
autoexpire=900  
nocomp
