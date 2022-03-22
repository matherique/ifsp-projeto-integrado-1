# VISAO GERAL 

> Tema: Sistema de gestão de Doceria

## Entrega 1 - 28/03/22
- Introducao 
  - Objetivos
  - Justificativa
  - Problema

- Tecnologia Utilziadas (Linguagens de programacao, banco de dados, etc)
  - Backend
    - Go
    - Postgresql
  - Frontend
    - React
  - App? Talvez 

- Usuarios (min 3) (1 tabela cliente com papeis diferentes)
  - Cliente (role=cliente)
    - Cria, cancela e visualiza um pedido
    - Pagamento (FUTURO)
  - Funcionario (role=funcionario)
    - Gerencia Receitas
    - Gerencia estoque
    - Gerencia Pedido
  - Admin (role=administrador)
    - Gerencia Clientes
    - Gerencia funcionários

- Requistos funcionais (min 30) e nao funcionais(min 10)
- Casos de uso (apenas titulo - minimo 20)
  - Desenvolver somente 12 items

## "Modulos"

 - Bolos
 - Produtos
 - Usuarios (divisoria por "roles")
 - Estoque
 - Contas (projeto 2)
 - Pedidos 
 - Relatório (projeto 2)
 - Cupons 
 - Pagamento ? (projeto 2)

## Requisitos Funcionais 

- RF1: O sistema deve permitir a criaçao de um pedido 
- RF2: O sistema deve permitir o cancelamento de um pedido pelo cliente e funcionário
- RF3: O sistema deve permitir a visualizacao de um pedido pelo cliente e funcionário
- RF4: O Sistema deve permitir a edicao de um pedido pelo funcionário
- RF5: O sistema deve permitir alteracao de status: "Iniciado", "Preparo", "Em rota de entrega", "Entregue", "Cancelado"
- RF6: O sistema deve gerar um link do google maps com a rota da entrega para pedidos com entrega
- RF7: O sistema deve permitir o cadastro de usuario com "role=client" 
- RF8: O sistema deve permitir que somente o usuario com "role=administrador" cadastrar usuario com "role=funcionário"
- RF9: O sistema deve permitir que somente o usuario com "role=adminitrador" alterar as "roles" do usuário
- RF10: O sistema deve permitir a criacao de um bolo pelo usuario com "role=funcionario,admninitrador"
- RF11: O sistema deve permitir a edicao de um bolo pelo usuario com "role=funcionario,admninitrador"
- RF12: O sistema deve permitir desabilitar um "bolo" da opção de compra pelo usuario com "role=funcionario,administrador"
- RF13: O sistema deve permitir a listagem de bolos com filtros do tipo: "Ativo/inativo, categoria, etc..."
- RF14: O sistema deve permitir o cadastro de produtos utilizados na criacao dos bolos (farinha, ovo, leite, etc) 
- RF15: O sistema deve notificar os usuarios quando um item do estoque esteja em baixa 
- RF16: O sistema deve permitir a definicao de um valor de unidade para caso seja menor, notificar os usuarios 
  ```go
    if quantidade_produto_x < quantidade_minima_produto_estoque {
      notificar();
    }
  ```
- RF17: O sistema deve permitir a entrada de produtos no estoque pelo usuario com "role=functionario,administrador"
- RF18: O sistema deve remover os produtos do estoque no momento da criacao do pedido
- RF19: O sistema deve "re-entrar" os produtos que foram removidos caso o pedido seja cancelado antes do preparo
- RF20: ? O sistema deve permitir a criação de um cupom de desconto (porcentagem ou quantidade)
- RF21: ? O sistema deve permitir a criacao de um cupom para um determinado bolo ou categoria
- RF22: O sistema deve permitir a criacao de contas a pagar pelo usuario com "role=adminitrador"
- RF23: O sistema deve permitir a criacao de contas a receber pelo usuario com "role=adminitrador" (fiado?) 
- RF24: O sistema deve permitir a configuracao de limite de pedidos diarios 
- RF25: O sistema deve bloquear horario de entrega para que nao possa ser utilizado esse horario
- RF26: O sistema deve reservar os horarios de entrega dos pedidos 
- RF27: O sistema deve gerar relatorios de pedidos 
- RF28: O sistema deve gerar relatorios de estoque
- RF29: O sistema deve gerar relatorios de contas
- RF30: O sistema deve gerar relatorios de produtos
- RF31: O sistema deve gerar relatorios de bolos 
- RF32: O sistema deve aceitar pagamento do cliente no momento do pedido
- RF32: O sistema deve gerar um link de pagamento para enviar para o cliente 
- RF33: O sistema deve

## Requisitos Não funcionais

- RNF1: O backend do sistema deve ser desenvolvido em Go
- RNF2: O frontend do sistema deve ser desenvolvido em ReactJs 
- RNF3: O sistema deve utilizar o banco de dados Postgress
- RNF4: O sistema deve ser resposivo para acesso mobile ou de tablet
- RNF5: O sistema deve salvar a sessao do usuario para proximos acessos
- RNF6: O sistema deve 
- RNF7: 
- RNF8: 
- RNF9: 
- RNF10: 


## Casos de uso
