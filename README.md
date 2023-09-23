# eng_dados-data_extraction
Repositório módulo IV (Extração de Dados) da trilha de Engenharia de Dados (Santander Coders 2023)

## Integração ETL, ELT, APIs e Arquivos

Você trabalha em um e-commerce de variados produtos, e no último mês os gerentes operacionais da companhia notaram que
houve uma variação muito grande em seus estoques por períodos de até 24h, cujos produtos, voltavam ao estoque 
no dia seguinte o que não caracterizava uma venda concretizada.
Sabendo disso um dos diretores sugeriu um estudo sobre os carrinhos em aberto, e qual o perfil dos usuários que deixavam seus carrinhos em aberto, e para isso fora criada uma demanda para seu time.

Para resolver esta demanda, você e seu time deverão realizar a ingestão dos dados de:

- Usuários
- Carrinhos 

Estes dados poderão ser obtidos através dos seguintes endpoints:

- Usuários: https://dummyjson.com/auth/users
- Carrinhos: https://dummyjson.com/auth/carts

Lembrando que estes são endpoints seguros então você deverá realizar a autenticação através do seguinte endpoint: https://dummyjson.com/auth/login

Lembre-se de verificar a documentação para obter mais detalhes do funcionamento dos endpoints https://dummyjson.com/docs/auth

Após isso, os passos de tratamento do dado, serão:

1. Após consumidos os dados, você deverá persistí-los utilizando a técnica aprendida em aula em uma pastas chamada raw no formato json

2. Consumir sua camada raw e criar uma nova entidade que relacione os clientes aos carrihos através do atributo userId do seu carrinho e o atribute id da tabela users, feito isso gravar o resultado dessa agregação em uma pasta chamda kitchen

3. Por fim você deverá contemplar se os dados gerados são capazes de responder as seguintes perguntas:

    - Qual o estado de residencia possui clientes com mais carrinhos em aberto ?
    - Qual a idade dos usuários com mais carrinhos em aberto ?
    - Quais os produtos que mais aparecem em carrinhos em aberto ?
