# rarity-levelup

Just a simple script to adventure and level up Rarity summoners  
[Rarity smart contract](https://ftmscan.com/address/0xce761d788df608bd21bdd59d6f4b54b2e27f25bb#code)  
[Intro Post from Andre Cronje](https://andrecronje.medium.com/loot-rarity-d341faa4485c)

## How to use

-   copy the `example.env` file to just `.env`
-   fill in the fields
-   add your summoner IDs to the `summoners.js` file
-   can run directly with `node run` or build a Docker image with `npm run build`
-   enjoy


## How to setup cron

`which node` -- Find Node Path

`crontab -e` in my case :

`0 0 * * * . ~/rarity-levelup/.env && cd ~/rarity-levelup && /root/.nvm/versions/node/v12.18.2/bin/node main.js $PRIVATE_KEY1 $SUMMONERS1 > ~/rarity-levelup/logs.txt 2>&1`

`1 0 * * * . ~/rarity-levelup/.env && cd ~/rarity-levelup && /root/.nvm/versions/node/v12.18.2/bin/node main.js $PRIVATE_KEY2 $SUMMONERS2 > ~/rarity-levelup/logs.txt 2>&1`

etc with any other: `node main.js [PRIVATE_KEY] [SUMMONERS]`