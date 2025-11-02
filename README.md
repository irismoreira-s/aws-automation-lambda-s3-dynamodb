# aws-automation-lambda-s3-dynamodb

O estudo começou com o entendimento detalhado do Amazon S3, analisando seu funcionamento como serviço de armazenamento de objetos, classes de armazenamento, políticas de acesso, versionamento e replicação entre regiões, o que permitiu compreender como os dados podem ser organizados e acessados de forma segura e eficiente. Paralelamente, foi explorado o AWS Lambda, entendendo seu modelo serverless, como criar funções que executam código em resposta a eventos, a gestão de memória, tempo de execução e triggers de serviços AWS, como o S3.

Combinando Lambda e S3, foi implementado um fluxo automatizado de upload e processamento de arquivos. Por exemplo, ao enviar um arquivo para um bucket do S3, uma função Lambda era acionada automaticamente, registrando informações no DynamoDB sobre o arquivo processado, como nome, tamanho e timestamp. Essa integração demonstrou a eficiência do modelo serverless em automatizar tarefas repetitivas sem intervenção manual, garantindo consistência e rastreabilidade.

Para validar a infraestrutura e os fluxos de trabalho de forma local antes do deploy na AWS, utilizamos LocalStack, que permitiu simular os serviços AWS de S3, Lambda e DynamoDB. Foram criados scripts para criar buckets, carregar arquivos de teste, disparar funções Lambda e verificar registros no DynamoDB, garantindo que todo o pipeline funcionasse corretamente antes de subir para a nuvem. Além disso, exercícios práticos de manipulação de arquivos localmente reforçaram a compreensão sobre eventos, triggers e logs das funções Lambda.

O estudo de caso aplicado ao final do laboratório consolidou todo o aprendizado, mostrando como arquiteturas serverless podem ser aplicadas em cenários reais, como:

Processamento de arquivos enviados por usuários: imagens, documentos ou dados de sensores podem ser automaticamente processados e catalogados;

Integração com bancos de dados para auditoria: cada arquivo processado gera uma entrada de registro em uma tabela do DynamoDB, garantindo rastreabilidade;

Testes e validações locais: LocalStack permite reproduzir todo o fluxo de trabalho sem custos de recursos na AWS, tornando o desenvolvimento mais rápido e seguro.

# Anotações importantes

Configurações de triggers no S3 e permissões de IAM necessárias para Lambda acessar buckets e DynamoDB;

Diferença entre eventos síncronos e assíncronos para Lambda;

Dicas para debugar funções Lambda usando logs do CloudWatch e testes locais com LocalStack;

Estratégias para estruturar buckets e funções para facilitar manutenção e escalabilidade futura.

