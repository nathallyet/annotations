# Mongodb


## Passo a passo para restaurar BD OrçaFascio no mongo

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
use orcafascio
```

- Agora, antes de restaurar o backup mais atual para a base de dados vamos remover os dados já existentes com o seguinte comando:

```
db.dropDatabase()
```

- Feito isso, podemos sair do mongo clicando em `CTRL + D`;

- O próximo passo é restaurar o backup de fato, para dentro da base de dados usando o comando a seguir:

```
mongorestore --gzip --db orcafascio orcafascio
```

- E como a OrçaFascio contém duas pastas de backup, para restaurar a outra pasta(orc_db) basta renomear ela para `orcafascio` com o seguinte comando:

```
mv orc_db orcafascio
```

- E depois é só rodar o comando novamente:

```
mongorestore --gzip --db orcafascio orcafascio
```
