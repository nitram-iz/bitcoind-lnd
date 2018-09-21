## A Simple Bitcoind + LND setup
With inspiration from https://github.com/jamesob/docker-bitcoind and https://github.com/lightningnetwork/lnd/blob/master/Dockerfile

You'll need >200GB of storage just for the Bitcoin blockchain as of 9/20/2018.

* Edit `bitcoind/bitcoin.conf` and `lnd/lnd.conf` with your settings and just `docker-compose up -d` should work

* If you'd like to stop just one of the services (btc/lnd containers), use `docker-compose stop btc/lnd` and then use the command below to start it again

* If you've made changes to any of the files and need to rebuild just one of the containers, use `docker-compose up -d --build btc/lnd`

TODO:
* Figure out a way to keep the lncli wallet unlocked since when you `exec` (i.e. `docker exec -it lnd bash`) into the container and `lncli unlock` it (after creation), the bash process exits the container
