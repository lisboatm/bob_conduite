# README - Cálculo do Menor Raio de Conduite

## Descrição

O objetivo deste programa é determinar o menor raio de um conduite circular necessário para acomodar dois cabos circulares de energia, dados os raios desses cabos. O programa calcula o raio do menor círculo que pode englobar ambos os cabos.

## Entrada

- A primeira linha contém um inteiro \( T \) (\( T \leq 10000 \)), indicando o número de casos de teste.
- Para cada caso de teste, há uma linha contendo dois inteiros \( R1 \) e \( R2 \), que representam os raios dos cabos, onde os raios são positivos.

## Saída

- Para cada caso de teste, imprima em uma única linha o menor raio possível do conduite.

## Fórmula

O menor raio do conduite \( R \) pode ser calculado pela fórmula:

\[
R = \max(R1, R2)
\]

onde:
- \( R1 \) = raio do primeiro cabo
- \( R2 \) = raio do segundo cabo

O raio do conduite deve ser igual ao maior dos dois raios, já que o conduite precisa ser grande o suficiente para acomodar ambos os cabos.

## Exemplo de Uso

### Entrada
```
3
1 1
2 8
8 2
```

### Saída
```
1
8
8
```

### Explicação
- No primeiro caso, ambos os raios são 1, então o raio do conduite também será 1.
- No segundo caso, o maior raio é 8, então o raio do conduite será 8.
- No terceiro caso, novamente o maior raio é 8.

## Implementação

O código foi implementado em Python e está estruturado da seguinte maneira:

```python
# Leitura do número de casos de teste
T = int(input())

# Processamento de cada caso de teste
for _ in range(T):
    R1, R2 = map(int, input().split())
    # Cálculo do menor raio do conduite
    menor_raio = max(R1, R2)
    # Impressão do resultado
    print(menor_raio)
```

## Testes

O programa foi testado com os seguintes exemplos:

| Entrada       | Saída |
|---------------|-------|
| 3             |       |
| 1 1           | 1     |
| 2 8           | 8     |
| 8 2           | 8     |

## Considerações Finais

O programa é eficiente e pode processar até 10.000 casos de teste rapidamente, com uma complexidade de \( O(T) \), onde \( T \) é o número de casos de teste. Essa solução é ideal para aplicações que envolvem cálculos geométricos simples.
