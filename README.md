<h1 align="center"> Taiko Katla Alpha-6 Node </h1>


<h1 align="center"> Donanım </h1>

> Hetzner'i 3$ sunucuyu kullandım. [Link](https://github.com/ruesandora/Hetzner)

```
2 CPU 
4 GB RAM 
50 GB SSD 
```

<h1 align="center"> Kurulum </h1>

```sh
# Komutları tek tek girelim.
sudo apt update 
sudo apt upgrade
apt install docker-compose
apt install git
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin

# Repoyu klonlayıp dizine girelim.
git clone https://github.com/taikoxyz/simple-taiko-node.git
cd simple-taiko-node

#Ayrı screende çalıştıracağız:
screen -S taiko
```

<h1 align="center"> Dikkat edilmesi gereken nokta </h1>

> Blockpi hesabımdan taiko için bir dApp oluşturdum.
>> Bu dApp, Ethereum - Holesky zinciri olacak.
>>>[Link](https://blockpi.io/)
![image](https://github.com/ruesandora/taiko-node/assets/101149671/30056a24-6387-4f62-9665-e5a72853d7bb)

> Daha sonra View key kısmından key bilgilerimi aldım:

![image](https://github.com/ruesandora/taiko-node/assets/101149671/74c21010-a0e0-446c-a45f-d1b200ddded4)

> Altta ki komutlar ile `.env` içine girdim.

```sh
cd simple-taiko-node
cp .env.sample .env
nano .env
```

> L1_ENDPOINT_HTTP= Bu kısıma Blockpi'den aldığınız HTTPS adresini yazıyorsunuz

> L1_ENDPOINT_WS= Bu kısıma Blockpi'den aldığınız WSS adresini yazıyorsunuz

> L1_PROVER_PRIVATE_KEY= Bu kısıma Metamask Private keyinizi yapıştırıyorsunuz

> CTRL X Y ile çıkıyoruz.

![image](https://github.com/ruesandora/taiko-node/assets/101149671/fd9a8b10-5da1-4598-9f0e-4dec72c8b835)

<h1 align="center"> Node'u çalıştırma </h1>

> Faucet Linki [Holesky](https://faucetlink.to/holesky)
 
``` 
# Node'u çalıştırın
docker compose up
```
![image](https://github.com/ruesandora/taiko-node/assets/101149671/a7f550ea-e83a-4b66-904f-ea44a731bf41)


