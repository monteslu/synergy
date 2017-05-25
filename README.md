# Citrix Synergy  - Simply Serve


## Hello World

[https://pagenodes.com](https://pagenodes.com)


* send message to uuid:
`d678af0a-aa81-4c17-9ed4-aeb5f1dc2ffc`


## Web Bluetooth

![screenshot](BLE_diagram.png)


## Bot Assembly
* connect motors
* connect pins
* connect battery pack
* secure the pieces
* customize

![screenshot](wiring.png)


## Bot connecting.

* service Id: `bada5555-e91f-1337-a49b-8675309fb099`

* digital Characteristic `2a56`

* analog Characteristic `2a58`


## directional movement

* Right wheel forward:
digital: `[8,1]` and `[7,0]`

* Left wheel forward:
digital: `[5,1]` and `[4,0]`


* Right wheel reverse:
digital: `[8,0]` and `[7,1]`

* Left wheel reverse:
digital: `[5,0]` and `[4,1]`


## speed

* Right wheel full speed:
analog: `[9,255]`

* Left wheel full speed:
analog: `[3,255]`


* Right wheel STOP:
analog: `[9,0]`

* Left wheel STOP:
analog: `[3,0]`


## last resort...

If you're having trouble getting things going, you can import this flow into pagenodes:

```javascript
[{"id":"x6p92bcijfg","type":"bluetooth out","z":"a755f2bb.9212b","name":"digital..","characteristicId":"2a56","bleServiceId":"bada5555-e91f-1337-a49b-8675309fb099","x":787,"y":108,"wires":[]},{"id":"TbiRghiJCPM","type":"bluetooth out","z":"a755f2bb.9212b","name":"analog..","characteristicId":"2a58","bleServiceId":"bada5555-e91f-1337-a49b-8675309fb099","x":673,"y":541,"wires":[]},{"id":"SqyjePHweJ8","type":"iot buttons","z":"a755f2bb.9212b","x":88,"y":81,"wires":[["hes-x-slZ6M"]]},{"id":"hes-x-slZ6M","type":"switch","z":"a755f2bb.9212b","name":"","property":"payload","propertyType":"msg","rules":[{"t":"eq","v":"3","vt":"num"},{"t":"eq","v":"4","vt":"num"},{"t":"eq","v":"2","vt":"num"},{"t":"eq","v":"6","vt":"num"},{"t":"eq","v":"5","vt":"num"},{"t":"eq","v":"7","vt":"num"},{"t":"eq","v":"8","vt":"num"}],"checkall":"true","outputs":7,"x":115,"y":235,"wires":[["nzbjd6fbVq8","6P3wqYuj5OE","F7tuXNHq8MM","BaQfra5Ywec"],["YSIsHQIMedc","lp0cAs5p9vg","ydjN1Tz6pls","cs7jTZsLzTU"],["nzbjd6fbVq8","6P3wqYuj5OE","ydjN1Tz6pls","cs7jTZsLzTU"],["F7tuXNHq8MM","BaQfra5Ywec","YSIsHQIMedc","lp0cAs5p9vg"],["NWN0VETOu2A","4Am4kkku1dA"],["NrCF6f_PRdk","MTWnzLkw04c"],["ZcZ7Y6RkQ34","HfipJnpWhRs"]]},{"id":"NWN0VETOu2A","type":"change","z":"a755f2bb.9212b","name":"stop left","rules":[{"t":"set","p":"payload","pt":"msg","to":"[3,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":260,"y":466,"wires":[["TbiRghiJCPM"]]},{"id":"4Am4kkku1dA","type":"change","z":"a755f2bb.9212b","name":"stop right","rules":[{"t":"set","p":"payload","pt":"msg","to":"[9,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":297,"y":432,"wires":[["TbiRghiJCPM"]]},{"id":"MTWnzLkw04c","type":"change","z":"a755f2bb.9212b","name":"med left","rules":[{"t":"set","p":"payload","pt":"msg","to":"[3,127]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":223,"y":546,"wires":[["TbiRghiJCPM"]]},{"id":"NrCF6f_PRdk","type":"change","z":"a755f2bb.9212b","name":"med right","rules":[{"t":"set","p":"payload","pt":"msg","to":"[9,127]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":242,"y":510,"wires":[["TbiRghiJCPM"]]},{"id":"ZcZ7Y6RkQ34","type":"change","z":"a755f2bb.9212b","name":"high left","rules":[{"t":"set","p":"payload","pt":"msg","to":"[3,255]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":203,"y":626,"wires":[["TbiRghiJCPM"]]},{"id":"HfipJnpWhRs","type":"change","z":"a755f2bb.9212b","name":"high right","rules":[{"t":"set","p":"payload","pt":"msg","to":"[9,255]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":200,"y":589,"wires":[["TbiRghiJCPM"]]},{"id":"6P3wqYuj5OE","type":"change","z":"a755f2bb.9212b","name":"forward right 2","rules":[{"t":"set","p":"payload","pt":"msg","to":"[7,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":428,"y":65,"wires":[["x6p92bcijfg"]]},{"id":"nzbjd6fbVq8","type":"change","z":"a755f2bb.9212b","name":"forward right 1","rules":[{"t":"set","p":"payload","pt":"msg","to":"[8,1]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":426,"y":29,"wires":[["x6p92bcijfg"]]},{"id":"BaQfra5Ywec","type":"change","z":"a755f2bb.9212b","name":"forward left 2","rules":[{"t":"set","p":"payload","pt":"msg","to":"[4,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":428,"y":146,"wires":[["x6p92bcijfg"]]},{"id":"F7tuXNHq8MM","type":"change","z":"a755f2bb.9212b","name":"forward left 1","rules":[{"t":"set","p":"payload","pt":"msg","to":"[5,1]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":424,"y":112,"wires":[["x6p92bcijfg"]]},{"id":"lp0cAs5p9vg","type":"change","z":"a755f2bb.9212b","name":"reverse right 2","rules":[{"t":"set","p":"payload","pt":"msg","to":"[7,1]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":483,"y":280,"wires":[["x6p92bcijfg"]]},{"id":"YSIsHQIMedc","type":"change","z":"a755f2bb.9212b","name":"reverse right 1","rules":[{"t":"set","p":"payload","pt":"msg","to":"[8,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":481,"y":244,"wires":[["x6p92bcijfg"]]},{"id":"cs7jTZsLzTU","type":"change","z":"a755f2bb.9212b","name":"reverse left 2","rules":[{"t":"set","p":"payload","pt":"msg","to":"[4,1]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":483,"y":361,"wires":[["x6p92bcijfg"]]},{"id":"ydjN1Tz6pls","type":"change","z":"a755f2bb.9212b","name":"reverse left 1","rules":[{"t":"set","p":"payload","pt":"msg","to":"[5,0]","tot":"json"}],"action":"","property":"","from":"","to":"","reg":false,"x":479,"y":327,"wires":[["x6p92bcijfg"]]}]
```
