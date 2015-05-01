# WorkingWithDocker

1) http://blog.sequenceiq.com/blog/2014/12/04/multinode-ambari-1-7-0/

2) http://blog.sequenceiq.com/blog/2014/05/26/ambari-shell/

3) increase docker vm disk size https://docs.docker.com/articles/b2d_volume_resize/

3) increase container sizing https://github.com/boot2docker/boot2docker-cli

docker pull sequenceiq/ambari:2.0.0

curl -Lo .amb https://raw.githubusercontent.com/sequenceiq/docker-ambari/2.0.0/ambari-functions && . .amb

amb-start-cluster 3

docker inspect --format='{{.NetworkSettings.IPAddress}}' amb0

docker run -i --rm sequenceiq/ambari-shell --ambari.host=172.17.0.1 --ambari.port=8080

ambari-shell> blueprint defaults

ambari-shell> blueprint list

ambari-shell> cluster build --blueprint multi-node-hdfs-yarn

ambari-shell> cluster autoAssign

ambari-shell> cluster create
