# Linked List Implementation in Go

This repository contains a simple implementation of a linked list in Go. It supports basic operations such as insert, find, get, and remove. Each of these operations is accompanied by comprehensive unit tests to ensure the correctness and stability of the implementation.

## Getting Started

### Prerequisites

Ensure you have Go installed on your system. You can verify this by running `go version` in your command line. If Go is not installed, you can download and install it from the [official Go website](https://golang.org/dl/).

### Running the Code

To run the main application which demonstrates some linked list operations, use the following command:

```bash
go run linkedList.go

```
Run Server on port 8080

**Inset Value:**

```bash
curl -X POST -H "Content-Type: application/json" -d '{"index": 0, "value": 10}' http://localhost:8080/v1/insert
```

**Get a Value:**

```bash
curl -X GET "http://localhost:8080/v1/get/1"
```

**Remove Value:**

```bash
curl -X GET "http://localhost:8080/v1/find/10"
```

**Find Value:**

```bash
curl -X DELETE "http://localhost:8080/v1/remove/1"
```

**Items List:**

```bash
curl -X GET "http://localhost:8080/v1/list"
```



### Running All Tests

```bash
go test ./linkedlist/ -v

```
### Run property-based test

```bash
go test ./linkedlist/ -v -run 'TestLinkedListPropertiesQuick'
```

# Run unit tests
```bash
go test -run TestLinkedListInsert ./linkedlist/ -v
```

#### Running Specific Function Tests

```bash
go test -run TestLinkedListInsert ./linkedlist/ -v

go test -run TestLinkedListFind ./linkedlist/ -v

go test -run TestLinkedListFind ./linkedlist/ -v

go test -run TestLinkedListRemove ./linkedlist/ -v

```

### Hurl tests
Run your app and then replace your port with the 8080 below and then run the following command

```bash
hurl hurl-tests/tests.hurl --test --variable host=localhost:8080
```

### Api v2
We are using echo for creating the v2 of the apis

**Inset Value:**

```bash
curl -X POST -H "Content-Type: application/json" -d '{}' http://localhost:8080/v2/numbers/0/10
```

**Get a Value By Index:**

```bash
curl -X GET "http://localhost:8080/v2/numbers/index/1"
```

**Find Value:**

```bash
curl -X GET "http://localhost:8080/v2/numbers/value/10"
```

**Remove Value:**

```bash
curl -X DELETE "http://localhost:8080/v2/numbers/1"
```

### Config
you can add configs in config/config.yaml file and then for hot reloading you can send a SIGHUP to the app after changing the config file

### Start the Docker Compose Services

```bash
docker-compose up -d
```
Open your browser and go to `http://localhost:3000` to access the Grafana web interface. 