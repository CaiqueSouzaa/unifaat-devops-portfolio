# Aula 01 — Fundamentos de Git e Docker

## O que aprendi

- Com o Git é possível aplicar o gerenciamento de versões de nosso projeto, adicionar comentários (commits) em nossos "salvamentos" e criar branch onde podemos implementar novas funcionalidades sem que afetem, em caso de falhas, a branch principal.
- O Docker elimina o famoso "na minha máquina funciona", é possível subir e inicializar um projeto com simples comandos e é possível criar "imagens/snapshots" de determinadas versões de nosso projeto.

## Comandos Git praticados

``` bash
"git init" para inicializar o Git em nosso projeto;
"git add ." para adicionar nossos arquivos no gerenciamento de arquivos do git para ele poder versionar;
"git commit -m "feat: este é um commit"" comando este para finalizar o nosso commit e registrar no histórico de vida de nosso projeto.
```

## Comandos Docker praticados

```bash
"docker build -t portfolio-aula01:1.0 ." usado para gerar a imagem do projeto;
"docker run -d --name portfolio-test -p 3000:3000 portfolio-aula01:1.0" para criar um container usando a imagem criada anteriormente;
"docker stop portfolio-test" para encerrar o container criado.
````

## Como executar este container

```bash
cd aula-01/app
docker build -t portfolio-aula01:1.0 .
docker run -d -p 3000:3000 portfolio-aula01:1.0
curl http://localhost:3000
