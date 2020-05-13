Table professores as P {
  id_prof int [pk]
  nome_prof varchar
  cpf_prof varchar
  rg_prof varchar
  sexo_prof int [ref: > S.id]
  dn_prof datetime
  ling_prof varchar
  exp_prof int
}

Table alunos as A {
  id_aluno int
  nome_aluno varchar
  cpf_aluno varchar
  rg_aluno varchar
  dn_aluno date
  endereco_aluno varchar
  cidade_aluno int [ref: > C.id]
  estado_aluno int [ref: > E.id]
  professor int [ref: > P.id_prof]
}
Table Sexo as S{
  id int [pk]
  sexo_desc varchar
}

Table Cidade as C{
  id int [pk]
  nome_cidade varchar
}

Table Estado as E{
  id int [pk]
  nome_estado varchar
}
