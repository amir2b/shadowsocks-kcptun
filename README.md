# shadowsocks-kcptun
shadowsocks with kcptun by docker

## Setup:
> git clone https://github.com/amir2b/shadowsocks-kcptun.git .  
> make env  
> make build  
> make start  
> make logs

## Command:
> make down

> make restart

## Shadowsocks environment:
PASSWORD=xxxxxxxxxx  
METHOD=aes-256-gcm  

port=29900

## Kcptun environment:
MODE=fast3  
SOCKBUF=16777217  
DSCP=46  

key=xxxxxxxxxx  
nocomp
