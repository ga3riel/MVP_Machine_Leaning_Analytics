MVP — Machine Learning & Analytics
Nome: Gabriel Pinto de Lira do Nascimento
Matrícula: 4052026000244
Data: 05/07/2026
Dataset: Coffee Quality Institute Arabica Reviews May2023

https://www.kaggle.com/datasets/erwinhmtang/coffee-quality-institute-reviews-may2023/data

Tipo de problema: Classificação

---

# 1. Definição do problema

## 1.1 Descrição do problema

Sou designer formado, mas sempre trabalhei com dados, fazendo apresentações e infográficos. Estou em transição de carreira, e por questão de afinidade, atualmente trabalho como analista de dados. O tema de machine learning foi um grande desafio de aprendizado. Como forma de tornar o assunto mais leve, e acima de tudo ter contexto: avalair os resultados exige entender o que é realmente relevante e extrair insights, escolhi Cafés Especiais como tema.



---



### **Contexto**
O mercado de cafés especiais é altamente valorizado e rigoroso. Para que um café receba o selo de "Especial", ele precisa atingir uma pontuação igual ou superior a 80 pontos (Total Cup Points) na avaliação da Specialty Coffee Association (SCA) / Coffee Quality Institute (CQI), e não possuir defeitos (categoria 1 de defeitos, a mais relevante) e até 5 efeitos na categoria 2.

O desafio é que essa nota final é obtida através de um processo de degustação sensorial (o cupping) feito por especialistas certificados (Q-Graders), o que ocorre apenas nas etapas finais da cadeia. Antes de virar bebida, o café é apenas um grão cru (verde) com características físicas, de plantio e de colheita.


---


### **Objetivo**

O modelo tem como objetivo principal apoiar a decisão de compra e precificação de lotes de café através de uma tarefa de **Classificação**. O algoritmo deve prever qual é a probabilidade de um lote de café cru ser classificado como "Especial" (Nota $\ge$ 80) baseando-se exclusivamente em suas características geográficas e físicas preliminares (como Altitude, País de Origem, Método de Processamento, Cor do grão e variedade do café), ou seja, sem a necessidade prévia da prova na xícara.


#### **Defeitos no café e origem**
Além disso existe um ponto importante, os defeitos no café tipo 1 dizem respeito mais ao cuidado (higiene) e ao processo de colheita e secagem do que da qualidade do grão em si. Os defeitos do tipo 2 dizem respeito ao momento certo de colheita, ou o grau de maturação.  Se a maturação for muito rapida, o café não tem tempo de ganhar caracteristicas importantes como sua doçura. Aqui a altitude ganha importância. Por isso esses atrubutos não vao ser utilizados no teste.

Como o país de origem tem forte relação com o processo e sua qualidade, assim como o defeito, retirei esses tres parametros para reduzir o viés, e foquei nas qualidades físicas preliminares. Cheguei a fazer um teste com o país de origem, e não obtive resultados muito bons (recall baixo, ou underfiting).



---


### **Grupo de interesse**

* **Compradores de Café Verde e Torrefações (Roasters):** Que precisam decidir quais lotes comprar e querem minimizar o risco de adquirir um café que não atinja o padrão de especialidade.

* **Produtores e Fazendeiros:** Que desejam entender o potencial da sua safra com base nos dados climáticos, geográficos e no processo de pós-colheita adotado na fazenda, antes mesmo de enviar o café para a avaliação de um especialista.

* **Cooperativas de Café:** Que precisam triar e categorizar rapidamente grandes volumes de sacas recebidas.


---


### **Relevância**

A avaliação sensorial humana é um processo caro, demorado e que exige mão de obra altamente especializada. Se o mercado puder estimar o potencial de qualidade de um lote de café de forma antecipada — olhando apenas para os dados técnicos da ficha do produtor (geografia e caracteristicas físicas do grão) —, é possível otimizar direcionar melhor os investimentos, antecipar a precificação correta de uma safra e focar em melhorar processos onde existem um potencial grande de se obter cafes especiais (e consequentimente de maior valor agregado).



---




### **Como um café é avaliado**

A Avaliação SCA/CQI é feita através de uma amostra padronizada, com cerca de 350g de grãos de café. Esta é a metodologia global para Cafés Especiais. O avaliador (Q Grader) pega uma amostra do café cru (verde). Ele mesmo faz uma torra clara, rigorosamente padronizada, e degusta a bebida (processo chamado de cupping).

O objetivo aqui é avaliar o potencial genético e o terroir (solo, clima, cuidado na colheita) do grão. A torra comercial pode "esconder" defeitos (se for muito escura) ou mascarar sabores. Ao padronizar uma torra clara apenas para a prova, o degustador consegue sentir exatamente o que aquele grão tem de bom (notas frutadas, florais) ou de ruim.
