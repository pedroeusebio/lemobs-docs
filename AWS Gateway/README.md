# AWS Storage Gateway

### O que é ?

É um serviço que conecta um dispositivo de software no local ao armazenamento baseado na nuvem para oferecer uma integração direta e segura entre o ambiente de TI local de uma organização e a infraestrutura de armazenamento da AWS.

Ele oferece desempenho de baixa latência mantendo os dados acessadso com frequência no local e armanzenando com segurança todos os dados cirptografados no Amazon S3 ou no Amazon Glacier.

### Capacidade

O volume do Gateway-Stored podem varias de 1GiB até 16TiB de tamanho, além disso, cada Gateway pode ser configurado para armazenar até 32 volumes, podendo chegar até 512TiB \(0,5 PiB\).

### Como Funciona![](http://docs.aws.amazon.com/storagegateway/latest/userguide/images/aws-storage-gateway-stored-diagram.png)

After you've installed the AWS Storage Gateway software appliance—the virtual machine \(VM\)—on a host in your data center and activated it, you can create gateway _storage volumes_ and map them to on-premises direct-attached storage \(DAS\) or storage area network \(SAN\) disks. You can start with either new disks or disks already holding data. You can then mount these storage volumes to your on-premises application servers as iSCSI devices. As your on-premises applications write data to and read data from a gateway's storage volume, this data is stored and retrieved from the volume's assigned disk.

To prepare data for upload to Amazon S3, your gateway also stores incoming data in a staging area, referred to as an _upload buffer_. You can use on-premises DAS or SAN disks for working storage. Your gateway uploads data from the upload buffer over an encrypted Secure Sockets Layer \(SSL\) connection to the AWS Storage Gateway service running in the AWS cloud. The service then stores the data encrypted in Amazon S3.

You can take incremental backups, called _snapshots_, of your storage volumes. The gateway stores these snapshots in Amazon S3 as Amazon EBS snapshots. When you take a new snapshot, only the data that has changed since your last snapshot is stored. You can initiate snapshots on a scheduled or one-time basis. When you delete a snapshot, only the data not needed for any other snapshot is removed.

### SetUp

O link abaixo levará a plataforma da AWS, onde contém todas as informações necessárias para configurar o serviço. Além disso, possui um passo-a-passo bem detalhado para que o serviço contratado seja o ideal para a aplicação.

link :  [http:\/\/docs.aws.amazon.com\/pt\_br\/storagegateway\/latest\/userguide\/GettingStarted-common.html](http://docs.aws.amazon.com/pt_br/storagegateway/latest/userguide/GettingStarted-common.html)

