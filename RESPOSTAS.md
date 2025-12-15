# Respostas do Trabalho - Pipeline de ML

## Identificação do Grupo

- **Integrantes:**
  1. Nome: Anna Elisa de Lara
  2. Nome: Giselle Oliveira Dias
  3. Nome: Vitor Zago Capanema
  4. Nome: ---

---

## Parte 1: Resultados do Pipeline

### 1.1 O pipeline executou sem erros?

<!-- Marque com X a opção correta -->

- [ X ] Sim
- [ ] Não

### 1.2 F1-Score obtido:

<!-- Copie o valor exibido ao final da execução -->

```
F1-Score: _______
```

### 1.3 Cole aqui o output final do pipeline:

<!-- Execute: python main.py e copie a saída -->

```
(cole o output aqui)
```

---

## Parte 2: Interpretação dos Resultados

### 2.1 O modelo é bom ou ruim? Por quê?

<!-- Considere: F1 de 0.5 seria jogar moeda. Acima de 0.5 = melhor que aleatório. -->

### 2.2 O dataset é balanceado ou desbalanceado? Como você descobriu?

<!-- Dica: veja a proporção da variável target na exploração dos dados -->

respondeu_campanha
0 0.5606
1 0.4394
Name: proportion, dtype: float64
--> Existe uma proporção ligeiramente maior de casos "não respodeu" (0). Isso pode fazer
com que o modelo tenda a fazer essa previsão, gerando certo enviesamento e deixando
de trazer casos importantes de previsibilidade de resposta.

### 2.3 Por que usamos F1-Score e não apenas Accuracy neste caso?

<!-- Dica: pense no que aconteceria se o modelo previsse sempre 0 -->

---

## Parte 3: Validação de Dados

### 3.1 Liste as validações Pandera que você implementou:

<!-- Descreva cada validação que você adicionou -->

1. cliente_id: Column(int, nullable=False, unique=True),
2. idade: Column(int, Check.in_range(18, 80)),
3. renda_mensal: Column(float, Check.in_range(1000, 50000)),
4. score_credito: Column(float, Check.in_range(300, 850)),
5. respondeu_campanha: Column(int, Check.isin([0, 1])),

### 3.2 Por que validar dados ANTES de treinar o modelo?

<!-- Pense no contexto de produção: o que aconteceria se dados inválidos entrassem no modelo? -->

Garbage in, garbage out - é necessário garantir que os dados estão adequados para entrar
no modelo, sob o risco de comprometer sua qualidade/capacidade preditiva.

---

## Parte 4: Versionamento

### 4.1 Liste os commits que vocês fizeram (copie do git log):

<!-- Execute: git log --oneline e cole aqui -->

```
(cole o output do git log aqui)
```

### 4.2 Por que mensagens de commit descritivas são importantes?

<!-- Pense: se outra pessoa olhar o histórico, vai entender o que foi feito? -->

É necessário que se tenha um hitórico claro porque possibilita saber o que
mudou e quem mudou. Isso permite fazer correções mais rápidas, voltar para uma versão anterior
(se houver necessidade) e comparar mudanças para entender o que funciona melhor.

---

## Parte 5: Reflexão (Opcional)

### 5.1 Qual foi a maior dificuldade do grupo?

### 5.2 O que vocês fariam diferente se fossem refazer?

---

**Data de entrega:** **_/_**/**\_\_**
