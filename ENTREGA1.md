# VISAO GERAL 

> Tema: Sistema de gestão de Doceria

## Entrega 1 - 28/03/22
- Introducao 
  - Objetivos
  - Justificativa
  - Problema

- Tecnologia Utilizadas (Linguagens de programacao, banco de dados, etc)
  - Backend
    - Go
    - Postgresql
  - Frontend
    - React
  - App? Talvez 

- Usuarios (min 3) (1 tabela cliente com papeis diferentes)
  - Cliente (role=cliente)
  - Funcionario (role=funcionario)
  - Admin (role=administrador)

- Requistos funcionais (min 30) e nao funcionais(min 10)
- Casos de uso (apenas titulo - minimo 20)
  - Desenvolver somente 12 items

## "Modulos"

C - Create
R - Read
U - Update
D - Disable

 - Bolos (C R U D)
 - Produtos (C R U D)
 - Usuarios (divisoria por "roles") (C R U D)
 - Estoque (C R U D)
 - Contas (projeto 2) (C R U D)
 - Pedidos (C R U D)
 - Relatório (projeto 2) (C R)
 - Cupons (C R U D)
 - Pagamento ? (projeto 2) (C) 

## Casos de uso

- 1 Cadastro de bolos
- 2 Cadastro de produtos
- 3 Cadastro de usuarios
- 4 Alteracao de roles de usuários
- 5 Login cliente
- 6 Login usuarios
- 7 Entrada de item no estoque
- 8 Saida de item no estoque
- 9 Cadastro de cliente
- 10 Cadastro de contas a pagar 
- 11 Cadastro de contas a receber
- 12 Criacao de um pedido (todos os status)
- 13 Cancelamento de um pedido
- 14 Geracao de relatorios
- 15 Cadastro de cupom
- 16 Notificacao de usuarios (todas "roles")
- 17 Fluxo de pagamento (rejected, schedule, paid)
- 18 
- 19 
- 20 

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
- RF33: O sistema deve gerar um link de pagamento para enviar para o cliente 
- RF34: O sistema deve gerar um link de pagamento para enviar para o cliente 
- RF35: O sistema deve notificar o cliente(role=cliente) a alteracao de status do pedido (Whatsapp?? twillow?)

## Requisitos Não funcionais

- RNF1: O backend do sistema deve ser desenvolvido em Go
- RNF2: O frontend do sistema deve ser desenvolvido em ReactJs 
- RNF3: O sistema deve utilizar o banco de dados Postgress
- RNF4: O sistema deve ser resposivo para acesso mobile ou de tablet
- RNF5: O sistema deve salvar a sessao do usuario para proximos acessos
- RNF6: O sistema deve estar online 24/7
- RNF7: O frontend deve se comunicar com o backend via REST API
- RNF8: O sistema devera ser de facil manutencao 
- RNF9: O sistema devera poder receber atualizacao qualquer momento via CI/CD
- RNF10: O sistema devera ter testes unitários e de integraçao


