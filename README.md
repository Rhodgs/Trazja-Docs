# Sistema Trazja

## Descrição Geral
O Trazja é uma plataforma digital de delivery que orquestra a interação entre Clientes, Restaurantes e Entregadores. O sistema gerencia todo o ciclo de vida de um pedido, desde a sua criação até a entrega final.

## Requisitos Gerais


## Diagramas UML


## Arquitetura do Sistema
O sistema **TrazJá** foi projetado seguindo o padrão arquitetural **MVC (Model-View-Controller)**, que separa a aplicação em três camadas lógicas para facilitar a manutenção e escalabilidade:

* **Model (Modelo):** Responsável pela estrutura de dados e regras de negócios.
    * Gerencia as entidades principais como *Cliente, Restaurante, Entregador e Pedido*.
    * Garante a integridade e segurança dos dados, incluindo a criptografia de informações sensíveis (conforme **RNF02** e **RSW01**)
    * Realiza a persistência das informações no Banco de Dados.

* **View (Visão):** Responsável pela interface com o usuário.
    * Apresenta as telas do aplicativo compatíveis com **Android e iOS** (conforme **RNF05**)
    * Exibe o status do pedido em tempo real e os formulários de cadastro.
    * É a camada que interage diretamente com o Cliente, Entregador e Restaurante.

* **Controller (Controlador):** Responsável por intermediar a comunicação entre a View e o Model.
    * Processa as requisições, como o cálculo automático de frete baseado na distância (conforme **RSW07**) e a validação de pagamentos em até 5 segundos (conforme **RNF01**)
    * Gerencia o fluxo de notificações automáticas entre os usuários (conforme **RSW06**)