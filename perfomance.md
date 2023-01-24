### Perfomance

#### O que é perfomance?
- É o desempenho que um software possui para completar um determinado workload.
- As unidades de medidas para avaliarmos a perfomance de um software são:
  - Latência ou "response time".
  - Throughput (Quantidade de requisição que um software aguenta).
- Ter um software performático é diferente de ter um software escalável.

#### Métricas para medir a performance
- Diminuir a latência:
  - Normalmente a medida em milliseconds.
  - É afetada pelo tempo de processamento da aplicação, rede e chamadas externas.
- Aumentando throughput:
  - Quantidade de requisições.
  - Diretamente ligado com a latência.

#### Principais razões para baixa performance
- Processamento ineficiente.
- Recursos computacionais limitados.
- Trabalhar de forma bloqueando.
- Acesso serial a recursos.

#### Principais razões para aumentar performance
- Escala da capacidade computacional (CPU, Disco, Memória, Rede).
- Lógica por trás do software (Algoritmos, queries, overhead de frameworks).
- Concorrência e paralelismo.
- Banco de dados (tipos de bancos, schema).
- Caching.

#### Capacidade computacional: Escala vertical vs horizontal
- Escala vertical:
  - Aumentar a capacidade computacional (Recursos computacionais).
- Escala horizontal:
  -  Aumentar a capacidade de máquinas (load balancer).

#### Diferença entre concorrência e paralelismo
- "Concorrência é sobre lidar com muitas coisas ao mesmo tempo. Paralelismo é fazer muitas coisas ao mesmo tempo". Ron Pike.

#### Vamos imaginar um webserver
- Trabalhando de forma serial - único processo.
- Forma concorrente / pararela

#### Caching
- Cache na borda / Edge computing
- Dados estáticos
- Páginas web
- Funções internas
  - Evita reprocessamento de algoritmos pesados
  - Acesso a banco de dados
- Objetos

#### Caching: Exclusivo vs Compartilhado
- Exclusivo:
  - Baixa latência.
  - Duplicado entre os nós.
  - Problemas relacionados a sessões.
- Compartilhado:
  - Maior latência.
  - Não há duplicação.
  - Sessões compartilhadas.
  - Banco de dados externo:
    - MySQL
    - Redis
    - Memcached

#### Caching: Edge computing
- Cache realizado mais próximo ao usuário
- Evita a requisição chegar até o Cloud Provider / Infra
- Normalmente arquivos estáticos
- CDN - Content Delivery Network
- Cloudflare workers
- Vercel