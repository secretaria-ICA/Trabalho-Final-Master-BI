# Otimizacao_de_Rota_para_Agente_Comercial

Problema - Caso real Caixeiro Viajante – Agente Comercial lotado nos Estados do CE, RN e PB que tem que cumprir uma rotina mensal de visitas a lojas de uma determinada Corporação

#### Aluno: [Sérgio Guerra](https://github.com/sgustavobr)
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC)

---

- [Link para o código de resolução do problema](https://github.com/sgustavobr/Trabalho-Final-Master-BI/blob/main/Controle%20de%20visita%20e%20distribui%C3%A7%C3%A3o%20de%20Chips_VF.xlsx)

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

### Resumo

Trata-se de um problema de um Agente Comercial que tem que visitar 20 municípios que se localizam nos Estados do Ceará, Rio Grande do Norte e Paraíba.

Esse Agente Comercial tem como objetivo incrementar as vendas das lojas desses Municípios e como só tem 20 dias úteis por mês para desempenhar esse papel, testamos as melhores hipóteses entre distâncias, custos de hospedagem e alimentação ou de combustível para otimizar o percurso e os gastos com as despesas.


### 1. Introdução

Para identificar a melhor rota definimos inicialmente quais seriam as variáveis de cada trajeto a fim de minimizar a distância total a ser percorrida ou os custos envolvidos nos deslocamentos. A partir daí, identificamos as distâncias envolvidas, os custos de alimentação e hospedagens necessários para cumprir o roteiro e os custos gastos com combustíveis para os deslocamentos, considerando que o Agente Comercial utiliza veículo próprio com reembolso.

Os trajetos serão realizados mensalmente pelo Agente e a função dele é aumentar as vendas nas lojas desses municípios, portanto a eficiência nesses deslocamentos é fundamental para que o profissional atinja as suas metas pessoais e consiga desempenhar um bom papel na sua firma.


### 2. Modelagem

Primeiro definimos as variáveis que mais influenciam no nosso entendimento e a partir de então rotas foram traçadas. Seguindo esse raciocínio dividimos o problema em 3 partes.

Rota 1 – Baseado nas distâncias entre os 20 munícipios em que o Agente Comercial deve visitar;
Rota 2 - Baseado nos custos de Alimentação e Hospedagem em cada Município que o Agente Comercial deverá pernoitar;
Rota 3 – Baseado nos Custos de combustível que o Agente vai despender para cumprir a tarefa de visitar 20 Municípios durante o mês.


Com os dados em mãos, montamos uma ordem dos Municípios e criamos uma matriz de valor para cada Rota específica.

A partir desse ponto utilizamos o solver para traçarmos as soluções. No solver, as restrições do problema eram:

1.	Ordem dos Municípios tinham que ser menor ou igual a 20;
2.	O número da ordem tinha que ser distinto;
3.	Número da ordem tinha que ser maior que 1;
4.	Número da ordem tem que ser inteiro.;
5.	O método de solução é evolutionary; e
6.	O Objeto é minimizar tanto as despesas quanto os custos.


### 3. Resultados

- [Mapa da Rota 1]

![rota1](https://github.com/sgustavobr/Trabalho-Final-Master-BI/blob/main/Rotas/Rota1.jpg "Rota 1")

Rota 1: Mostra o melhor traçado para percorrer os 20 municípios só considerando as distâncias. Essa rota seria a melhor a ser feito sem levar em conta os custos. Contudo, é o principal parâmetro de comparação, principalmente visual, com as demais rotas.

- [Mapa da Rota 2]

![rota2](https://github.com/sgustavobr/Trabalho-Final-Master-BI/blob/main/Rotas/Rota2.jpg "Rota 2")

Rota 2: Nessa rota buscamos equilibrar o trajeto com os custos de hospedagem e alimentação. Quando fizemos isso, percebemos que a rota otimizada segue um zig-zague que não é recomendado para esse tipo de problema.

- [Mapa da Rota 3]

![rota3](https://github.com/sgustavobr/Trabalho-Final-Master-BI/blob/main/Rotas/Rota3.jpg "Rota 3")

Rota 3: Como nos últimos tempos temos observado uma grande alta nos preços dos combustíveis, testamos a nossa hipótese considerando no trajeto a variável gastos com gasolina para atender a demanda do Agente Comercial. Nota-se uma rota talvez não esteja tão otimizada quanto a rota 1, mas não tão diferente e considerando que tais custos são elevados, essa opção tem que ser analisada em conjunto com a 1° rota.


### 4. Conclusões

Com o objetivo de ter também uma análise visual, utilizamos uma ferramenta gráfica para nos ajudar a ter uma conclusão visual. O software utilizado é ferramenta de mapas avançada que nos foi muito útil aqui.

Depois de feita essa explicação, uma análise pura e simples de traçado nos levaria a escolher a Rota 1 por ser mais direta em termos de distância e consequentemente no dispêndio da variável tempo de deslocamento.

Contudo, levando em consideração que os custos de combustíveis atualmente têm que fazer parte integrante desse problema e considerando que o mapa geográfico da Rota 1 e 3 não são tão distintos, optamos por escolher a Rota 3 como a ideal para o problema do Agente Comercial.

---

Matrícula: 201.110.026

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós-graduação - *Business Intelligence Master*

