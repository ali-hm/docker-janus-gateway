# Janus gateway in a Docker Container

Run janus gateway configurable using environment variables.

```
docker run --rm \
 -e GATEWAY_IP=<Your server IP Address> \
 -e STUN_SERVER=stun.l.google.com \
 -e STUN_PORT=19302 \
 -e WEBSOCKETS_ENABLED=true \
 -e ADMIN_HTTP_ENABLED=true \
 -e RTP_PORT_RANGE=10000-10099 \
 -p 8088:8088 \
 -p 8188:8188 \
 -p 7188:7188 \
 -p 7088:7088 \
 -p 10000-10099:10000-10099/udp \
 -d --name janus-webrtc alihamidi/janus-gateway 
 ```