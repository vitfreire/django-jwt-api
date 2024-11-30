
# **Django JWT API**

Este projeto foi desenvolvido como parte da disciplina **Desenvolvimento Back-End** do curso **Análise e Desenvolvimento de Sistemas** do **Centro Universitário CESMAC**. O objetivo do projeto é implementar uma API em Django com autenticação JWT, seguindo as melhores práticas de segurança e organização de código.

## **Descrição do Projeto**

Este projeto consiste em uma API construída com Django e Django REST Framework. A aplicação utiliza **JSON Web Tokens (JWT)** para autenticação de usuários, implementada com o pacote **Simple JWT**. 

Os endpoints fornecem acesso a dados de usuários cadastrados, com proteção baseada em autenticação para operações restritas.

## **Funcionalidades**
- Geração de tokens JWT para autenticação de usuários.
- Renovação de tokens JWT.
- Operações CRUD para gerenciamento de usuários.
- Endpoint protegido com autenticação JWT.

---

## **Tecnologias Utilizadas**
- **Python**: Linguagem principal do projeto.
- **Django**: Framework web para desenvolvimento back-end.
- **Django REST Framework**: Para criação de APIs RESTful.
- **Simple JWT**: Implementação de autenticação baseada em JWT.

---

## **Instalação e Configuração**

### **1. Clone o Repositório**
```bash
git clone https://github.com/vitfreire/django-jwt-api.git
cd django-jwt-api
```

### **2. Crie e Ative um Ambiente Virtual**
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

### **3. Instale as Dependências**
```bash
pip install -r requirements.txt
```

### **4. Realize as Migrações**
```bash
python manage.py makemigrations
python manage.py migrate
```

### **5. Crie um Superusuário**
Para acessar o painel de administração:
```bash
python manage.py createsuperuser
```
Informe as credenciais conforme solicitado.

### **6. Inicie o Servidor**
```bash
python manage.py runserver
```

---

## **Endpoints**

### **Autenticação**
1. **Gerar Token JWT**  
   Endpoint: `/api/token/`  
   Método: `POST`  
   Corpo da Requisição:
   ```json
   {
     "username": "login",
     "password": "senha"
   }
   ```

2. **Renovar Token**  
   Endpoint: `/api/token/refresh/`  
   Método: `POST`  
   Corpo da Requisição:
   ```json
   {
     "refresh": "<seu_refresh_token>"
   }
   ```

### **Listar Usuários**
- Endpoint: `/api/usuarios/`  
- Método: `GET`  
- Autenticação: Obrigatória (envie o token no cabeçalho `Authorization` como `Bearer <seu_token_access>`).

---

## **Usuário de Teste**
- **Usuário:** `vitoria25`  
- **Senha:** `madeira47#`

---

## **Sobre a Disciplina**
Este projeto foi desenvolvido como requisito da disciplina **Desenvolvimento Back-End**, ministrada no curso **Análise e Desenvolvimento de Sistemas** do **Centro Universitário CESMAC**.

O objetivo da atividade é aplicar conceitos de desenvolvimento back-end, criar APIs RESTful, e implementar autenticação segura com JWT.

---
