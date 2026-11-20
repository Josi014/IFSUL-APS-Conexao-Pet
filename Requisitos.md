## 2. Requisitos

### 2.1 Requisitos Funcionais

| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| **RF01** | O sistema deve permitir o cadastro de usuários (nome, e-mail, telefone, cidade e senha) e a solicitação de cadastro de ONGs (nome, CNPJ, endereço, telefone, e-mail e senha), ficando a ONG com status "pendente". | Alta | — |
| **RF02** | O sistema deve permitir login e logout com e-mail e senha. | Alta | RF01 |
| **RF03** | O sistema deve permitir que o administrador aprove ou rejeite cadastros de ONGs. | Alta | RF01, RF02 |
| **RF04** | O sistema deve permitir que ONGs aprovadas cadastrem animais para adoção com espécie, raça, sexo, porte, idade, situação de vacinação e castração e até 5 fotos. | Alta | RF03 |
| **RF05** | O sistema deve permitir que a ONG edite, exclua ou marque como "adotado" os animais que cadastrou. | Média | RF04 |
| **RF06** | O sistema deve permitir que qualquer visitante pesquise animais para adoção por espécie, sexo, porte, idade e cidade e visualize os detalhes e o contato da ONG. | Alta | RF04 |
| **RF07** | O sistema deve permitir que o usuário cadastrado registre pets perdidos ou encontrados com fotos, características, data, local e forma de contato. | Alta | RF02 |
| **RF08** | O sistema deve permitir que qualquer visitante pesquise anúncios de perdidos e encontrados por tipo, espécie, cidade, bairro e período e visualize os detalhes e o contato do autor. | Alta | RF07 |
| **RF09** | O sistema deve permitir que o usuário edite, exclua ou marque como "resolvido" os anúncios que publicou, na área "Meus anúncios". | Média | RF07 |
| **RF10** | O sistema deve permitir que o administrador oculte ou exclua anúncios e bloqueie usuários ou ONGs. | Média | RF02 |
| **RF11** | O sistema deve permitir que o usuário cadastrado denuncie um anúncio, informando o motivo, para análise do administrador. | Baixa | RF02, RF10 |

### 2.2 Requisitos Não Funcionais

| ID | Categoria | Descrição | Prioridade | Depende de |
|---|---|---|---|---|
| **RNF01** | Usabilidade / Portabilidade | O sistema deve ser responsivo, adaptando-se a computadores, tablets e celulares, e funcionar nos principais navegadores. | Alta | — |
| **RNF02** | Desempenho | As páginas de listagem e os resultados de busca devem carregar em até 3 segundos. | Média | RF06, RF08 |
| **RNF03** | Segurança | As senhas devem ser armazenadas com criptografia e toda a comunicação deve ocorrer via HTTPS. | Alta | RF01, RF02 |
| **RNF04** | Segurança | O sistema deve restringir as funcionalidades conforme o perfil do usuário (visitante, usuário, ONG e administrador). | Alta | RF02 |
| **RNF05** | Usabilidade | Um usuário cadastrado deve conseguir publicar um anúncio de pet perdido ou encontrado em no máximo 3 etapas. | Média | RF07 |
| **RNF06** | Privacidade | Os dados pessoais dos usuários devem ser usados apenas para o funcionamento da plataforma, sem serem compartilhados com terceiros. | Alta | RF01 |
| **RNF07** | Manutenibilidade | O código-fonte deve ser versionado no GitHub e organizado em camadas (como MVC), facilitando a correção de erros e a inclusão de novas funcionalidades. | Média | — |

### 2.3 Regras de Negócio

| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| **RN01** | Somente ONGs aprovadas pelo administrador podem cadastrar animais para adoção. Usuários comuns não podem publicar anúncios de adoção. | Alta | RF03, RF04 |
| **RN02** | A plataforma apenas intermedeia o contato entre interessados e ONGs. O processo de adoção (entrevista, termo e entrega do animal) é de responsabilidade exclusiva da ONG. | Alta | RF06 |
