## Arbitrum Node Kurulum

## Minimum Sistem Gereksinimleri

**CPU:** 4 CPU

**RAM:** 8 GB

**SSD:** 200 GB


#### sunucumuzu güncelliyoruz
```
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install docker.io -y
```

#### gerekli klasör ve izinler
```
mkdir -p ~/data/arbitrum
```
```
chmod -fR 777 ~/data/arbitrum
```

#### Kurulum
```
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec --l1.url <Alchemykod> --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts=* --init.url="https://snapshot.arbitrum.io/mainnet/nitro.tar"

```


#### Güncel blok kontrolü
```
docker ps
```

```
docker logs -f <ConteinerID>
```

