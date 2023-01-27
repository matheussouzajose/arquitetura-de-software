### Resiliência

#### O que é resiliência?
- É um conjunto de estratégias adotadas intencionalmente para adaptação de um sistema quando um falha ocorre.
- Ter estratégias de resiliências nos possibilita minizar os riscos de perda de dados e transações importantes para o negócio.

#### Proteger e ser protegido
- Um sistema em uma arquitetura distribuída precisa adotar mecanismos de autopreservação para garantir ao máximo sua operação com qualidade.
- Um sistema não pode ser "egoísta" ao ponto de realizar mais requisições em um sistema que está falhando.
- Um sistema lento no ar muitas vezes é pior que um sistema fora do ar. (efeito dominó)

#### Health check
- Sem sinais vitais, não é possível saber a "saúde" de um sistema.
- Um sistema que não está saudável possui uma chance de se recuperar caso o tráfego para de ser direcionado a ele temporariamente.
- Health check de qualidade.

#### Rate limit
- Proteger o sistema baseado no que foi projetado para suportar.
- Preferência programada por tipo de client.

#### Circuit breaker
- Protege o sistema fazendo com que as requisições feitas para ele sejam negadas. Ex: 500
- Circuito fechado = Requisições chegam normalmente.
- Circuito aberto = Requisições não chegam ao sistema. Erro instantâneo ao client.
- Meio aberto = Permite uma quantidade limitada de requisições para verificação se o sistema tem condições de voltar ao ar integralmente.

#### API Gateway
- Uma API gateway recebe todas as chamadas de APIs de clientes e então as roteia para os microserviços correspondentes...
- Em alguns casos ela também é responsável por realizar processos de verificação de segurança, como autenticação e autorização.
- Garante que requisições "inapropriadas" cheguem até o sistema:
  - Ex: usuário não autenticado.
- Implementa políticas de Rate Limiting, Health check, etc.
- Ex: Kong

#### Service mesh
- Controla o tráfego de rede.
- Evita implementações de proteção pelo próprio sistema.
- mTLS

#### Trabalhar de forma assíncrona
- Evita perda de dados.
- Não há perda de dados no envio de uma transação de o server estiver fora.
- Servidor pode processar a transação em seu tempo quando estiver online.
- Entender com profundidade o message broker / sistema de stream.

#### Garantias de entrega: Retry
- Linear - Sem backoff
- Exponential backoff
- Exponential backoff - Jitter

#### Garantias de entrega: Kafka

#### Situações complexas
- O que acontece se o message broker cair?
- Haverá perda de mensagens?
- Seu sistema ficará fora do ar?
- Como garantir resiliência?