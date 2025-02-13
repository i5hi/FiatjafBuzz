# FiatjafBuzz

Install [noscl](https://github.com/fiatjaf/noscl)

Create keys for the bot (private first)

```
noscl key-gen
```

Get the public key:

```
noscl public
```

The public key of this bot is: 

hex: `61c17ee154594cf8aea19d3195001bae83baa74d11f784e6a8288113505f5dc9`
OR
npub: `npub1v8qhac25t9x03t4pn5ce2qqm46pm4f6dz8mcfe4g9zq3x5zlthyslyjr0k`

Add a relay:
```
noscl relay add wss://relay.damus.io
noscl relay add wss://nostr-pub.wellorder.net
```

Edit cronjobs:

```bash
crontab -e
```

Add the following job:

```
0 6 */2 * * [ $(date +\%u) -ge 6 ] && noscl publish "gfy fiatjaf" || noscl publish "GM fiatjaf"
```
