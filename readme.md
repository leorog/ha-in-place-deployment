# Running

haproxy: `haproxy -V -f haproxy.cfg`

copy http server template unit to `/etc/systemd/user`: `cp simple-http@.service /etc/systemd/user/`

watch haproxy frontend: `watch -n 0.2 curl -s localhost:4444`

trigger deploy: `ansible-playbook ha.yml --ask-become-pass`
