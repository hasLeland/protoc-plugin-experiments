
PLUGIN=protoc-gen-unotest
OUTPUT=result.log

all: result.log

$(PLUGIN): initial.go
	go build -o $@ $^

$(RESULT): $(PLUGIN)
	protoc -I/usr/local/include -I. -I.. --plugin=$(PLUGIN) --unotest_out=. service.proto

