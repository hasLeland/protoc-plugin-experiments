
PLUGIN=protoc-gen-unotest

INPUT=initial.go
OUTPUT=result.log

all: $(OUTPUT)

$(PLUGIN): $(INPUT)
	go build -o $@ $^

$(OUTPUT): $(PLUGIN)
	protoc -I/usr/local/include -I. -I.. --plugin=$(PLUGIN) --unotest_out=. service.proto

