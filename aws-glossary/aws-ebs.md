# EBS (Elastic Block Store)
- diferentes tipos
  - **SSD (general purpose)**
    - É um tipo de volume EBS de propósito geral que fornece um equilíbrio entre preço e desempenho.
    - recomendado para a maioria de cargas de trabalho
    - volumes de inicialização do sistema
    - ambientes de desenvolvimento e testes.
    - tamanho do volume: 1GIB a 16TB
  - **SSD (IOPS)**
    - Esse tipo de volume EBS é projetado para cargas de trabalho que exigem um desempenho de I/O (entrada/saída) consistente e baixa latência.
    - aplicações critícas de negócios que exigem performance de IOPS
    - cargas de trabalho de grandes bancos de dados
    - tamanho do volume: 4GIB a 16TB
  - **HDD (otimizado para taxas de transferencias)** - 
    - cargas de trabalho de streaming que exigem taxa de transferência rápida e consistente.
    - big data
    - data warehouse
    - processamento de logs
    - não pode ser volume de inicialização
    - taamnho do volume: 500GIB a 16TB
  - **HDD (frio, cold)** 
    - armazenamento orientado para taxa de transferência para grandes volumes de dados acessados.
    - não pode ser um volume de inicialização
    - tamanho do volume: 500GIB a 16TB


- criptografia
- snapshots
- capacidade provisionada
- ciclo de vida independente da instancia do EC2
- varios volumes distribuiidos para criar grandes volumes.



