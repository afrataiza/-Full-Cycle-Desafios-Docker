# Etapa 1: Usar uma imagem base oficial do Go para compilar o binário
FROM golang:1.19-alpine AS builder

# Definir o diretório de trabalho dentro do container
WORKDIR /app

# Copiar o arquivo Go para o diretório de trabalho
COPY main.go .

# Compilar o binário Go de forma estática (necessário para scratch)
RUN go mod init app && \
    CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -ldflags="-s -w" -o app .

# Etapa 2: Usar a imagem 'scratch' para reduzir o tamanho da imagem
FROM scratch

# Copiar o binário do builder para a nova imagem
COPY --from=builder /app/app /app/app

# Definir o ponto de entrada da aplicação
ENTRYPOINT ["/app/app"]