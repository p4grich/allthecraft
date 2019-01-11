FROM anapsix/alpine-java
RUN mkdir -p /opt/minecraft/server/run.sh 
COPY run.sh white-list.txt ops.txt eula.txt server.jar /opt/minecraft/server/
CMD ["bash", "/opt/minecraft/server/run.sh"]

