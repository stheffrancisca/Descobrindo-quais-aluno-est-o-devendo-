# Descobrindo-quais-aluno-est-o-devendo-
Descobrindo quais aluno estão devendo.


### Você recebeu uma lista de alunos da Arroba Treinamentos e precisa descobrir quantos alunos e quais aluno estão devendo ainda algum pagamento do curso. O curso custa 2.000 reais e os pagamentos dos alunos são representados por uma lista de valores já pagos no dicionário de alunos


pagamentos_alunos = {
    "André": [2000],
    "Fulano": [1000, 1000],
    "Ciclano": [500, 500],
    "Beltrano": [100], 
    "João": [100, 100, 100, 100, 100, 100, 100, 100, 100, 100, 100],
    "Amanda": [200, 300, 250, 250, 500, 400, 100],
    "Lira": [1000],
    "Alon": [10]
}


preco_curso = 2000
qtde_alunos_devendo = 0
for aluno in pagamentos_alunos:
    total_pago = sum(pagamentos_alunos[aluno])
    if total_pago < preco_curso:
        print(aluno, "está devendo", preco_curso - total_pago, "reais")
        qtde_alunos_devendo += 1

print(qtde_alunos_devendo, "estão devendo algum valor")
