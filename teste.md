# Table of Contents

## [1. Compromised AWS Account Credentials](#compromised-aws-account-credentials)

## [2. Como realizar novo Pix no iti](#como-realizar-novo-Pix-no-iti)

## [3. ](#)

-------

## Compromised AWS Account Credentials

Infosec has identified a security incident related to AWS credentials leakage. Execute the procedure below to either contain or prevent a possible attack.

1. **Run the commands below to remove all permissions from the affected AWS user without revoking credentials:**

   1.1. Find a user with admin IAM permissions:

   ```itau sec iam show group infosec-permissions-admin```

   1.2. Request the removal of all the inline policies from the affected IAM user:
   
   ```itau iam disallow <user> Source```

   1.3. Request a list of all IAM groups the affected user is included:

   ```itau sec iam show <user>```

   1.4. Request the removal of the affected user from all listed groups:

   ```itau sec iam remove <user> <groups>```

2. **Communicate the incident to the relevant stakeholders.**

3. **Notify the affected user:**

    *"Your AWS permissions have been temporarily suspended pending an investigation into a possible compromise. If you have any questions, do not hesitate to contact me or the security team and, for security reasons, please keep the incident private until further notice from Infosec."*

4. **Request an admin IAM user (*see step 1.1.*) to revoke the affected AWS credentials and disable/delete the affected credentials using the AWS console.**

5. **Generate new credentials and a new keypair via AWS console.**

Refer to the [AWS Java Developer Guide](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html) for information on how to work with AWS credentials and to the [Prescriptive Guide](https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/controls-acct.html) for information on how to secure your account.

------

# Como realizar novo Pix no iti

Este tutorial contém as informações necessárias para você realizar uma transferência via Pix, para uma chave não cadastrada, no aplicativo do banco iti.

## Pré-requisitos

* Possuir uma conta no iti. Caso não possua, abra sua conta pelo [site](https://iti.itau/conta-digital/) ou aplicativo no seu celular;
* Possuir a versão mais atualizada do aplicativo do banco iti no seu celular. Instale ou atualize pela [Play Store](https://play.google.com/store/games?device=phone) se o seu celular for Android, ou pela [App Store](https://www.apple.com/br/app-store/) se o seu celular for iPhone.

## Abra o aplicativo

1. Clique em **entrar**;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/01_tela_inicial.jpg" alt="tela inicial" width="150">

2. Digite seu CPF;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/02_login_cpf.jpg" alt="login cpf" width="150">

3. Digite sua senha e clique em **entrar**;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/03_login_senha.jpg" alt="login senha" width="150">

4. Selecione a opção **Pix**.

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/04_opcao_pix.jpg" alt="opcao pix" width="150">

## Realize um novo Pix

1. Clique na opção **transferir**;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/05_transferir.jpg" alt="transferir" width="150">

2. Clique em **fazer novo Pix**;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/06_novo_pix.jpg" alt="novo pix" width="150">

3. Digite a chave Pix para a qual deseja fazer a transferência e clique em **transferir**;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/07_chave_pix.jpg" alt="chave pix" width="150">

4. Digite o valor que deseja transferir e clique em **continuar**;
> Obs: para visualizar o saldo da sua conta, habilite a opção **visualizar**, à direita da tela.

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/08_valor_pix.jpg" alt="valor pix" width="150">

5. Confirme os dados do pagamento e clique em **pagar**;
> Obs: caso deseje realizar outras transferências para esse mesmo contato no futuro, sem precisar digitar a chave Pix novamente, salve esse contato habilitando a opção **Salvar contato**.

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/09_dados_pix.jpg" alt="dados pix" width="150">

6. Digite sua senha para confirmar a transferência;

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/10_senha_pix.jpg" alt="senha" width="150">

7. Pronto! Sua transferência foi realizada. Clique em **ver comprovante** para conferir os dados da transação.

<img src="https://github.com/tiannamen/squad_doc/blob/main/images/11_ver_comprovante.jpg" alt="comprovante" width="150">
