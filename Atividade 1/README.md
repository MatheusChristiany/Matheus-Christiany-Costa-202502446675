# 🧮 Calculadora API

API simples para realizar operações matemáticas básicas.

## 🚀 Tecnologias

* Node.js
* Express

---

## 📌 Endpoint

### POST `/calcular`

Realiza uma operação matemática entre dois números.

### 📥 Body (JSON)

```json
{
  "numero1": 10,
  "numero2": 5,
  "operacao": "soma"
}
```

### 🔢 Operações disponíveis

* `soma`
* `subtracao`
* `multiplicacao`
* `divisao`

---

## 📤 Resposta de sucesso

```json
{
  "numero1": 10,
  "numero2": 5,
  "operacao": "soma",
  "resultado": 15
}
```

---

## ❌ Erros possíveis

### Parâmetros inválidos

```json
{
  "erro": "Parâmetros obrigatórios: numero1, numero2, operacao"
}
```

### Operação inválida

```json
{
  "erro": "Operação inválida. Use: soma, subtracao, multiplicacao, divisao"
}
```

### Divisão por zero

```json
{
  "erro": "Divisão por zero não é permitida"
}
```

---

## ▶️ Como rodar o projeto

```bash
# Instalar dependências
npm install

# Rodar a API
npm start
```

A API estará disponível em:

```
http://localhost:3000
```

---

## 🧪 Teste com curl

```bash
curl -X POST http://localhost:3000/calcular \
-H "Content-Type: application/json" \
-d '{"numero1":10,"numero2":5,"operacao":"multiplicacao"}'
```
