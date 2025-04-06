# ☁️ Projeto Toshiro Shibakita - Python + Docker + NGINX

Inspirado na história de Toshiro Shibakita, este projeto converte um sistema feito em PHP para Python com Flask, utilizando Docker para criar um ambiente com múltiplos microsserviços e balanceamento de carga com NGINX.

---

## 📦 Tecnologias usadas

- Python 3.11 (Flask)
- Docker e Docker Compose
- NGINX (Load Balancer)
- MySQL (com banco .sql)

---

## 🧭 Como rodar

1. **Clone o repositório**
```bash
git clone https://github.com/vhmedeiros/toshiro-shibakita.git
cd toshiro-shibakita
```

2. **Suba a aplicação**
```bash
docker-compose up --build
```

3. **Acesse no navegador**
```
http://localhost:4500
```
Você verá o nome de um dos containers (flask1, flask2 ou flask3) sendo exibido — o NGINX distribui a carga entre eles.

---

## 🗂️ Estrutura dos containers

- **flask1, flask2, flask3** → Aplicações Python em Flask (com IPs 192.168.1.16–18)
- **db** → MySQL com base de dados importada do `banco.sql`
- **nginx** → Load Balancer acessível em `localhost:4500`

---

## 🧠 Aprendizados

- Criar múltiplos serviços Python com Docker
- Atribuir IPs fixos dentro de uma rede Docker
- Usar NGINX para balanceamento
- Iniciar banco MySQL com script SQL

---

## 📘 Créditos

Projeto baseado em desafio prático da [Digital Innovation One](https://dio.me), adaptado para Python por Victor.
