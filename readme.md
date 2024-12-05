# Nomes: Nicolas Enzo Yassuda, Kevin Nagayuki Shinohara
```markdown
# Testes da Linguagem de Programação

Este README contém uma série de testes realizados para validar a sintaxe e o comportamento de comandos de uma linguagem de programação projetada para controlar um robô, incluindo operações como movimentação, rotação, leituras de sensores, condicionais e loops.

## Testes

### Teste 1: Comandos de Limpeza Simples
**Código Fonte:**
```plaintext
_startclean
_stopclean
```
**Saída Esperada:**
```plaintext
Iniciando a limpeza
Parando a limpeza
```

---

### Teste 2: Leitura de Sensores
**Código Fonte:**
```plaintext
_readSensor 1
_readSensor 2
_readSensor 3
```
**Saída Esperada:**
```plaintext
Lendo o sensor 1
Lendo o sensor 2
Lendo o sensor 3
```

---

### Teste 3: Declaração e Atribuição de Variáveis
**Código Fonte:**
```plaintext
int contador
bool ativo

contador = 10
ativo = true

contador++
contador--
_readSensor 10
ativo = false
```
**Saída Esperada:**
```plaintext
Lendo o sensor 10
```

---

### Teste 4: Comandos de Movimento e Rotação
**Código Fonte:**
```plaintext
_move frente 5
_rotate esquerda 90
_move tras 3
_rotate direita 45
```
**Saída Esperada:**
```plaintext
Movendo frente por 5 unidades
Rotacionando esquerda por 90 graus
Movendo tras por 3 unidades
Rotacionando direita por 45 graus
```

---

### Teste 5: Comando de Repetição (_repeat)
**Código Fonte:**
```plaintext
_repeat 3 {
    _move frente 2
    _rotate direita 90
}
```
**Saída Esperada:**
```plaintext
Movendo frente por 2 unidades
Rotacionando direita por 90 graus
Movendo frente por 2 unidades
Rotacionando direita por 90 graus
Movendo frente por 2 unidades
Rotacionando direita por 90 graus
```

---

### Teste 6: Comando Condicional (_if) e (_returndock)
**Código Fonte:**
```plaintext
int status
status = 1

_if status == 1 {
    _returndock
}
```
**Saída Esperada:**
```plaintext
Retornando à base de carregamento
```

---

### Teste 7: Loop Condicional (_while)
**Código Fonte:**
```plaintext
int contador
contador = 0

_while (contador < 3) {
    _move frente 1
    contador = contador + 1
}
```
**Saída Esperada:**
```plaintext
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Análise concluída com sucesso!
```

---

### Teste 8: Operações Matemáticas Complexas
**Código Fonte:**
```plaintext
int resultado
resultado = (2 + 3) * 4 - 5 / 5
_readSensor resultado
```
**Saída Esperada:**
```plaintext
Lendo o sensor 19
```

---

### Teste 9: Operações Lógicas
**Código Fonte:**
```plaintext
bool a
bool b
bool c

a = true
b = false
c = a and b
_readSensor c
c = a or b
_readSensor c
c = !a
_readSensor c
c = true and a
_readSensor c
```
**Saídas Esperadas:**
```plaintext
Lendo o sensor 0
Lendo o sensor 1
Lendo o sensor 0
Lendo o sensor 1
```

---

### Teste 10: Uso de Parênteses em Expressões
**Código Fonte:**
```plaintext
int resultado
resultado = 2 + 3 * 4
_readSensor resultado
resultado = (2 + 3) * 4
_readSensor resultado
```
**Saída Esperada:**
```plaintext
Lendo o sensor 14
Lendo o sensor 20
```

---

### Teste 11: Incremento e Decremento
**Código Fonte:**
```plaintext
int contador
contador = 5
contador++
contador--
contador--
_readSensor contador
```
**Saída Esperada:**
```plaintext
Lendo o sensor 4
```

---

### Teste 12: Operações de Comparação
**Código Fonte:**
```plaintext
int a
int b
bool resultado

a = 10
b = 5
resultado = a > b
_readSensor resultado
resultado = a < b
_readSensor resultado
resultado = a == b
_readSensor resultado
resultado = a > true
_readSensor resultado
```
**Saídas Esperadas:**
```plaintext
Lendo o sensor 1
Lendo o sensor 0
Lendo o sensor 0
Lendo o sensor 1
```

---

### Teste 13: Comando de Limpeza com Condição
**Código Fonte:**
```plaintext
bool iniciar
iniciar = true

_if iniciar {
    _startclean
    _move frente 3
    _stopclean
}
```
**Saída Esperada:**
```plaintext
Iniciando a limpeza
Movendo frente por 3 unidades
Parando a limpeza
```

---

### Teste 14: Leitura e Uso de Sensores em Condições
**Código Fonte:**
```plaintext
int distancia
int sujeira
bool limpar

distancia = 5
sujeira = 3
limpar = false

_if distancia < 10 {
    _move frente distancia
}

_if sujeira > 2 {
    _cleanthrash
    limpar = true
}

_if limpar {
    _startclean
}
```
**Saída Esperada:**
```plaintext
Movendo frente por 5 unidades
Limpando o lixo
Iniciando a limpeza
```

---

### Teste 15: Controle de Fluxo com Múltiplos Blocos
**Código Fonte:**
```plaintext
int i
int j
bool continuar

i = 0
j = 0
continuar = true

_while (i < 2) {
    _repeat 2 {
        _move frente 1
        j = j + 1
    }
    i = i + 1
    _if j == 4 {
        continuar = false
    }
}
```
**Saída Esperada:**
```plaintext
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Movendo frente por 1 unidades
```

---

## Conclusão

Estes testes demonstram os diversos comportamentos da linguagem de programação, como a execução de comandos simples, operações matemáticas e lógicas, controle de fluxo com condicionais e loops, e interação com sensores. Todos os testes foram bem-sucedidos, com as saídas correspondendo às expectativas.

```

Esse formato segue o padrão de markdown para facilitar a leitura e organização dos testes, proporcionando uma visão clara e concisa dos códigos e resultados esperados.
