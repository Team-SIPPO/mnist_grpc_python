# grpc on raspberry pi 4 

## make environments.
```
# create virtual env
python -m virtualenv venv
source ./venv/bin/activate

# install library
pip install grpcio
pip install grpcio-tools
```

## write proto, which is definition of interface.
see [hellowold.proto](./proto/hellowold.proto)


## generate code interface with helloworld.proto
```
python -m grpc_tools.protoc -I./proto --python_out=. --grpc_python_out=. ./proto/helloworld.proto
```

## generate programs
- server  
wirte code for server
- client  
write code for client

