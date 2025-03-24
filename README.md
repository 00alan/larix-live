Note: Right now there is no ip authorization on the stream server. Please do not post these links publicly

### RTMP live stream link: 
rtmp://192.168.0.89:1935/live/LARIXxiaoniao250

### HLS 60s delay link: 
http://192.168.0.89:8080/live/LARIXxiaoniao250.m3u8




The configured 60-second playlist window is an upper bound on how many seconds of segments the server keeps available. The actual latency each viewer sees depends on how their HLS player starts playback (usually after 2–3 segments). Hence for live viewers a real-world delay of ~25–30 seconds is common with 6-second segments.


*Container Restart*
~docker logs rtmp-server
~docker stop rtmp-server
~docker rm rtmp-server
~docker build -t my-nginx-rtmp .
~docker run -d -p 1935:1935 -p 8080:8080 --name rtmp-server my-nginx-rtmp
