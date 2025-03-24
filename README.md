Note: Right now there is no ip authorization on the stream server. Please do not post these links publicly

### RTMP live stream link: 
rtmp://192.168.0.89:1935/live/LARIXxiaoniao250

### HLS 60s delay link: 
http://192.168.0.89:8080/live/LARIXxiaoniao250.m3u8





*Container Restart*
~docker logs rtmp-server
~docker stop rtmp-server
~docker rm rtmp-server
~docker build -t my-nginx-rtmp .
~docker run -d -p 1935:1935 -p 8080:8080 --name rtmp-server my-nginx-rtmp
