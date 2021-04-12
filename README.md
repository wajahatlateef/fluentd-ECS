# fluentd-ECS
Default-Port 24224

Add elasticSearch URL/IP in fluentd.conf

Build Fluentd image: docker build -t <Fluentd-Image-Name> .
  
  
RUN Fluentd container: docker run -d -p 24224:24224 -p 24224:24224/udp <FLuentd-Image-Name>

Build your image where you want to parse logs using fluentd


docker run -d --rm --log-driver=fluentd --log-opt tag="docker" --log-opt fluentd-address=localhost:24224  <Image name>

