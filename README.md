docker-compose-efk
------------------

This project handle a orchestration of a `log` centralization using [Elaticsearch](https://www.elastic.co/) to persist data, [Fluentd](https://www.fluentd.org/) as data collection and [Kibana](https://www.elastic.co/products/kibana) to interact with the logs and [Nginx](https://nginx.org/) to be the reverse proxy.

By default, Kibana does not perform an authentication. To deal with this limitation we put a reverse proxy using nginx with `auth_basic_user_file` option to handle the authentication. The file `nginx/passwords/.httpasswd` contains the default login and password (admin/admin). If you want to change this, you can access [this](http://aspirine.org/htpasswd_en.html) website whom allows you to generate your own login and password. Feel free to handle your logs.

Usage
-----

You just have to run `docker-compose up -d` to orchestrate the project. Nginx is using the port `5601` of host to receive connections. Feel free to change this if you want to (line `6` of `docker-compose.yaml`).

What can I do with this?
------------------------

Everything you want. :) 

But log output of docker containers, log php requests, log {anything goes here}. In [this](https://www.fluentd.org/datasources) link you can find all datasources plugins to `fluentd`.

But you did not talk about {anything goes here}
-----------------------------------------------

Fell free to ask me anything [here](https://github.com/pedromazala/docker-compose-efk/issues)

Contributing
------------

Please help me :)
