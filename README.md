# **Desafio Dio - Criando um Ecossistema Hadoop Totalmente Gerenciado com Google Cloud Dataproc**

O Google Cloud Dataproc é um serviço totalmente gerenciado que permite executar o ecossistema Apache Spark e Apache Hadoop no Google Cloud Platform. Ele fornece uma maneira fácil e rápida de criar clusters Hadoop, gerenciar recursos, executar tarefas e monitorar seu ecossistema.

Este guia mostrará como criar um ecossistema Hadoop totalmente gerenciado com o Google Cloud Dataproc. Para isso, você precisará de uma conta do Google Cloud Platform e do Google Cloud SDK instalado em sua máquina.

1. Crie uma conta do Google Cloud Platform

Se você ainda não tem uma conta do Google Cloud Platform, você pode criar uma gratuitamente aqui.

1. Instale o Google Cloud SDK

Para instalar o Google Cloud SDK, você pode seguir as instruções aqui.

1. Criar um cluster Hadoop

Para criar um cluster Hadoop, você pode usar o seguinte comando:

```plaintext
gcloud dataproc clusters create my-cluster \
  --region us-central1 \
  --zone us-central1-a \
  --master-machine-type n1-standard-1 \
  --worker-machine-type n1-standard-1 \
  --num-workers 1
```

Este comando criará um cluster Hadoop com um nó mestre e um nó de trabalho na região us-central1.

1. Enviar um programa Spark para o cluster

Para enviar um programa Spark para o cluster, você pode usar o seguinte comando:

```plaintext
gcloud dataproc jobs submit spark my-job \
  --cluster my-cluster \
  --jars /path/to/spark-assembly-2.4.5-hadoop2.6.0-uber.jar \
  --class org.apache.spark.examples.SparkPi \
  --master yarn \
  --deploy-mode cluster \
  --num-executors 1 \
  --executor-cores 1 \
  --executor-memory 1G
```

Este comando enviará um programa Spark que calcula o valor de pi para o cluster.

1. Monitorar seu cluster

Você pode monitorar seu cluster Hadoop usando o seguinte comando:

```plaintext
gcloud dataproc clusters describe my-cluster
```

Este comando exibirá informações sobre o cluster, incluindo o status dos nós, o uso de recursos e os logs.

Com o Google Cloud Dataproc, você pode criar e gerenciar um ecossistema Hadoop totalmente gerenciado em minutos. Você pode usar o Dataproc para executar programas Spark, Hadoop e MapReduce, e pode escalar seu cluster conforme necessário. O Dataproc é a maneira mais fácil de começar a usar o Hadoop no Google Cloud Platform.

O Google Cloud Dataproc é um serviço totalmente gerenciado que permite executar o ecossistema Apache Spark e Apache Hadoop no Google Cloud Platform. Ele fornece uma maneira fácil e rápida de criar clusters Hadoop, gerenciar recursos, executar tarefas e monitorar seu ecossistema.

Este guia mostrará como criar um ecossistema Hadoop totalmente gerenciado com o Google Cloud Dataproc. Para isso, você precisará de uma conta do Google Cloud Platform e do Google Cloud SDK instalado em sua máquina.

1. Crie uma conta do Google Cloud Platform

Se você ainda não tem uma conta do Google Cloud Platform, você pode criar uma gratuitamente aqui.

1. Instale o Google Cloud SDK

Para instalar o Google Cloud SDK, você pode seguir as instruções aqui.

1. Criar um cluster Hadoop

Para criar um cluster Hadoop, você pode usar o seguinte comando:

```plaintext
gcloud dataproc clusters create my-cluster \
  --region us-central1 \
  --zone us-central1-a \
  --master-machine-type n1-standard-1 \
  --worker-machine-type n1-standard-1 \
  --num-workers 1
```

Este comando criará um cluster Hadoop com um nó mestre e um nó de trabalho na região us-central1.

1. Enviar um programa Spark para o cluster

Para enviar um programa Spark para o cluster, você pode usar o seguinte comando:

```plaintext
gcloud dataproc jobs submit spark my-job \
  --cluster my-cluster \
  --jars /path/to/spark-assembly-2.4.5-hadoop2.6.0-uber.jar \
  --class org.apache.spark.examples.SparkPi \
  --master yarn \
  --deploy-mode cluster \
  --num-executors 1 \
  --executor-cores 1 \
  --executor-memory 1G
```



Este comando enviará um programa Spark que calcula o valor de pi para o cluster.

1. Monitorar seu cluster

Você pode monitorar seu cluster Hadoop usando o seguinte comando:

```plaintext
gcloud dataproc clusters describe my-cluster
```

Este comando exibirá informações sobre o cluster, incluindo o status dos nós, o uso de recursos e os logs.

Com o Google Cloud Dataproc, você pode criar e gerenciar um ecossistema Hadoop totalmente gerenciado em minutos. Você pode usar o Dataproc para executar programas Spark, Hadoop e MapReduce, e pode escalar seu cluster conforme necessário. O Dataproc é a maneira mais fácil de começar a usar o Hadoop no Google Cloud Platform.



* ### Digital Innovation One

  Código criado para utilização junto a plataforma da Digital Innovation One

  <p align="center"><img src="./DIO.png" width="500"></p>

  ## Desafio GCP Dataproc

  O desafio faz parte do curso na plataforma da Digital Innovation One:

  __*Criando um ecossitema Hadoop totalmente gerenciado com Google Cloud Platform*__

  O desafio consiste em efetuar um processamento de dados utilizando o produto Dataproc do GCP. Esse processamento irá efetuar a contahem das palavras de um livro e informar quantas vezes cada palavra aparece no mesmo.

  ---

  ### Etapas do Desafio

  1. Criar um bucket no Cloud Storage
  1. Atualizar o arquivo ```contador.py``` com o nome do Bucket criado nas linhas que contém ```{SEU_BUCKET}```.
  1. Fazer o upload dos arquivos ```contador.py``` e ```livro.txt``` para o bucket criado (instruções abaixo)
      - https://cloud.google.com/storage/docs/uploading-objects

  1. Utilizar o código em um cluster Dataproc, executando um Job do tipo PySpark chamando ```gs://{SEU_BUCKET}/contador.py```
  1. O Job irá gerar uma pasta no bucket chamada ```resultado```. Dentro dessa pasta o arquivo ```part-00000``` irá conter a lista de palavras e quantas vezes ela é repetida em todo o livro.

  ### Entrega do Resultado

  1. Criar um repositório no GitHub.
  2. Criar um arquivo chamado ```resultado.txt```. Dentro desse arquivo, colocar as 10 palavras que mais são usadas no livro, de acordo com o resultado do Job.
  3. Inserir os arquivo ```resultado.txt``` e ```part-00000``` no repositório e informar na plataforma da Digital Innovation One.

  ---

  ### Considerações Finais

  NOTA: Se o Job mostrar um WARN de Interrupt, basta ignorar. Existe um bug no Hadoop que é conhecido. Isso não impacta no processamento.

  Qualquer outra dúvida, informação ou sugestão, fique a vontade para entrar em contato.

  

  agardecimento especial:    marcelo@smarques.com
