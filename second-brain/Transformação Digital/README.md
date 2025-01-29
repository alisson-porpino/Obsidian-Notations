Aqui ficará as informações e algumas anotações pensadas sobre o projeto Transformação Digital.
## [Auth](Auth.md)

O módulo de autenticação será um dos módulos principais do sistema, e será responsável por autenticar usuários e gerenciar as permissões de cada usuário.

O módulo de autenticação tem como base a interação entre as seguintes tabelas:
- User: Tabela com dados principais do usuário para login no sistema.
- User_Profile: Tabela com dados adicionais do usuário.
- Module: Tabela que conterão os módulos do sistema.
- Role: Tabela com as roles do sistema.
- Permissions: Tabela com as permissões do sistema.
- Group: Tabela com os grupos do sistema.

Para permitir a interação entre essas tabelas, existirão as tabelas de relacionamento:
- User_Modules: Tabela de relacionamento entre usuários e módulos.
- User_Roles: Tabela de relacionamento entre usuários, roles e módulos.
- User_Permissions: Tabela de relacionamento entre usuário, módulos e permissões.
- User_Groups: Tabela de relacionamento entre usuário e grupos.
- Role_Permissions: Tabela de relacionamento entre roles, módulos e permissões.
- Role_Assignable_Roles: Tabela de relacionamento entre roles e roles.
- Module_Roles: Tabela de relacionamento entre módulos e roles.
- Module_Permissions: Tabela de relacionamento entre módulos e permissões.

Existem outras duas tabelas diferentes que funcionam de maneira diferente. São elas:
- Password_Reset_Tokens: Tabela para redefinição de senha que interage com a tabela User.
- Audit_Logs: Tabela para logs de auditoria; não interage diretamente com as outras tabelas.

A tabela de "Audit_Logs" será responsável por armazenar logs de auditoria. A interação entre o usuário e os módulos do sistema será armazenada nessa tabela, mas a forma de interação dessa tabela acontece através de um middleware da aplicação, que preenche os dados de todas as ações realizadas pelo usuário. 

A tabela de Password_Reset_Tokens será responsável por armazenar tokens de redefinição de senha.