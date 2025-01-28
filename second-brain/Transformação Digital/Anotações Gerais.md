Aqui ficará as informações e algumas anotações pensadas sobre o projeto Transformação Digital.
## Autenticação
---
### Login.

##### Primeiro login de usuário.
- Redirecionamento para uma página de redefinição de senha
- Após a redefinição, um email de confirmação será gerado, e um campo para o envio do código vai aparecer na página.
##### Ideias sobre isso:
- Alterar o metodo de confirmação por código, para um link de autorização que permite a autenticação.

##### Demais logins.
- Ele será autenticado a um módulo que ele está vinculado. Se ele tiver vínculo com mais de um módulo, ele vai ser autenticado sempre no último módulo
- Após autenticação do módulo, a página será renderizada de acordo com as permissões daquele usuário.
- As permissões por padrão estão vinculadas a uma role, então a renderização dinâmica dependerá da role daquele usuário, e das permissões "adicionais" que esse usuário pode ter.

##### Tabelas.

As tabelas necessárias para o módulo de autenticação serão:

- User: Tabela com dados principais de usuário.
- Module: Tabela que conterão os módulos do sistema.
- Role: Tabela com as roles do sistema.
- Permissions: Tabela com as permissões do sistema.
- Group: Tabela com os grupos do sistema.

Existirão as tabelas de relacionamento entre essas tabelas, que serão:
- User_Modules: Relacionamento entre usuários e módulos.
- User_Roles: Relacionamento entre usuários, roles e módulos.
- User_Permissions: Relacionamento entre usuário, módulos e permissões.
- User_Groups: Relacionamento entre usuário e grupos.
- Role_Permissions: Relacionamento entre roles, módulos e permissões.
- Role_Assignable_Roles: Relacionamento entre roles e roles. (Uma role pode se relacionar com nenhuma ou N roles)
- Module_Roles: Relacionamento entre módulos e roles.
- Module_Permissions: Relacionamento entre módulos e permissões.
- Password_Reset_Tokens: Relacionamento com a tabela de usuários, para redefinição de senha.
- Audit_Logs: Tabela para logs de auditoria.

##### Sugestões de tabelas adicionais.
- Failed_Logins: Tabela para logs de tentativas de login.