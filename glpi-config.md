# Configurando GLPI com docker

É necessário ter certeza que o docker está instalado em sua máquina.

## Baixando as imagens

Para baixar e configuarar a imagem do mysql: 

```bash
sudo docker run --name mysql -e MYSQL_ROOT_PASSWORD=diouxx -e MYSQL_DATABASE=glpidb -e MYSQL_USER=glpi_user -e MYSQL_PASSWORD=glpi -d mysql:5.7.23
```

Para baixar e configurar a imagem do glpi:

```bash
sudo docker run --name glpi --link mysql:mysql -p 80:80 -d diouxx/glpi
```

## Acessando a interface do GLPI:

Após baixado e configurado as imagens e tornado elas em containers, a interface do GLPI estará disponível para acesso através do [localhost:80](http://localhost:80)

- escolha o idioma

- escolha instalar (se necessário)

- continuar

- acesso: 
    - mysql
    - glpi_user
    - mysql

- escolha o glpidb

Para ter acesso ao software utilize as credenciais:

- `usuário`: glpi
- `senha`: glpi

## Configurando os itens

### Ativos:

<img src="imgs/GLPI - Computadores - -1 - Google Chrome_003.png"
     alt="Adicionando o fabricante do computador:"
     style="float: left; margin: 10px;" />

<img src="imgs/GLPI - Computadores - 1 - Google Chrome_005.png"
     alt="Adicionando um computador como ativo:"
     style="float: left; margin: 10px;" />

### Chamada:

<img src="imgs/GLPI - Novo chamado - Google Chrome_006.png"
     alt="Adicionando uma chamada:"
     style="float: left; margin: 10px;" />

### Regra:

<img src="imgs/GLPI - Listas negras - -1 - Google Chrome_007.png"
     alt="Adicionando uma regra"
     style="float: left; margin: 10px;" />


### Grupo:

<img src="imgs/GLPI - Grupos - 1 - Google Chrome_011.png"
     alt="Adicionando um grupo"
     style="float: left; margin: 10px;" />


### Entidade:

<img src="imgs/GLPI - Entidade - 1 - Google Chrome_009.png"
     alt="Adicinando uma entidade"
     style="float: left; margin: 10px;" />

### Usuário:

<img src="imgs/GLPI - Usuários - Google Chrome_010.png"
     alt="Adicionando um usuário"
     style="float: left; margin: 10px;" />