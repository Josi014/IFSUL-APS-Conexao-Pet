# 🐾 Conexão Pet

> Plataforma que conecta pessoas, ONGs e instituições de proteção animal para facilitar a **adoção** de animais e a **busca por pets perdidos e encontrados**.

## 1. Descrição e delimitação do escopo

### 1.1 Cenário do sistema

O **Conexão Pet** é uma plataforma web que centraliza, em um único lugar, a divulgação de animais disponíveis para adoção e de pets perdidos ou encontrados.

**Propósito:** aproximar pessoas interessadas em adotar das ONGs e instituições de proteção animal, além de ajudar tutores a reencontrar seus animais com o apoio da comunidade.

**Contexto de uso:** o sistema é acessado pela internet, tanto em computadores quanto em celulares. ONGs utilizam a plataforma para divulgar os animais sob seus cuidados; o público em geral a utiliza para procurar um pet para adotar, divulgar o desaparecimento de um animal ou informar que encontrou um animal na rua.

### 1.2 Problema a ser resolvido

Atualmente, a divulgação de animais para adoção e de pets perdidos está espalhada em redes sociais, grupos de mensagens e cartazes, o que gera:

- **Dificuldade de encontrar informações:** quem quer adotar precisa procurar em vários lugares diferentes.
- **Baixa visibilidade das ONGs:** instituições pequenas têm pouco alcance para divulgar seus animais.
- **Perda de informações:** publicações sobre pets perdidos se perdem rapidamente em feeds e grupos.
- **Comunicação desorganizada:** não há um canal padronizado entre adotantes, tutores e instituições.

O Conexão Pet resolve esses problemas ao reunir todas essas informações em uma única plataforma, com busca por filtros, dados padronizados e acesso direto aos contatos responsáveis.

### 1.3 Público-alvo

| Perfil | Como usa a plataforma |
|---|---|
| **Interessados em adotar** | Buscam animais disponíveis e entram em contato com as ONGs |
| **Tutores de pets perdidos** | Divulgam o desaparecimento do animal e acompanham registros de pets encontrados |
| **Pessoas que encontraram um animal** | Registram o animal encontrado para ajudar a localizar o tutor |
| **ONGs e instituições** | Cadastram, atualizam e divulgam animais disponíveis para adoção |
| **Administrador** | Gerencia cadastros, aprova ONGs e modera anúncios |

### 1.4 Funcionalidades contempladas

**Adoção**
- Cadastro, edição e remoção de animais para adoção pelas ONGs
- Busca de animais com filtros (espécie, porte, sexo, idade, cidade)
- Visualização dos detalhes do animal e dos contatos da ONG responsável

**Pets perdidos e encontrados**
- Registro de animais perdidos e encontrados, com foto, descrição, data e local
- Busca de anúncios com filtros (tipo, espécie, cidade, bairro, período)
- Marcação de anúncios como resolvidos quando o pet é reencontrado

**Usuários e administração**
- Cadastro e autenticação de usuários e ONGs
- Aprovação de ONGs e moderação de anúncios pelo administrador
- Denúncia de anúncios impróprios

## 2. Requisitos

### 2.1 Requisitos Funcionais

| ID | Descrição |
|---|---|
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

| ID | Categoria | Descrição |
|---|---|---|
| **RNF01** | Usabilidade / Portabilidade | O sistema deve ser responsivo, adaptando-se a computadores, tablets e celulares, e funcionar nos principais navegadores.|
| **RNF02** | Desempenho | As páginas de listagem e os resultados de busca devem carregar em até 3 segundos. |
| **RNF03** | Segurança | As senhas devem ser armazenadas com criptografia e toda a comunicação deve ocorrer via HTTPS. |
| **RNF04** | Segurança | O sistema deve restringir as funcionalidades conforme o perfil do usuário (visitante, usuário, ONG e administrador). |
| **RNF05** | Usabilidade | Um usuário cadastrado deve conseguir publicar um anúncio de pet perdido ou encontrado em no máximo 3 etapas. |
| **RNF06** | Privacidade | Os dados pessoais dos usuários devem ser usados apenas para o funcionamento da plataforma, sem serem compartilhados com terceiros. |
| **RNF07** | Manutenibilidade | O código-fonte deve ser versionado no GitHub e organizado em camadas (como MVC), facilitando a correção de erros e a inclusão de novas funcionalidades. |

### 2.3 Regras de Negócio

| ID | Descrição |
|---|---|
| **RN01** | Somente ONGs aprovadas pelo administrador podem cadastrar animais para adoção. Usuários comuns não podem publicar anúncios de adoção. |
| **RN02** | A plataforma apenas intermedeia o contato entre interessados e ONGs. O processo de adoção (entrevista, termo e entrega do animal) é de responsabilidade exclusiva da ONG. |
