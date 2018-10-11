# Testes de Software
Ricardo Ajáx

**Problema**: Encontrar os defeitos de um modelo de dados;

**Método de Verificação:** Inspeção

### Definição de Papéis
**Redator**: Gabriela
**Moderador**: Adrianne
**Inspetores**: Maria Luiza, Natália, Letícia, Vítor e João Carlos

### Níveis de Criticidade

Os níveis de criticidade dizem respeito à classificação dos erros encontrados nos artefatos. Foram analisados o diagrama Entidade-Relacionamento, relativo ao modelo conceitual do problema apresentado, o modelo lógico e o dicionário de dados correspondente. Para estabelecer um nível de criticidade para cada erro relatado, utilizou-se a escala presente na tabela abaixo:

![criticidade.png](https://uploaddeimagens.com.br/images/001/663/264/original/criticidade.png?1539197076)

**Referência**
> GALIN, Daniel. Software quality assurance: from theory to implementation. Pearson Education India, 2004.

### Resultado

De acordo com a discussão entre todos os membros de equipe, encontrou-se os erros listados nas duas tabelas abaixo. A primeira delas diz respeito ao DE-R (Diagrama Entidade-Relacionamento), segunda ao diagrama lógico e última diz respeito ao dicionário de dados. Os prazos sugeridos para o reparo foram determinados de acordo ao nível de criticidade do defeito, como se segue.

### Erros do DE-R
#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo
:-:|:-|:-:|:-|:-:
D1|Falta da entidade ITEM causa inconsistência com a descrição do problema|5|Colocar a entidade ITEM se relacionando com PRODUTO e VENDA| 1h
D2|Id desnecessário na entidade MEDICAMENTO|3|Retirar o id| 10 min
D3|O atributo telefone da entidade FABRICANTE está como multivalorado, em desacordo com a descrição do problema, pois não é requisitado|1|Colocar como atributo simples| 20 min
D4|O atributo nome_cliente na entidade VENDA fere a forma normal recomendada para garantir a consistência do banco|4|Criar uma entidade CLIENTE com seus respectivos atributos: CPF, nome e id | 50 min
D5|Indicar a direção do relacionamento entre PRODUTO e VENDA|1|Colocar a direção no relacionamento| 10 min
D6|A entidade RECEITA não possui chave primária |4| Colocar chave primária id na entidade RECEITA| 20 min
D7|Cardinalidade entre MEDICAMENTO e RECEITA deve ser de N:1 não 1:1 |5|Arrumar a cardinalidade no relacionamento| 30 min

**Total do tempo para reparo**: 2 horas e 20 minutos

### Erros do Diagrama Lógico
|#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo|
:-:|:-|:-:|:-|:-:
|L1|Não é necessária a tabela para telefone| 1 | Excluir tabela e adicionar atributo telefone na entidade Fabricante| 10 min
|L2|A cardinalidade entre as tabelas de Receita e Medicamento está errada, pois é N:1|5|Arrumar a cardinalidade entre essas tabelas| 10 min
|L3|Deve haver tabela para ITEM | 5 |  Colocar a tabela ITEM entre as tabelas de Produto e Venda| 1h
|L4|Não deve ter id em MEDICAMENTO | 3 |Retirar id na tabela de Medicamento | 10 min

**Total do tempo para reparo**: 1 hora e 30 minutos

### Erros do Dicionário de Dados
#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo
:-:|:-|:-:|:-|:-:
DD1|O atributo cep em FABRICANTE está incosistente com o diagrama lógico|4|Mudar o tamanho do atributo no dicionário de dados| 10 min
DD2|O atributo fragancia em PERFUMARIA está incosistente com o diagrama lógico|4|Mudar o tamanho do atributo no dicionário de dados| 10 min

**Total do tempo para reparo**: 20 min

### Sugestões de Melhoria

Como acordado em cada uma das análises apresentadas nas tabelas acima, sabe-se que as correções levariam um total de 4h e 10 min. Além disso, foram identificadas as seguintes prováveis melhorias:

* No dicionário de dados, mudar o tipo do atributo data_emissao da tabela Receita para DATE;
* Adicionar complemento no atributo composto de endereço da entidade FABRICANTE;
* Mudar tipo do atributo cep de VARCHAR para INTEGER;
* Mudar o tamanho do atributo nome_cliente para 50;
* Padronizar nomenclatura dos atributos;
