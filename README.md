🎓 Mentorship Program
Gestão de mentores e sessões de mentoria no ServiceNow.

Projeto de aprendizagem desenvolvido durante o Bootcamp AOOP de ServiceNow, com foco na construção de uma aplicação, modelagem de dados e controle de acesso por papéis e ACLs.



✨ Sobre o projeto
O Mentorship Program organiza o cadastro de mentores e o registro de sessões de mentoria. A aplicação também serve como exercício prático de segurança: diferentes usuários acessam os registros conforme as permissões configuradas.

O desenvolvimento acontece em uma Personal Developer Instance (PDI), com versionamento integrado ao GitHub.
🧩 Funcionalidades
- Cadastro e manutenção de mentores.
- Criação e acompanhamento de sessões de mentoria.
- Registro de feedback nas sessões.
- Controle de acesso por roles e Access Control Lists (ACLs).
- Testes de acesso com impersonação de usuários.
- Versionamento da aplicação pelo Source Control do ServiceNow.
🗂️ Estrutura funcional
Componente	Finalidade
Mentor	Cadastro dos mentores do programa.
Mentorship Session	Registro das sessões de mentoria e seus feedbacks.
Roles e ACLs	Definição das permissões de acesso aos recursos e registros.


Os nomes técnicos das tabelas, campos, papéis e regras estão nos arquivos exportados pelo ServiceNow.
🔐 Segurança e validação
O projeto explora permissões de criação, leitura, edição e exclusão, incluindo restrições sobre registros de outros usuários e acesso ao campo de feedback.

As validações manuais realizadas durante os exercícios incluem:
- Criação e edição de mentor com o usuário responsável pelo registro.
- Tentativa de edição de mentor pertencente a outro usuário.
- Criação de sessão e tentativa de alteração de sessão de outro usuário.
- Verificação do acesso ao feedback e da exclusão de registros.
- Comparação da visibilidade de registros com usuários diferentes.
As ACLs presentes na aplicação são a referência para o comportamento efetivo de cada papel.
🛠️ Tecnologias e recursos
Recurso	Uso
ServiceNow	Plataforma da aplicação.
App Engine Studio	Construção e configuração da aplicação.
Tables & Forms	Modelagem de dados e formulários.
Roles e ACLs	Controle de acesso.
Source Control / GitHub	Histórico e versionamento dos arquivos da aplicação.
Update Sets / XML	Exportação de uma cópia das configurações da aplicação.


🚀 Instalação em uma PDI
Pelo Git
1. Acesse uma instância de desenvolvimento com as permissões necessárias para importar aplicações.
2. Abra o Studio e localize Import from Source Control.
3. Informe a URL deste repositório:
   https://github.com/douglasamaral1981/servicenow-mentorship-program.git
4. Configure uma credencial com acesso de leitura ao repositório.
5. Selecione a branch sn_instances/dev437324, utilizada pela PDI de origem.
6. Conclua a importação e confira a aplicação, suas dependências e os papéis necessários aos usuários de teste.
Os nomes e a localização dos menus podem variar conforme a versão do ServiceNow.
Por XML
Se você tiver o XML do Update Set exportado:
1. Acesse System Update Sets → Retrieved Update Sets.
2. Selecione Import Update Set from XML e envie o arquivo.
3. Abra o Update Set importado e execute Preview Update Set.
4. Analise e resolva os conflitos ou erros de prévia antes de prosseguir.
5. Execute Commit Update Set e valide a aplicação.
O XML é uma cópia de segurança mantida separadamente. Sua presença neste repositório não é pressuposta.

💾 Versionamento e backup
Branch utilizada pela instância de desenvolvimento:
sn_instances/dev437324
Ao concluir uma atividade, utilize Source control → Commit Changes no ServiceNow e confira o commit no GitHub. As alterações feitas na instância precisam ser enviadas por commit para atualizar a cópia no repositório.

Exemplos de mensagens de commit:
feat: adiciona recurso ao programa de mentoria
fix: corrige permissões de edição de mentores
docs: atualiza instruções do projeto
Para gerar um novo XML da aplicação, abra seu registro em My Company Applications, utilize Publish to Update Set e depois Export to XML no Update Set gerado.
Escopo do backup: o versionamento dos arquivos da aplicação não equivale a um backup completo da PDI. Registros de mentores e sessões, usuários de teste, atribuições de papéis, anexos e outras dependências podem exigir exportação ou configuração adicional. Não presuma que esses dados estão incluídos sem conferir o conteúdo exportado.

📚 Aprendizados
- Modelagem de uma aplicação na plataforma ServiceNow.
- Configuração de tabelas e formulários.
- Uso de papéis e ACLs para controlar acesso.
- Validação de permissões com usuários distintos.
- Integração entre ServiceNow e GitHub.
- Preservação do projeto por versionamento e exportação XML.
👤 Autor
Douglas Amaral
Perfil no GitHub

Projeto educacional em evolução, desenvolvido para praticar os fundamentos de desenvolvimento na plataforma ServiceNow.
