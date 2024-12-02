Teste 1 Comandos de Limpeza Simples:
source_code = """
_startclean
_stopclean
"""
Saída 1:
Iniciando a limpeza
Parando a limpeza


Teste 2  Leitura de Sensores:
source_code = """
_readSensor 1
_readSensor 2
_readSensor 3
"""
Saída 2:
Lendo o sensor 1
Lendo o sensor 2
Lendo o sensor 3


Teste 3 Declaração e Atribuição de Variáveis:
source_code = """
int contador
bool ativo

contador = 10
ativo = true

contador++
contador--
_readSensor 10
ativo = false
"""
Saída 3:
Lendo o sensor 10


Teste 4 Comandos de Movimento e Rotação:
source_code = """
_move frente 5
_rotate esquerda 90
_move tras 3
_rotate direita 45
"""
Saída 4:
Movendo frente por 5 unidades
Rotacionando esquerda por 90 graus
Movendo tras por 3 unidades
Rotacionando direita por 45 graus



Teste 5 Comando de Repetição (_repeat):
source_code = """
_repeat 3 {
    _move frente 2
    _rotate direita 90
}
"""
Saída 5:
Movendo frente por 2 unidades
Rotacionando direita por 90 graus
Movendo frente por 2 unidades
Rotacionando direita por 90 graus
Movendo frente por 2 unidades
Rotacionando direita por 90 graus


Teste 6 Comando Condicional (_if) e (_returndock):
source_code = """
int status
status = 1

_if status == 1 {
    _returndock
}
"""
Saída 6:
Retornando à base de carregamento


Teste 7 Loop Condicional (_while):
source_code = """
int contador
contador = 0

_while (contador < 3) {
    _move frente 1
    contador = contador + 1
}
"""
Saida 7:
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Movendo frente por 1 unidades
Análise concluída com sucesso!


Teste 8 Operações Matemáticas Complexas:
source_code = """
int resultado
resultado = (2 + 3) * 4 - 5 / 5
_readSensor resultado
"""
Saída 8:
Lendo o sensor 19


Teste 9 Operações Matemáticas Complexas:
source_code = """
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
"""
Saídas 9:
Lendo o sensor 0
Lendo o sensor 1
Lendo o sensor 0
Lendo o sensor 1


Teste 10 Uso de Parênteses em Expressões:
source_code = """
int resultado
resultado = 2 + 3 * 4
_readSensor resultado
resultado = (2 + 3) * 4
_readSensor resultado
"""
Saída 10:
Lendo o sensor 14
Lendo o sensor 20


Teste 11:
source_code = """
int contador
contador = 5
contador++
contador--
contador--
_readSensor contador
"""
Saída 11:
Lendo o sensor 4



