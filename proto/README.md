# OpenCue Protobuf Files

These files define the high-level data types in OpenCue, used across components.

To use them, they must first be compiled into the native language of the component.

## Cuebot

Gradle automatically compiles these proto files, no further action is needed.

## RQD

To generate:

```
python -m grpc_tools.protoc -I=. --python_out=../rqd/rqd/compiled_proto --grpc_python_out=../rqd/rqd/compiled_proto ./*.proto
```

## pycue

To generate:

```
python -m grpc_tools.protoc -I=. --python_out=../pycue/opencue/compiled_proto --grpc_python_out=../pycue/opencue/compiled_proto ./*.proto
```

