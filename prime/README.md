# Annotations


## Passo a passo para restaurar BD OrçaFascio Prime no mongo

- No terminal, dentro do diretório onde encontra-se o backup rode o comando seguinte:

```
mongo
```

- Feito isso, para visualizar as bases de dados ativas, vamos inserir o seguinte comando no terminal:

```
show databases()
```

- E vamos "usar" a base de dados que queremos restaurar, com o seguinte comando:

```
use [nome_database]
use gryfus
```

- Agora, antes de restaurar o backup mais atual para a base de dados vamos remover os dados já existentes com o seguinte comando:

```
db.dropDatabase()
```

- Feito isso, podemos sair do mongo clicando em `CTRL + D`;

- O próximo passo é restaurar o backup de fato, para dentro da base de dados usando o comando a seguir:

```
mongorestore --gzip --db gryfus gryfus
```