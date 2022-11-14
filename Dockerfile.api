FROM golang:1.19.3-alpine
WORKDIR /server

COPY go.mod ./
COPY go.sum ./

RUN go mod download

COPY main.go ./
COPY routes ./
COPY utils ./

RUN go build -o /build

EXPOSE 8080
CMD [ "/build" ]
