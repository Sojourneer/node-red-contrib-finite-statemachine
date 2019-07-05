# NODE RED STATEMACHINE

A finite state machine implementation for node red. Displays also a graphical representation of the state machine.

![node-settings](/Users/lutz/Projects/node-red-contrib-statemachine/images/node-settings.png)

## Install in node

### Inside Node-red

* TODO

### From Terminal

* go in node-red install folder, in os x its usually: `~/.node-red`
* run `npm install git+https://github.com/lutzer/node-red-contrib-statemachine.git`

## Usage

Check node-reds info panel to see how to use the state machine

### Example Flow

```javascript
{
  "state": {
    "status": "IDLE",
    "data" : { "x": 5 }
  },
  "transitions": {
    "IDLE": {
      "run": "RUNNING"
    },
    "RUNNING": {
      "stop": "IDLE",
			"set": "RUNNING"
​   }
  }
}
```

![flow](/Users/lutz/Projects/node-red-contrib-statemachine/images/flow.png)



### Feedback Flow

Set finite state machine definiton to:

```javascript
{
  "state": {
    "status": "IDLE",
    "data" : { "x": 5 }
  },
  "transitions": {
    "IDLE": {
      "run": "RUNNING"
    },
    "RUNNING": {
      "stop": "IDLE"
    }
  }
}
```

![node-settings](/Users/lutz/Projects/node-red-contrib-statemachine/images/node-settings.png

![flow-feedback](/Users/lutz/Projects/node-red-contrib-statemachine/images/flow-feedback.png)

## Development

* run `npm install`
* install grunt `npm install -g grunt-cli`
* build with `npm run build`
