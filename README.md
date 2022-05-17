# JSFProblems
Conjunto de pequenas aplicações utilizando o framework web JSF.

## Objetivos
- Desenvolver pequeno projeto na linguagem de programação Java utiizando o framework JSF.

## Requisitos
- Realizar o download do Eclipse Java EE junto ao website: (https://www.eclipse.org/downloads/packages/release/2021-03/r). Projeto funcionou na versão do Eclipse Java EE: 2021/03. (Versão mais nova de 2022 apresentou problemas).
- Realizar o download do Tomcat junto ao website: (https://tomcat.apache.org/download-90.cgi), versão: 9.0.62.
- Instalar Java 11: (sudo apt-get install openjdjk-11). (Opcional: Funcionou no Java 15).

### Links de apoio
- Projeto Algaworks: (https://github.com/algaworks/curso-jsf-primefaces-essencial).
- Helper GitHub: (https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer) e (https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Configura%C3%A7%C3%A3o-Inicial-do-Git).

### Subir Tomcat por linha de comando
- Na linha de comando, dentro da pasta bin, atribuir permissão de execução: chmod +x *.sh.
- Iniciar servidor com o comando: ./startup.sh.
- Digitar no browser: (http://localhost:8080/). Se tudo estiver ok, uma página deverá ser exibida.
- Para encerrar o servidor, inserir o comando: ./shutdown.sh.

### Configuração do Tomcat no Eclipse 
- Clicar na aba de instalação de server (Atentar para seleção da versão correta do Tomcat).
- Adicionar caminho do diretório do Tomcat e finalizar instalação.
- Iniciar servidor em modo debug como teste.

### Configuração do Eclipse
- Corrigir enconding para UTF-8: Window >> Preferences.

## Criação do projeto no Maven
- Acessar: File >> New >> Maven Project.
- Deixar selecionadas as opções: (Create a simple...) e (Use default..).
- Inserir dados do projeto: GroupId: com.algaworks, ArtifactID: OlaMaven, Version: 1.0.0-Snapshot e Packing: war.

### Configuração do POM.xml
- O projeto apresentará erros no POM, em especial na ausência do arquivo: web.xml.
- Adicionar codificação: UTF-8 junto as propriedades do projeto
- Adicionar execução no Java 15 junto as propriedades do projeto.
- Adicionar dependência do JSF Mojarra 2.2 (https://mvnrepository.com/artifact/org.glassfish/javax.faces/2.2.20).

### Configurações no Eclipse para execução
- Adicionar o JavaServer Faces 2.2: Botão Direito no Projeto >> Properties >> Project Facets.
- Selecionar opção do JavaServer Faces 2.2.
- Selecionar opção: Disable Library Configuration.
- Realizar a configuração exigida: Remover o /faces/ e adicionar *.xhtml no URL Mapping Patterns.
- Adicionar o Apache Tomcat 9 nos runtimes.
- Aplicar e confirmar alterações.
- Após confirmação os arquivos: faces-config.xml e web.xml serão criados.
- Definir a pasta WebApp no buildpath: Clicar com direito >> Build Path >> Use as Source Foulder.
- Executar atualização do Maven para corrigir pequenos erros: Botão Direito no Projeto >> Properties >> Maven >> Update Maven.

## Criar projeto
- Verificar se o arquivo: faces-config.xml apresenta problemas e corrigí-los.
- Verificar se o arquivo: web.xml apresenta problemas e corrigi-los.
- Criar arquivo JSP em: WebApp >> New >> Jsp File >> OlaMaven.jsp.
- Associar projeto junto ao servidor Tomcat: Clicar com direito no servidor >> Add and Remove.
- Iniciar servidor em modo debug.
- Executar via browser em: (http://localhost:8080/OlaMaven/OlaMaven.jsp).

## Adicionando o Primefaces
- Pode ser feita com a adição da dependência junto ao POM.xml (https://mvnrepository.com/artifact/org.primefaces/primefaces/11.0.0).










