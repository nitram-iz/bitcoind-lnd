## Bitcoind + LND
With inspiration from https://github.com/jamesob/docker-bitcoind

* Edit bitcoind/bitcoin.conf and lnd/lnd.conf with your settings and just `docker-compose up -d` should work. If you've made changes to any of the files and need to rebuild just one of the containers, use `docker-compose up -d --build btc/lnd`.

* If you'd like to stop just one of the services (btc/lnd containers), use `docker-compose stop btc/lnd`
