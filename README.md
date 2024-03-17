# ProjetoBancoDeDados
Primeiro projeto de banco de dados: modelo conceitual
Aluno: Marcelo Nunes
![Captura de tela 2024-03-17 164410](https://github.com/marcelopetroni/ProjetoBancoDeDados/assets/105806830/b218bf22-5f6c-4c5c-b7c5-d0911ac81628)


Descrição do diagrama:

ALUNO:
um a N alunos ESTUDA 'Disciplina',
um a N alunos COMPARECEM a um 'Ambiente' na escola,
um a N alunos PRATICAM 'Exercicio_fisico',
um aluno é REGISTRADO a uma 'Matricula',
um a N alunos REALIZA uma 'Avaliacao',

MATRICULA:
uma matricula é REGISTRADA a um 'Aluno',

PROFESSOR:
um a N professores LECIONA uma 'Aula',
um a N professores CORRIGE a uma 'Avaliacao',
um a N professores MINISTRA 'Disciplina',
um a N professores são COORDENADOS por um 'coordenador'

DISCIPLINA:
uma disciplina é MINISTRADA por um 'professor',
uma disciplina é ESTUDADA por um 'aluno',
Restrição de disjunção: uma disciplina pode ser OBRIGATORIA ou ELETIVA

Entidade extras:
Coordenador é inserido para ter uma relação de coordenar um ou mais 'professor', possui uma restrição de sobreposição em que o(a) coordenador(a) pode ser de diferentes períodos de ensino em um colégio.
Gestor é inserido para ter uma relação de gerenciar um ou mais coordenadores.
Avaliacao é inserido para ter uma relação de ser realizada por um ou mais 'aluno' e corrigida por um ou mais "professor", possui uma restrição de disjunção em que pode ser do tipo ORAL ou ESCRITA.
Exercicio_fisico é inserido para ter uma relação de ser praticada por um ou mais 'aluno' e ocorrida em um ou mais 'ambiente'.
Aula é inserido para ter uma relação de ser assistido por um ou mais 'aluno' e lecionado por um ou mais 'professor', possui uma restrição de disjunção em que pode ser do tipo EAD ou PRESENCIAL.
Ambiente é inserido para ser ocorrido um ou mais 'exercicio_fisico' e comparecida por um ou mais 'aluno', possui uma restrição de disjunção em que pode ser em diferentes localizações da escola (sala de aula, piscina, coordenação, quadra, biblioteca, campus, cantina)
