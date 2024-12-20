🎯 Dica de Dev: Proteja suas Variáveis Sensíveis com .env!

Se você trabalha com desenvolvimento, já sabe como é importante proteger informações como senhas, chaves de API e credenciais de banco de dados. Nada pior do que cometer o erro de subir essas informações no repositório, né? 🫣

Uma das melhores práticas é usar um arquivo .env junto com a biblioteca python-dotenv. Quer ver como é fácil? 👇



1️⃣ Instale o python-dotenv:

pip install python-dotenv



2️⃣ Crie o arquivo .env:

No diretório do projeto, adicione:

# Banco de dados

DB_HOST=localhost

DB_PORT=5432

DB_USER=meu_usuario

DB_PASSWORD=minha_senha



# Chave secreta

SECRET_KEY=minha_chave_super_secreta

3️⃣ Carregue as variáveis no código:

from dotenv import load_dotenv

import os



# Carrega as variáveis do .env

load_dotenv()



# Acessa as variáveis

db_host = os.getenv("DB_HOST")

db_user = os.getenv("DB_USER")

secret_key = os.getenv("SECRET_KEY")



print(f"Conectando ao banco em {db_host} com o usuário {db_user}. 🔐")

4️⃣ Adicione o .env ao .gitignore:

Certifique-se de que o .env não vai para o repositório:

echo ".env" >> .gitignore

Com isso, suas informações sensíveis ficam protegidas, e o código ganha uma dose extra de organização e segurança. 🚀

📌 Dica bônus: Em produção, prefira configurar as variáveis diretamente no servidor (Heroku, AWS, Docker, etc.) para aumentar a segurança!
