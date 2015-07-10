# golang-shoutbox

### Installation

Install go and Setup a GOPATH and go basic framework
Download the mgo drivers to your gopath
- go get gopkg.in/mgo.v2

Download the golang-shoutbox
- go get github.com/pblaas/golang-shoutbox

Build the go code by entering the golang-shoutbox and typing
- go build

### Defaults

By default the go app will be listening on port 3005.
It will use MongoDB on localhost without credentials using DB: mgodb and collection shouts.

The wordcloud is creating by a mapreduce script that needs to be run e.g in a cron.
You can find the mapreduce.js script in the mongodb subdir of the app.

### Running the application

Start the app by typing 
- ./golang-shoutbox

### Generating the wordcloud

- $MONGODBPATH/mongo localhost/mgodb $GOPATH/src/github.com/pblaas/golang-shoutbox/mongodb/mapreduce.js

