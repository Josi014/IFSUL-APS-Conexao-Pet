## 2. Requisitos

### 2.1 Requisitos Funcionais

| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| **RF01** | O sistema deve permitir que o usuário se cadastre informando nome, e-mail, telefone, cidade e senha. |
| **RF02** | O sistema deve permitir que o usuário cadastrado faça login com e-mail e senha e encerre a sessão (logout). |
| **RF03** | O sistema deve permitir que uma ONG solicite cadastro informando nome, CNPJ, endereço, telefone e e-mail, ficando com status "pendente" até a aprovação. |
| **RF04** | O sistema deve permitir que o administrador aprove ou rejeite solicitações de cadastro de ONGs. |
| **RF05** | O sistema deve permitir que a ONG aprovada cadastre um animal para adoção com nome, espécie, raça, sexo, porte, idade aproximada, descrição, situação de vacinação e castração e até 5 fotos. |
| **RF06** | O sistema deve permitir que a ONG edite, exclua ou marque como "adotado" os animais que cadastrou. |
| **RF07** | O sistema deve permitir que qualquer visitante pesquise animais para adoção filtrando por espécie, sexo, porte, idade e cidade. |
| **RF08** | O sistema deve exibir a página de detalhes do animal com suas fotos, informações e os dados de contato da ONG responsável. |
| **RF09** | O sistema deve permitir que o usuário cadastrado registre um pet perdido informando espécie, características, fotos, data e local do desaparecimento e forma de contato. |
| **RF10** | O sistema deve permitir que o usuário cadastrado registre um animal encontrado informando espécie, características, fotos, data e local onde foi encontrado e forma de contato. |
| **RF11** | O sistema deve permitir que qualquer visitante pesquise anúncios de pets perdidos e encontrados filtrando por tipo (perdido/encontrado), espécie, cidade, bairro e período. |
| **RF12** | O sistema deve permitir que o autor de um anúncio de perdido ou encontrado o marque como "resolvido", removendo-o das buscas ativas. |
| **RF13** | O sistema deve permitir que o usuário visualize, edite e exclua os anúncios que publicou na área "Meus anúncios". |
| **RF14** | O sistema deve permitir que o administrador oculte ou exclua anúncios e bloqueie usuários ou ONGs. |
| **RF15** | O sistema deve permitir que o usuário cadastrado denuncie um anúncio, informando o motivo da denúncia, para análise do administrador. |

### 2.2 Requisitos Não Funcionais

| ID | Categoria | Descrição | Prioridade | Depende de |
|---|---|---|---|---|
| **RNF01** | Usabilidade / Portabilidade | O sistema deve ser responsivo, adaptando-se a computadores, tablets e celulares, e funcionar nos principais navegadores.|
| **RNF02** | Desempenho | As páginas de listagem e os resultados de busca devem carregar em até 3 segundos. |
| **RNF03** | Segurança | As senhas devem ser armazenadas com criptografia e toda a comunicação deve ocorrer via HTTPS. |
| **RNF04** | Segurança | O sistema deve restringir as funcionalidades conforme o perfil do usuário (visitante, usuário, ONG e administrador). |
| **RNF05** | Usabilidade | Um usuário cadastrado deve conseguir publicar um anúncio de pet perdido ou encontrado em no máximo 3 etapas. |
| **RNF06** | Privacidade | Os dados pessoais dos usuários devem ser usados apenas para o funcionamento da plataforma, sem serem compartilhados com terceiros. |
| **RNF07** | Manutenibilidade | O código-fonte deve ser versionado no GitHub e organizado em camadas (como MVC), facilitando a correção de erros e a inclusão de novas funcionalidades. |

### 2.3 Regras de Negócio

| ID | Descrição | Prioridade | Depende de | 
|---|---|---|---|
| **RN01** | Somente ONGs aprovadas pelo administrador podem cadastrar animais para adoção. Usuários comuns não podem publicar anúncios de adoção. |
| **RN02** | A plataforma apenas intermedeia o contato entre interessados e ONGs. O processo de adoção (entrevista, termo e entrega do animal) é de responsabilidade exclusiva da ONG. |
