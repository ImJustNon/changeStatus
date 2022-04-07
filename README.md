# changeStatus
changeStatus code 

- code 
```js
async function change_status(client) {
    try {
        client.user.setActivity(`${PREFIX}help | ${client.guilds.cache.size} เซิฟเวอร์`, { 
            type: "STREAMING", url: "https://www.twitch.tv/im_just_non",
            shardID: shard
        });
    } 
    catch (e) {
        client.user.setActivity(``, {
            type: "STREAMING", url: "https://www.twitch.tv/im_just_non",
            shardID: 0
        });
    }
}
module.exports = async bot => {
  change_status(bot);
    //loop through the status per each 10 minutes
    setInterval(() => {
        change_status(bot);
    }, 10 * 1000);
}
```
