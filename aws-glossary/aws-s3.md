# Amazon S3
- controle de acesso
- multipart upload
- internet-api acessível
- capacidade praticamente ilimitada
- disponibilidade regional
- resiliente: 99,9999999999%

## Amazon S3: Classes de Armazenamento
- **Uso geral: Amazon S3 Stanadard**
  - requisitos de disponibilidade mais altos: usar replicações entre regiões.

- **Dados acessados com pouca frequência: Amazon S3 Standard Infrequent Access**.
  - menor custo por GB armazenado
  - maior custo por solicitação PUT, COPY, POST, GET
  - armazenamento mínimo de 30 dias.

# Amazon Glacier
- backup de dados e armazenamento de arquivos
- cofres e arquivamentos
- recuperações expressa, padrão em massa
- criptografia
- política de ciclo de vida de objetos do S3
- disponibilidade regionalmente
- resiliente 99.9999999999%