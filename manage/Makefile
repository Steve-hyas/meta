BINARY=manage

run: deps build
	./$(BINARY)

releases: deps build
	./$(BINARY) releases

issues: deps build
	./$(BINARY) issues v0.16

build: clean $(BINARY)

clean:
	rm -rf $(BINARY)

$(BINARY):
	go build -o $(BINARY)

deps:
	go get -u gopkg.in/yaml.v2
	go get -u github.com/google/go-github/github

.PHONY: run deps clean build
