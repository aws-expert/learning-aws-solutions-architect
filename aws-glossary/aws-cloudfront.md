# Amazon CloudFront
- caso de uso e benefícios
- conteúdo estático e dinâmico
- origens: servidores S3, EC2, ELB, HTTP
- proteger conteúdo privado
- melhorar a segurança
  - AWS Shield Standard e Advanced
  - AWS WAF

# Escalabilidade vertical vs Escalabilidade horizontal
## Escalabilidade vertical (aumentar e reduzir a escala)
- alteração nas especificações das instâncias (mais CPU, memória)

## Escalabilidade horizontal (reduzir e expandir a escala)
- alteração no número de instâncias (adicione e remova instâncias conforme necessário).

# AutoScaling
- inicia ou encerra instâncias
- registra automaticamente novas instâncias com balanceadores de carga
- pode ser iniciado em zonas de disponibilidade

## Componentes do AutoScaling
- configuração de execução doAuto Scaling
  - especifica o tamanho da instância do EC2 e o nome do AMI

- grupo de Auto Scaling
  - refeencia a configuração de execução
  - especifica o tamanho mínimo, máximo e o desejado do grupo de Auto Scaling
  - tipo de verificação de integridade.

- Politica de Auto Scaling
  - especifica quanto a escala deve ser reduzida ou expandida.
  - uma ou mais podem ser anexadas ao grupo Auto Scaling.




