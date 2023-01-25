### Escalabilidade

### O que é escalabilidade?
- Escalabilidade é a capacidade de sistemas suportarem o aumento (ou a redução) dos workloads incrementando (ou reduzindo)
  o custo em menor ou igual proporção.

### Escalabilidade vs Perfomance
- Enquanto a perfomance que o foco em reduzir a latência e aumentar o throughput, a escalabilidade visa termos a possibilidade
  de aumentar ou diminuir throughput adicionando ou removendo a capacidade computacional.

### Escalando software
- Escala vertical:
  - Recursos computacional.

- Escala horizontal:
    - Não está relacionado a aumentar o recurso computacional, mas sim a quantidade de máquinas em si.
    - Utiliza-se um load balance / Proxy reverso.

### Escalando software - Descentralização
- Disco efêmero.
- Servidor de aplicação vs Servidor de assets
- Cache centralizado.
- Sessões centralizadas.
- Upload / Gravação de Arquivos.
- Tudo pode ser destruído e criado facilmente.

### Escala de banco de dados
- Aumentando recurso computacionais.
- Distruindo responsabilidades (escrita vs leitura).
- Shards de forma horizontal.
- Serverless

### Otimização de queries e índices
- Trabalho com índices de forma consciente.
- APM (Application perfomance monitoring) nas queries.
- Explain nas queries.
- CQRS (Command Query Responsibility Segregation).

### Proxy reverso
- Um proxy reverso é um servidor que fica na frente dos servidores web e encaminha as solicitações do cliente
  (por exemplo, navegador web) para esses servidores web.

### Soluções populares de Proxy Reverso
- Nginx.
- HAProxy (HA = High Availability).
- Traefik.