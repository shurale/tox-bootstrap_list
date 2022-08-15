# Tox DHT bootstrap servers list

Actual official list of tox DHT bootstrap servers can be downloaded by command

```
wget https://nodes.tox.chat/json
wget -O nodes.json https://nodes.tox.chat/json
```

Downloaded list may be converted from json into C syntax by @jq@:

```
jq '.nodes[]|[.public_key,.ipv4,.ipv6,.port]' < nodes.json |sed -e 's/\[/\{/' -e 's/]/},/' > temp.c
```

