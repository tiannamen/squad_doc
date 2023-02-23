# Table of Contents

## [1. Compromised AWS Account Credentials](#compromised-aws-account-credentials)

## [2. Como fazer um novo Pix no iti](#como-fazer-um-novo-Pix-no-iti)

### [2.1. Pré-requisitos](#pr%C3%A9-requisitos)

### [2.2. Abra o aplicativo](#abra-o-aplicativo)

### [2.3. Faça um novo Pix](#fa%C3%A7a-um-novo-pix)

## [3. Como utilizar o ChatGPT via Python](#como-utilizar-o-chatgpt-via-python)

### [3.1. Pré-requisitos](#pr%C3%A9-requisitos-1)

### [3.2. Utilizando o script](#utilizando-o-script)

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

# Como fazer um novo Pix no iti

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

## Faça um novo Pix

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

----------

# Como utilizar o ChatGPT via Python

Este tutorial vai te guiar nos passos necessários para utilizar o ChatGPT via script em Python. Isso possibilita a utilização da ferramenta mesmo que o sistema da OpenAI não esteja funcionando por excesso de usuários.

## Pré-requisitos

* Python 3.8 ou acima - caso não possua, realize o [download no site python.org](https://www.python.org/downloads/release/python-3112/). Em caso de dúvidas, consulte a [documentação disponível](https://docs.python.org/).
* API Key do ChatGPT - crie sua API Key no [site da OpenAI](https://platform.openai.com/account/api-keys).

## Utilizando o script

Agora que você já possui o Python em versão 3.8 ou superior, é possível utilizar o ChatGPT diretamente no seu terminal de comando, através de um simples script. Veja o tutorial abaixo para executar o script corretamente. 

> Para testar o correto funcionamento do Python, execute o comando: ```python --version```. 
Se a instalação foi bem sucedida, esse comando deverá retornar a versão do Python. 

1. Abra o prompt de comando (CMD) do seu computador e execute o seguinte comando para instalar o gerenciador de pacotes do Python (pip):

```winget install --id=lencx.ChatGPT -e```

2. Crie um novo arquivo com a extensão .py e cole o seguinte script:

```import openai

API_KEY = "API Key"

# Set the API key
openai.api_key = API_KEY

# Use the ChatGPT model to generate text
model_engine = "text-davinci-002"
while (True):
    question = input("Question: ")
    prompt = question
    completion = openai.Completion.create(engine=model_engine, prompt=prompt, max_tokens=1024, n=1,stop=None,temperature=0.7)
    message = completion.choices[0].text
    print("ChatGPT: " + message + "\n")
 ```

4. Substitua "API Key" pelas informações da sua API Key gerada no site da OpenAI [(veja os pré-requisitos)](#pré-requisitos);
5. Salve o arquivo com o nome de sua escolha e com a extensão .py - exemplo (chatgpt.py);
6. No seu terminal (git bash ou cmd), navegue até o local onde o arquivo foi salvo (utilize o comando `cd`) e execute o comando: ```python nome do arquivo.py``` - exemplo ```python chatgpt.py```. Ao executar esse comando, aparecerá a opção de digitar sua pergunta no próprio terminal, e a resposta aparecerá logo em seguida
7. Pronto! Agora você pode utilizar as funcionalidades do ChatGPT, mesmo que a rede da OpenAI esteja sobrecarregada.
