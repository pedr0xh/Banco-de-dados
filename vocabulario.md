1) No seu github pessoal, criar um repositório de banco de dados (caso ainda não exista) e dentro dele um arquivo chamado vocabulario.md. Nele preencher o significado das expressões abaixo, mantendo o texto ordenado:
sistema gerenciador de banco de dados:
SGBD, como mencionado acima, é um sistema de gerenciamento para banco de dados que controla, organiza, acessa e protege as informações de uma aplicação.

restrições em banco de dados:
Há cinco tipos de restrições: estrutural, funcional, integridade, referencial e NOT NULL. As restrições estruturais restringem quais dados podem fazer parte do banco, enquanto as funcionais restringem como esses dados podem ser aplicados. A integridade se baseia na chave primária, enquanto a integridade referencial utiliza chaves estrangeiras. Por fim, temos a NOT NULL, que é uma regra que impede que haja valores nulos em determinada linha ou coluna de uma tabela.

modelo relacional:
É uma ideia mais definida, já com atributos e chaves definidos, diferente da modelagem conceitual.

modelagem conceitual:
Um modelo relacional tem o intuito de ser algo mais teórico do que prático; podemos dizer que ele é um esboço do que será feito.

modelagem lógica:
Usa a estrutura da modelagem conceitual e adiciona outras informações para assim dar maior sentido ao que está sendo desenvolvido.

modelagem física:
É algo mais detalhado, assim ajudando mais os desenvolvedores do banco de dados.

linguagem SQL:
É a linguagem que usamos para mexer no banco de dados, desde fazer pesquisas até armazenar ou deletar dados.

Data Definition Language (DDL):
É o que permite o usuário definir novas tabelas e o que será associado a ela, responsável também pelos comandos CREATE, ALTER e DROP.

Data Manipulation Language (DML):
Já esse, é o que permite interagir diretamente com os dados das tabelas, responsável pelos comandos INSERT, UPDATE e DELETE.

Boas práticas em modelagem de banco de dados
Utilizar nomes descritivos e consistentes para tabelas, colunas e restrições, facilitando a compreensão e manutenção do banco de dados ao longo do tempo.
Procure sempre utilizar, sempre que possível, apenas uma chave primária. Quando houver uma relação muitos para muitos (n para n), crie uma chave primária específica para aquela tabela.]

# PESQUISAS SQL

1) SELECT * from cliente
2) SELECT * FROM veiculo, cliente WHERE placa LIKE '%3'
3) SELECT * FROM cliente WHERE uf_cnh = 'RS' AND telefone IS NULL
5) SELECT COUNT(*) AS total_veiculos FROM veiculo
6) SELECT v.* FROM veiculo v JOIN contrato_aluguel ca ON v.id_veiculo = ca.id_veiculo JOIN cliente c ON ca.id_cliente = c.id_cliente WHERE c.nome = 'Alexandre Zamberlan'
7) SELECT c.nome AS nome_cliente, e.nome AS nome_escritorio FROM contrato_aluguel ca JOIN cliente c ON ca.id_cliente = c.id_cliente JOIN escritorio e ON ca.id_escritorio = e.id_escritorio
