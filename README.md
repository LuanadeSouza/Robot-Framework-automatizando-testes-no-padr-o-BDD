# Projeto de Testes Automatizados com Robot Framework

## Descrição
Este projeto utiliza o **Robot Framework** para automatizar o teste de um sistema web que permite a criação de "cards" atribuídos a diferentes times. A funcionalidade principal é validar os comportamentos esperados em cenários de preenchimento correto e incorreto do formulário de cadastro.

---

## Estrutura do Projeto

### Diretórios e Arquivos Principais

- **`pages/`**: Contém os recursos e palavras-chave específicas para interagir com as páginas do sistema.
  - `cadastro_organo.robot`: Define palavras-chave para a página de cadastro e elementos relacionados.

- **`shared/`**: Contém configurações e palavras-chave compartilhadas entre os testes.
  - `setup_teardown.robot`: Palavras-chave para inicialização e encerramento dos testes.
  - `main.robot`: Recursos compartilhados, incluindo bibliotecas e configurações gerais.

- **`testes/`**: Contém os cenários de teste organizados por preenchimento correto ou incorreto do formulário.
  - `preenchimento_correto.robot`: Testes para validar preenchimentos corretos.
  - `preenchimento_incorreto.robot`: Testes para validar mensagens de erro em preenchimentos incorretos.

---

## Configurações Utilizadas

### Bibliotecas
- **`SeleniumLibrary`**: Para interações com o navegador.
- **`FakerLibrary`**: Para gerar dados aleatórios em `pt_BR`.

### Navegador
- **`Chrome`**: Utilizado para execução dos testes.

---

## Como Executar

### Requisitos
Certifique-se de ter as seguintes ferramentas instaladas:
- Python 3+
- Robot Framework
- SeleniumLibrary
- FakerLibrary
- WebDriver do Chrome compatível com sua versão do navegador

### Instalação
1. Clone este repositório:
   ```bash
   git clone <URL-DO-REPOSITORIO>
   cd <NOME-DO-PROJETO>
   ```

2. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```

### Execução dos Testes
Para executar todos os testes:
```bash
robot testes/
```

Para executar um arquivo de teste específico:
```bash
robot testes/preenchimento_correto.robot
```

---

## Cenários de Teste

### Preenchimento Correto
1. **Verificar se ao preencher corretamente o formulário os dados são inseridos corretamente na lista e um novo card é criado no time escolhido.**
2. **Verificar se é possível criar mais de um card se preenchermos os campos corretamente.**
3. **Verificar se é possível criar um card para cada time se preenchermos os campos corretamente.**

### Preenchimento Incorreto
1. **Verificar se quando um campo obrigatório não for preenchido corretamente, o sistema exibe uma mensagem de campo obrigatório.**

---

## Estrutura do Código

### Palavras-Chave Específicas
- **`Dado que eu preencha os campos do formulário`**: Preenche os campos obrigatórios do formulário com dados aleatórios.
- **`E clique no botão "Criar Card"`**: Aciona o botão de criação de card.
- **`Então identificar o card no time esperado`**: Verifica se o card foi criado no time correto.
- **`Então sistema deve apresentar mensagem de campo obrigatório`**: Valida a exibição de mensagens de erro para campos obrigatórios.

---

## Contribuições
- **Issues:** Relate problemas ou sugestões na seção de issues do repositório.
- **Pull Requests:** Aceitamos contribuições! Certifique-se de seguir as boas práticas de desenvolvimento e incluir testes adequados.

---

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
