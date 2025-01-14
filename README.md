# Sistema de Envio de Mensagens e e-mails para integração com o Gestão de Estoque (SGE)

Bem-vindo ao Notify, um projeto webhook e callmebot desenvolvido com intuito didático no Curso Django Master ministrado pela PycodeBR, 
em DjangoRestFramework. Este Projeto possui integração com o SGE para envio de mensagens via WhatsApp e e-mail para o administrador de acordo com movimentações de saídas de produtos.
Este README fornece informações essenciais sobre como configurar e executar o projeto em seu ambiente local.
## Requisitos

Certifique-se de que você tenha os seguintes requisitos instalados em seu sistema:

    Python (versão recomendada: 3.7 ou superior)
    DjangoRestFramework (instalado automaticamente ao seguir as instruções abaixo)
    Outras dependências listadas no arquivo requirements.txt

## Instalação das Dependências

Com o ambiente virtual ativado, instale as dependências do projeto usando o comando:
```
pip install -r requirements.txt
```
## Configurar chave OPENAI_KEY e OPENAI_MODEL
Criar na raiz do projeto em app o arquivo .env e colocar dentro as variáveis:
```
CALLMEBOT_API_URL='https://api.callmebot.com/whatsapp.php'
CALLMEBOT_PHONE_NUMBER='seu_numero_celular'
CALLMEBOT_API_KEY='codigo_callmebot'
EMAIL_HOST='seu_provedor_de_email'
EMAIL_PORT='conf_porta'
EMAIL_USE_TLS='True'
EMAIL_HOST_USER='email_utilizado_envio'
EMAIL_HOST_PASSWORD='sua_senha'
EMAIL_ADMIN_RECEIVER='email_receptor'
```
## Rodar o projeto

Após instalar as dependências, aplique as migrations no banco de dados com o comando:
```
python manage.py migrate
```
Agora o projeto jã pode ser inicializado com o comando:
```
python manage.py runserver
```
Após isso, o sistema estará pronto para ser acessado em: http://localhost:8001.
para que as mensagens sejam enviadas, o SGE deve estar rodando em: http://localhost:8000.
