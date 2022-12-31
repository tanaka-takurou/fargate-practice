FROM golang:latest
WORKDIR /app
COPY main.go /app/
COPY go.mod /app/
RUN go mod tidy

CMD [ "go", "run", "main.go" ]
