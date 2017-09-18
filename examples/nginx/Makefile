TARGET ?= nginx-example
.PHONY: build run

run: build
	docker run -it --rm -p 8080:80 $(TARGET)

build:
	docker build -t $(TARGET) .

