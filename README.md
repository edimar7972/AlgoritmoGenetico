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
