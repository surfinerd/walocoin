# Minado con CPU

Se debe usar un minero de otra criptomoneda que está habilitada para el uso de lo necesario.
Paso previo, debes haber creado un nodo y tener billetera, ya que los datos necesarios son:

1. IP del nodo. El puerto necesario es el 9772/TCP del protocolo RPC

2. Nombre de usuario: Definido en el archivo walocoin.conf en la directiva **rpcuser=**

3. Clave del usuario: Definido en el archivo walocoin.conf en la directiva **rpcpassword=**

4. La dirección de tu billetera en formato bech32, es decir, debe comenzar con wlc
 

## Ubuntu 18.04
```bash
sudo apt-get install -y \
build-essential libssl-dev libcurl4-openssl-dev libjansson-dev libgmp-dev automake zlib1g-dev && \
git clone https://github.com/cryptozeny/cpuminer-opt-sugarchain.git && \
cd cpuminer-opt-sugarchain && \
./build-yespower.sh 
```

Luego se debe ejecutar de la siguiente forma:
```bash
./cpuminer -a scrypt -o http://IP_DEL_NODO:9772 -u ususario_del_walocoin.conf  -p password_del_walocoin.conf --coinbase-addr=TU_BILLETERA_BECH32 -D --no-stratum --no-longpoll
```

## Windows 

Descargar el minero desde la siguiente URL  https://github.com/cryptozeny/cpuminer-opt-sugarchain/releases/download/v3.8.8.1.7rc1/cpuminer-opt-sugarchain-v3.8.8.1.7-w64.zip

Luego se debe ejecutar de la siguiente forma:
```cmd
cpuminer.exe -a scrypt -o http://IP_DEL_NODO:9772 -u usuario_del_walocoin.conf  -p password_del_walocoin.conf --coinbase-addr=TU_BILLETERA_BECH32 -D --no-stratum --no-longpoll
```



# Minado con GPU 
### WIP - Necesitamos tu ayuda:
El minero por GPU debe cumplir 3 condiciones:

1. Soportar el algo scrypt

2. Soportar GetBlockTemplate o GBT

3. Direcciones segwit bech32

 
