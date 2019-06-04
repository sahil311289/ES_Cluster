1. Start master node with overlay network

docker-compose up


2. Start an nginx service so that other nodes can view network

docker service create --name my-nginx --network es_cluster_with_overlay_backend --replicas 3 --publish published=8080,target=80 nginx:latest


3. Start nodes on other hosts with overlay network

docker-compose up



Happy searching :)
