# Algoritmo Genético
---
 
 
 Trabaho de Inteligencia Artificial

 Aluno: [Edimar Antonio da Cruz](https://github.com/edimar7972)
---
 ## Explicação Teórica
---
 O _*Algoritmo Genético Binário*_ representa o uso computacional da Inteliência Artificial inspirada na Teoria da Evolução das espécies de **Charles Darwin**, o uso de algoritmos genéticos projeta melhores buscas e otimizações dentro de um domínio de interesse.
 
 A aplicação deste código consiste em tentar várias soluções começando pelo levantamento de alguns indivíduos escolhidos via seleção natural, no qual dentro desse grupo é realizada a aplicação de cruzamento ('crossover') e calculada uma chance de ocorrência de mutação para o genoma (bits) nas gerações seguintes.

 Os algoritmos genéticos possuem algumas características como por exemplo não ser determinístico, trabalhar com uma população de soluções de maneira simultanea e utilizar apenas informações de custo e recompensa. Também são computacionalmente fáceis de serem implementados e são facilmento hibridizados com outras técnicas dentro do campo de pesquisa da Inteligencia Artificial.

---
 ## Problema Proposto  
---

O desafio proposto é utilizar a implementação de algum algoritmo genético para minimizar a função descrita abaixo:


![descrição1](https://user-images.githubusercontent.com/55880792/150849825-02809e63-ff77-4029-868e-3734cd0075ec.png)

---
## Instalação e Execução
---
a construção do programa utilizou a versão 3 do **Python**, então recomendo o uso dessa mesma versão para execução do arquivo main.py. Segue o link da documentação da linguagem para as instalações da versão 3:
- https://docs.python.org/3/using/index.html
- faça um clone do projeto ou faça o download dos arquivos.
- Por meio da linha de comando caminhe até o diretório onde se encontram os arquivos-fonte.
- Execute o comando "python main.py".

## Implementação

A estrutura da implementação tomou como base não somente o pseudocódigo passado, mas também por meio de inferências/deduções com base nos materiais pesquisados (referências ao final do documento). Para fins de transparência, segue o modelo de pseudocódigo que foi usado como suporte:

1. geração de população inicial <br>
2. Avaliação de cada indivíduo dada sua sequ~encia de bits <br>
3. Loop iterativo nas partículas processando-as da seguinte forma:<br>
   1. seleção dos individuos mais aptos
   2. Criação de filhos no processo de crossover e mutação
   3. Armazenamento de dados em uma nova população
   4. Nova avaliação dos indivíduos

### Descrição dos Arquivos:
- *main.py* - Arquivo de chamada principal onde são especificados a quantidade de testes para rodar, a quantidade de iterações do AG e quantidade de populações.
- *AlgoritmoGenetico.py - Arquivo com a implementação do algoritmo junto com funções de validação, que são listadas no escopo do problema.
- *Cromossomo.py* -Arquivo com a classe que representa uma entidade Cromossomo.
   - contém atributos de:
   - valor binário;
   - aptidão;
   - valor binário decodificado
- *persistência.py* - Arquivo com funções para exportação dos resultados.

### Trechos mais importantes da implementação segundo o Pseudocódigo

**População Inicial** 
   
![populacaoInicial](https://user-images.githubusercontent.com/55880792/150856280-75d1110e-edc0-4766-b59e-bd04e451acaa.png)

**seleção por Torneio**

![selecao_torneio](https://user-images.githubusercontent.com/55880792/150856632-ea18782c-899f-4064-86d1-9ea179307a69.png)

**Decodificação**

![decodificacao](https://user-images.githubusercontent.com/55880792/150856740-c6c38d0a-6060-44a3-9ffa-906979fb06ab.png)

**Crossover**

![Crossover](https://user-images.githubusercontent.com/55880792/150856839-c2f374b6-2746-4490-8e43-8f8471d92eb3.png)

**Mutação**

![mutacao](https://user-images.githubusercontent.com/55880792/150856937-d94d1e15-3239-41ec-b8e8-1a96dcb64d13.png)

**Remove pior filho**

![removePiorFilho](https://user-images.githubusercontent.com/55880792/150857205-ee664260-b79b-4a36-81b8-8849810bbeda.png)

**Mantem melhor pai**

![mantemPai](https://user-images.githubusercontent.com/55880792/150857302-31c668a8-d819-4d77-8769-5874e03b656f.png)
---
## Resultados
As tabelas a seguir mostram os resultados gráficos(média e melhor) de gBest em cada iteração, processados em uma pilha de 10 testes para os casos de:

- [10 gerações e 10 indivíduos]

![testes - 10 interacoes-10populacao-10geracao](https://user-images.githubusercontent.com/55880792/150859772-6e696194-4ae4-4166-8734-b0014628c163.png)

![10,10,10 exec 2](https://user-images.githubusercontent.com/55880792/150859802-4d7b0129-0c0d-4cfb-834e-4617f55dd66e.png)

- [10 gerações e 20 indivíduos]
 
![testes - 10 interacoes - 20 populacao - 10 geracao](https://user-images.githubusercontent.com/55880792/150860027-33f2688d-4e6e-4dcd-af44-093fd6d7c8f4.png)

![10, 20 10, exec 1, 3 ,5, 9](https://user-images.githubusercontent.com/55880792/150860092-21c1c90a-8de7-424f-9d41-9a90ee7bbf7a.png)

- [20 gerações e 10 indivíduos]
![testes - 10 interacoes - 10 populacao - 20 geracoes](https://user-images.githubusercontent.com/55880792/150860310-2c64aba2-9273-4b16-93bb-855ff02205ff.png)

![10,10,20 exec 1, 2](https://user-images.githubusercontent.com/55880792/150860343-580d273f-c550-44d8-9aea-27b90704a00f.png)

- [20 gerações e 20 indivíduos]



![testes - 10 interacoes - 20 populacao - 20 geracao](https://user-images.githubusercontent.com/55880792/150860473-74c23b63-7a00-41e6-8670-dbde460abb63.png)

![10, 20, 20, exec 4, 7](https://user-images.githubusercontent.com/55880792/150860493-31412c91-35ef-49a6-ad7d-d7dff8eb105a.png)

## Referências
 * Slides e Vídeos
 * Contei também com a ajuda do repositório de Malu Freitas
