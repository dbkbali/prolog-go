## this application uses Protobuf and as a result you will need to install the appropriate protobuf release from https://github.com/protocolbuffers/protobuf/releases


```bash
wget https://github.com/protocolbuffers/protobuf/releases/download/v3.19.1/protoc-3.19.1-osx-x86_64.zip

unzip protoc-3.19.1-osx-x86_64.zip -d /usr/local/protobuf

echo 'export PATH="$PATH:/usr/local/protobuf/bin"' >> ~/.zshenv
```

- You will also need to install the appropriate runtime for your machine

#### Install Protobuf Runtime
```bash
go get google.golang.org/protobuf/...@v1.25.0

```

#### Compile Protobuf

```go

protoc api/v1/*.proto \
			--go_out=. \
			--go_opt=paths=source_relative \
			--proto_path=. 

```
