# Checkmate
Your lightwalletd checkpoint mate. 

## Requirements
* grpcurl
* python 3

## Usage 

Example: call checkmate and generate checkpoint json files starting from block 1346316 until latest height with a 10000 blocks interval.

```` bash
python3 checkmate.py lightwalletd.com:9067 --start-height 1346316 --to-json
````

## Generated Output
checkmate dumps the output of GetTreeState into a json file like this one

**Example of 1430000.json**
```` json
{
  "network": "main",
  "height": "1430000",
  "hash": "00000000018865a445b8677f1227b1ab1194a790997e5b5c7419364b8b2c5ed9",
  "time": 1634635150,
  "tree": "01c5acc382555e72951ceb578a4b3ee586fbdc5f38b813e926ebe3d02180fe036f00130001897617c720372627310c50150d0a32a4c2940d946f9c6097f89c10d5dcdcd31001b9d91186dbc4b7de2fc90923da31d28691b1ff09bc6c22fa285b2b2514613e1b0001d3fec2031df5b05cfe5ae60da0251c497b82c00109ec5995487dfba3dff5400300000123d1c05283a0a805397b6a27a62d1ad51921f7761d2a6bd0462780a411c6c95301a5bbeff16030f5314d7cd7f83c258068b35ba5dc52152423bced5c117a98011c01bc0d4b825129e3910eb822375b4467f1486ce9fafd82c90f744287f0d481545501bd6d46ab0ad0be85a948886aacad2279e0c3b073108a6c4cc093dd60b323454100000001034afd8677bf7cb50ebd76fdc07fb5a94224fd468b233a20fde901263e422815000001ecceb776c043662617d62646ee60985521b61c0b860f3a9731e66ef74ed8fb320118f64df255c9c43db708255e7bf6bffd481e5c2f38fe9ed8f3d189f7f9cf2644"
}
````
## Manual
```` python
def usage():
    return """
Checkmate: your GetTreeState checkpoint mate. 

checkmate.py LIGHTWALLETD_HOST --start-height HEIGHT [--interval BLOCK_INTERVAL] [--to-json]
--start-height the height you want to start pulling tree states from
--to-json exports the outputs to [height].json files instead of just stdout
"""
````

## Contributing
Contributions are totally welcome! This was coded in about an hour by someone that barely knows any Python. 

