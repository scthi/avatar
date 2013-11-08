Avatar
=================

Small utility providing user avatar pics in various sizes with good caching.

Setup
-------------------------------------------------

* install node.js and npm
* go to project folder and run `npm install`
* `.bin/avatar <port>` (starts the server, port is optional)

Note: installation can be a bit tricky, since the required lib (node-canvas) depends on a lib call "cairo", which must be installed properly on the system. (See: https://github.com/LearnBoost/node-canvas#installation)

Usage
-------------------------------------------------

Query params:

* `t` - user name or email of the user
* `h` - hash to identify the user (optional, if not set t is used)
* `u` - url of possible user pic (optional)
* `c` - force a color (optional)
* `s` - preferred size of pic (optional, default is 150)

Caching
-------------------------------------------------

* `max-age` is set to `7 days`
* `etag` is the current date

Production
-------------------------------------------------

endpoint: http://getcatchapp.com:8888/
cloudfront: http://d35va0jwnexy3a.cloudfront.net
on: web.hojoki.com
folder: /var/avatar
user: bitbucket

Timm has a cronjob running, which auto restarts the avatar process on the server.