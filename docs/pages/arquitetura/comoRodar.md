# <center> Como rodar o Jobz

<div align="justify">

## 1. Introdução
Esse documento tem como objetivo mostrar como rodar o Jobz localmente.

## 2. Pré requisitos:

Docker => 20.10.12

Docker compose => 1.29.2

### 3. Passo a passo
1. Clone o [Jobz Backend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd) ou [Jobz Backend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd).

```
git clone https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd.git
```
ou

```
git clone https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackendEnd.git
```

2. Entre na pasta /deploy.

3. Rodar o projeto
```
make run
```
[Acesso ao Jobz](localhost:3000) - localhost:3000
  
4. Parar o projeto.
```
make stop
```
## 3. Informações Complementares

Existe automação para criação da imagem docker dentro do github para o [frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/master/.github/workflows/build.yml) e [backend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_Backend/blob/master/.github/workflows/build.yml). Pode se baixar as imagens:

```
docker push antonioaldisio/jobzfrontend
```

```
docker push antonioaldisio/jobzbackend
```

</div>


### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 15/04/2022 |  0.1   | Antônio Aldísio | Criação do documento |
| 17/04/2022 |  0.2   | Antônio Aldísio | Correção de link |
