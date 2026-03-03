FROM golang:1.22-alpine

WORKDIR /app

COPY app.go .

RUN apk upgrade --no-cache && apk add --no-cache curl

EXPOSE 80

CMD ["go", "run", "app.go"]