# Socks
Python's low-level network module (socket)

run docker images (with tags!):
docker run  --name="server" --env LISTEN_HOST="127.0.0.1" --env LISTEN_PORT="5555" --net=host -d server


docker run --name="client" --env SEND_HOST="localhost" --env SEND_PORT="5555" --net=host -d client


or


docker network create --driver bridge sample


docker run  --name="server" --env LISTEN_HOST="0.0.0.0" --env LISTEN_PORT="5555" --network=sample -d server


docker run --name="client" --env SEND_HOST="server" --env SEND_PORT="5555" --network=sample -d client
