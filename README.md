<div align="center">
  <h1>MySQL</h1>
  <p>
      <a href="https://opensource.org/licenses/MIT">
          <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow.svg">
      </a>
      <a href="#">
          <img alt="License" src="https://img.shields.io/github/languages/count/magdacastro/MySQL">
      </a>
      <a href="#">
          <img alt="License" src="https://img.shields.io/github/last-commit/magdacastro/MySQL">
      </a>
      <a href="#">
          <img alt="License" src="https://img.shields.io/github/followers/magdacastro?style=social">
      </a>
  </p>
</div>

<b style="font-size:12px;">Exercício 1:</b> Crie um banco de dados para um sistema de tarefas
e crie uma tabela de tarefas no mysql para armazenar os dados do array abaixo:

```Javascript
[
  { id: 1, description: 'Criar um projeto básico', completed: false },
  { id: 2, description: 'Colocar o lixo para fora até as 19h', completed: true },
  { id: 3, description: 'Fazer o jantar até as 22h', completed: true },
  { id: 4, description: 'Reunião de alinhamento dia 18/07 as 14h', completed: true },
  { id: 5, description: 'Reunião de alinhamento projeto bradesco 18/07 as 16h', completed: false },
  { id: 6, description: 'Criar conteúdo da aula', completed: false }
]
```

```SQL
create database task_systems;
use task_systems;

create table mytasks (
	id int not null AUTO_INCREMENT,
	description varchar(255) not null,
	completed bool not null,
	primary key (id)
);
```

<b style="font-size:12px;">Exercício 2:</b> Crie uma query para inserir todos os dados do array do exercício anterior.

```SQL
insert into mytasks (description, completed ) values
('Criar um projeto básico', false),
('Colocar o lixo para fora até as 19h', true),
('Fazer o jantar até as 22h', true),
('Reunião de alinhamento dia 18/07 as 14h', true),
('Reunião de alinhamento projeto bradesco 18/07 as 16h', false),
('Criar conteúdo da aula', false);

```

<b style="font-size:12px;">Exercício 3:</b> Crie uma query para listar todas as tarefas.

```SQL
select * from mytasks;
```

<b style="font-size:12px;">Exercício 4:</b> Crie uma query para listar uma tarefa pelo id 2.

```SQL
select * from mytasks where id = 2;
```

<b style="font-size:12px;">Exercício 5:</b> Crie um query para inserir uma tarefa na tabela.

```SQL
insert into mytasks (description, completed ) values ('Levar o cachorro para passear', true);
```

<b style="font-size:12px;">Exercício 6:</b> Crie uma query para atualizar uma tarefa na tabela.

```SQL
update mytasks set description = 'Entregar projeto finalizado até 13/08' where id = 7;
```

<b style="font-size:12px;">Exercício 7:</b> Crie uma query para remover uma tarefa da tabela.

```SQL
delete from mytasks where id = 1;
```
