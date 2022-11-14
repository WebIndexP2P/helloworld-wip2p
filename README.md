# helloworld-libwip2p

This is a demo project with the bare minimum code to connect to a wip2p node, fetch and publish data.

The source code is commented and there is logging at important steps commented out if you want to inspect the data structures in use.

This will not output anything to the browser, open the developer tools and monitor the console output for output.

## Wip2p node

This demo project assumes a locally running wip2p node on localhost is accessible. You can download wip2p-go at http://wip2p.com

The easiest option is to run a new private tree like so:
`./wip2p-go -new` or `./wip2p-go -new -db helloworld.db`


## Steps to run :
1. Clone this repo
2. Run `gx i` to install the two dependencies (will require IPFS or attempt to use public gateway)
3. Manually open the `index.html` in a browser and open the dev tools

## What's going on

* The browser will generate a new ethereum account in browser.
* It will attempt to connect to the locally running wip2p node
* The wip2p node will add the browser account as the default root account
* The browser will request the /myApp namespace but it wont exist
* The browser will create a new dataset and save it to /myApp and publish it
* Subsequent reloads of the browser will fetch the same dataset and then overwrite it with a new instance of the same data.
