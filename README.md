# 🧩 Agrupamento de Palavras por Prefixo

## 📌 Visão Geral

Este repositório contém uma implementação em Ruby do método `group_by_prefix(words, n)`.  
O objetivo é agrupar palavras com base em um prefixo comum de comprimento **`n`**, atendendo a um conjunto definido de requisitos e passando por uma suíte de testes automatizados.

A solução prioriza **correção**, **legibilidade** e **boas práticas idiomáticas em Ruby**.

---

## 🛠️ Requisitos

O método deve:

- Considerar apenas **strings** com pelo menos `n` caracteres
- Agrupar palavras de forma **case-insensitive** (sem diferenciar maiúsculas de minúsculas)
- Preservar a **forma original** das palavras na saída
- Retornar um **array de arrays**, onde cada subarray contém palavras com o mesmo prefixo

---

## ⚠️ Restrições

- `words` deve ser um `Array`
- `n` deve ser um `Integer` maior que zero
- Elementos que não forem strings devem ser **ignorados**
- Argumentos inválidos devem gerar `ArgumentError`

---

## 🧪 Exemplo de Uso

```ruby
group_by_prefix(["car", "cart", "cat", "bank", "banana"], 2)
# => [["car", "cart", "cat"], ["bank", "banana"]]
```

## ⏱️ Complexidade Esperada

```bash
O(k * m)
```

Onde:

- `k` é o número de palavras
- `m` é o comprimento médio das palavras

## 🧠 Notas de Implementação

A solução utiliza uma abordagem baseada em `Hash`:

- Chave: prefixo normalizado (`word[0, n].downcase`)
- Valor: array com as palavras originais que compartilham o mesmo prefixo

Essa estratégia garante boa performance, clareza no código e facilidade de manutenção.

## ▶️ Executando os Testes

No terminal, execute:

```bash
ruby challenge.rb
```

### Resultado Esperado

- ✔️ Todos os testes passam → mensagem de sucesso
