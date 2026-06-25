# Análise — as 3 responsabilidades da classe `Academia` (v1.0)

**Sua tarefa (Parte 2 da atividade, 0,3):** responder com **suas palavras**
(2–4 frases por item), olhando o arquivo `academia.py` da pasta da aula.
Substitua cada `...` pela sua resposta.

---

## 1. Quais são as 3 responsabilidades grudadas na classe `Academia`?
Escreva no formato "a classe faz **X** e **Y** e **Z**":

> a classe academia faz ligação com o usuário(entrada e saida de dados)
> regra de negócio (calcula o valor do plano e também controla o check-ins)
> e faz notificação de mensagem simulando whatsapp para os alunos.

## 2. Aponte, no código, **uma linha** de cada responsabilidade
(diga o número da linha e cole o trecho)

- **Regra de negócio** (cálculo / contagem): linha 17 — 20 `if plano == "1": valor = 100.0`
- **Tela** (interface com o usuário): linha 14 — `nome = input("Nome do aluno: ")`
- **Notificação** (aviso ao aluno): linha 29 — `print(f"[WhatsApp para {nome}] Bem-vindo(a) à FitPará! Mensalidade: R${valor:.2f}.")`

## 3. Como o SRP separa essas responsabilidades?
Diga **em qual componente** cada responsabilidade passa a morar:

> com o SRP criaria diferentes componentes, ex: a regra de negócio ficaria em uma classe de serviço (ex: cálculo de planos e check-ins), a tela ficaria em uma camada de interface (menu e inputs), e a notificação ficaria em um serviço próprio de mensagens. assim mesmo que alterace uma classe não afetaria as outras.

## 4. Por que ficou melhor? Cite **um** RNF
(manutenibilidade, testabilidade **ou** extensibilidade — veja `docs/requisitos.md`)
e explique em 1–2 frases:

> Ficou melhor em manutenibilidade, porque quando a regra de cálculo do plano muda, não vai ser preciso mexer na parte da interface nem na da notificação. Isso reduz erros e facilita corrigir ou atualizar o sistema no futuro.
