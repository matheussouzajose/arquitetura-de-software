### Sistemas Microserviços

#### O que é um serviço?
- Disponibiliza informação.
- Realização transações.
- Resolve problemas de negócio.
- Independente de tecnologia ou produto.
- Pode estabelecer comunicação com diversos "clientes".

#### SOA: Arquitetura orientada a serviços
- Serviços normalmente maiores baseados em funcionalidades.
- Necessidade de ESB.
- Single point of failure.
- Compartilhamento de banco de dados é comum.
- Muitas vezes também podem ter sistemas monoliticos sendo utilizado como serviços.

#### Arquitetura baseada em Microserviços
- Serviços pequenos com poucas responsabilidades.
- Maior tolerância a falhas.
- Totalmente independente.
- Cada serviço possui seu próprio banco de dados.
- Comunicação síncrona ou assíncrona.

#### Microserviços não são para todas as situações
- Arquitetura complexa.
- Custo mais elevado.
- Necessidade de mais equipes para manter.
- Sistema precisa ser grande o suficiente para justificar.
- Gera problemas que normalmente você não tinha antes.
- Monitoramento complexo.
- Microserviços não são moda, mas sim necessidade.

#### Microserviços: Principais características

#### Componentização via serviços.
- Services dos microserviços != Services da OO.
- Componente é uma unidade de software independente que pode ser substituída ou atualizada.
- Desvantagens:
  - Chamadas externas são mais custosas do que chamadas locais.
  - Cruzamento entre componentes podem se tornar complexo.
  - Transações entre serviços são "grandes desafios".
  - Mudanças bruscas em regras de negócio podem afetar diversos serviços tornando o processo difícil de ser refeito.

### Organização em torno do negócio.
- Um projeto é baseado em um ou mais produtos que trabalham em diferentes contextos.
- Time de desenvolvedores por produto.
- Muitas empresas tratam os times como "squads".
- Cada squad é multidisciplinar.
- Cada squad é responsável por um ou mais produtos.
- Cada produto pode ter um ou mais serviços envolvidos.

### Estrutura baseada em produtos, não em projetos.

### Smart endpoints & Dumb pipes.
- Exposição de APIS (ex: Rest).
- Comunicação entre serviços.
- Comunicação síncrona e assíncrona.
- Utilização de sistemas de mansageria (ex: RabitMQ).
- Garantia de que um serviço foi executado baseado na execução de filas.

### Governança descentralizada.
- Ferramenta certa para o trabalho certo. Tecnologias pode ser definidas baseadas na necessida do produto.
- Diferentes padrões entre squads.
- Contratos de inteface de forma independente.

### Descentralização no gerenciamento de dados.

### Automação de infraestrutura.
- Cloud computing.
- Testes automatizados.
- Continuos delivery.
- Continuos integration.
- Load balancer / Autoscaling.

### Desenhado para falhar.
- Tolerância a falha.
- Serviços que se comunicam precisa de fallback.
- Logging
- Monitoramento em tempo real.
- Alarmes.

### Design evolutivo.
- Produtos bem definidos evoluir ou serem extintos por razões de negócio.
- Gerenciamento de versões.
- Replacement and upgradeability