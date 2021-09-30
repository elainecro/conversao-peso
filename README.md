# conversao-peso

# Criar imagem com Dockerfile
docker build -t conversao-peso -f Dockerfile .

# Ver imagem criada
docker images
ou
docker image ls

# Criar container com a imagem criada
docker create --name conversao-peso-kubedev conversao-peso
# Rodar container
docker start conversao-peso-kubedev


ou

# Criar e rodar container
docker run -d -p 5000:80 --name conversao-peso-kubedev conversao-peso