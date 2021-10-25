# docker-mariadb-ssh-tunnel-example

```shell
sudo lsof -iTCP -sTCP:LISTEN -n -P
```

```shell
ssh -i erc-key root@91.200.42.185 -L 3317:localhost:3306 -N
```

Host mysql-tunnel # You can use any name
    HostName ssh-tunnel.corporate.tld # Tunnel
    IdentityFile ~/.ssh/id_rsa # Private key location
    User cagatay.guertuerk # Username to connect to SSH service
    ForwardAgent yes
    TCPKeepAlive yes
    ConnectTimeout 5
    ServerAliveCountMax 10
    ServerAliveInterval 15