# Testes de Software
Ricardo Ajáx

**Problema**: Achar os defeitos de um modelo de dados;

**Método de Verificação:** Inspeção

### Definição de Papéis
**Redator**: Gabriela 
**Moderador**: Adrianne
**Inspetores**: Maria Luiza, Natália, Letícia, Vítor e João Carlos

### Níveis de Criticidade

![criticidade.png](https://uploaddeimagens.com.br/images/001/663/264/original/criticidade.png?1539197076)

**Referência** 
> GALIN, Daniel. Software quality assurance: from theory to implementation. Pearson Education India, 2004. 

### Resultado

### Erros do DE-R
|#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo| 
:-:|:-|:-:|:-|:-:
|D1|Falta da entidade ITEM causa inconsistência com a descrição do problema|5|Colocar a entidade ITEM se relacionando com PRODUTO e VENDA||
|D2|Id desnecessário na entidade MEDICAMENTO|3|Retirar o id||
|D3|O atributo telefone da entidade FABRICANTE está como multivalorado, em desacordo com a descrição do problema, pois não é requisitado|1|Colocar como atributo simples||
|D4|O atributo nome_cliente na entidade VENDA fere a forma normal recomendada para garantir a consistência do banco|4|Criar uma entidade CLIENTE com seus respectivos atributos: CPF, nome e id ||
|D5|Indicar a direção do relacionamento entre PRODUTO e VENDA|1|Colocar a direção no relacionamento||
|D6|A entidade RECEITA não possui chave primária |4| Colocar chave primária id na entidade RECEITA||
|D7|Cardinalidade entre MEDICAMENTO e RECEITA deve ser de N:1 não 1:1 |5|Arrumar a cardinalidade no relacionamento||


### Erros do Diagrama Lógico
|#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo| 
:-:|:-|:-:|:-|:-:
|L1|Não é necessária a tabela para telefone| 1 | Excluir tabela e adicionar atributo telefone na entidade Fabricante| 
|L2|A cardinalidade entre as tabelas de Receita e Medicamento está errada, pois é N:1|5|Arrumar a cardinalidade entre essas tabelas|
|L3|Deve haver tabela para ITEM | 5 |  Colocar a tabela ITEM entre as tabelas de Produto e Venda|
|L4|Não deve ter id em MEDICAMENTO | 3 |Retirar id na tabela de Medicamento |


### Erros do Dicionário de Dados
|#|Descrição do defeito|Criticidade|Proposta de Reparo | Prazo sugerido para Reparo| 
:-:|:-|:-:|:-|:-:
|DD1|O atributo cep em FABRICANTE está incosistente com o diagrama lógico|4|Mudar o tamanho do atributo no dicionário de dados||
|DD2|O atributo fragancia em PERFUMARIA está incosistente com o diagrama lógico|4|Mudar o tamanho do atributo no dicionário de dados||

### Sugestões de Melhoria

* No dicionário de dados, mudar o tipo do atributo data_emissao da tabela Receita para DATE;
* Adicionar complemento no atributo composto de endereço da entidade FABRICANTE;
* Mudar tipo do atributo cep de VARCHAR para INTEGER;
* Mudar o tamanho do atributo nome_cliente para 50;
* Padronizar nomenclatura dos atributos;

