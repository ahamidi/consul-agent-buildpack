## Consul Agent Heroku Buildpack

[Consul](https://www.consul.io)

### TODO
- [ ] Add shell script to simplify launching
- [ ] Read in config file
- [ ] See if we can *pass through* call (so that only 1 dyno is needed)
- [ ] Cache downloaded zip file

### Usage

* Add the buildpack to your app:
    
    `heroku buildpacks:add https://github.com/ahamidi/consul-agent-buildpack`
* Start Consul dyno:
    
    ```
    # Procfile
    consul: bin/consul agent -data-dir /tmp/consul -join=$CONSUL_SERVER
    ```
