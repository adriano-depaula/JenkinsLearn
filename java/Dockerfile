# Imagem base para construir imagem do container
FROM debian

# Usado para executar comandos no container (quantos menos RUN melhor porque o container terá menocamadas. Sempre que possível concatene os comandos)
RUN apt-get update && apt-get install vim && apt-get clean

# Copia diretório ou arquivo de uma origem remota para dentro da imagem
ADD $PWD:/app /container

# Copia apenas diretórios e arquivo para dentro do container
COPY $PWD:/app /container

# Descrição para o container, nota de versão
LABEL Description="Primeiro Dockerfile"

# Permite o container executar um processo ou executável
ENTRYPOINT ["/usr/bin/apache2ctl"]

# É um parâmetro para o entryoit (principal processo do container)
CMD ["-D", "FOREGROUND"]

# Determina variáveis de ambiente no formato CHAVE="valor"
ENV NOME="Adriano de Paula"

# Expoẽ a porta do container
EXPOSE 80/tcp
EXPOSE 21/tcp
EXPOSE 20/udp

# Usuário default da imagem
USER usuario[:grupo]

# Diretório de trabalho do container (inicia o container dentro do diretório)
WORKDIR /usuario

# Cria um ponto de montagem entre o host docker e o container
VOLUME  /home/CONTAINERs/JAVA

# Executed as cmd /S /C echo hello
SHELL ["cmd", "/S", "/C"]
RUN echo hello