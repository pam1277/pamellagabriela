1. O que é o Node.js? Explique sua finalidade e por que ele é considerado um ambiente de execução e não uma linguagem de programação.O Node.js é um ambiente de execução (runtime environment) de código aberto e multiplataforma que permite aos desenvolvedores
 executar JavaScript no lado do servidor (back-end),
fora de um navegador web. Ele foi construído sobre o motor V8 do Google Chrome, o mesmo motor que interpreta JavaScript no navegador, mas com APIs adicionais para interagir com o sistema operacional.

2. Qual a diferença entre Node.js e JavaScript executado no navegador? Cite pelo menos duas diferenças.A principal diferença entre Node.js e JavaScript no navegador é o ambiente de execução (runtime environment) e o propósito de cada um,
    embora ambos utilizem o motor V8 do Google Chrome para interpretar o código.

3. O que é o V8 Engine e qual sua importância para o funcionamento do Node.js?O V8 Engine é um motor JavaScript de código aberto, de alto desempenho, desenvolvido pelo Google em C++ para o Google Chrome, capaz de compilar código
 JavaScript diretamente em código de máquina nativo.
   Ele funciona fora do navegador, compilando o código em tempo de execução (Just-In-Time - JIT), o que é fundamental para o Node.js funcionar com extrema rapidez no servidor.

4. Explique o conceito de I/O não bloqueante no Node.js. Por que isso melhora o desempenho de aplicações?O I/O (Input/Output) não bloqueante é um dos pilares fundamentais do Node.js, permitindo
    que o ambiente de execução manipule múltiplas operações simultâneas
   (como leitura de banco de dados, requisições de rede ou manipulação de arquivos) sem travar a thread principal de execução.

5. O que é o Event Loop? Descreva, de forma resumida, como ele funciona.O Event Loop (Laço de Eventos) é um padrão de design ou mecanismo fundamental no JavaScript (e em ambientes como Node.js e navegadores)
que permite a execução de operações assíncronas não bloqueantes, mesmo que a linguagem seja single-threaded (execute uma coisa de cada vez) [1, 2]. 
Como funciona (Resumo)
O Event Loop funciona monitorando continuamente a Call Stack (pilha de execução) e a Callback Queue (fila de tarefas) para gerenciar o fluxo de código: 
Execução Síncrona (Call Stack): O código JavaScript roda linearmente na "Call Stack". Funções são empilhadas e executadas [2].
Operações Assíncronas: Quando uma operação assíncrona (como setTimeout, fetch, ou leitura de arquivo) é encontrada, ela é enviada para APIs do ambiente (Web APIs no navegador). A Call Stack continua livre [1, 2].
Fila de Tarefas (Callback Queue/Task Queue): Após a operação assíncrona terminar, seu callback (função de retorno) é movido para uma fila [2].
O Laço (Event Loop): O Event Loop verifica constantemente: "A Call Stack está vazia?".

6. O que são módulos no Node.js? Explique a diferença entre:

Módulos internos
Módulos externos
Módulos criados pelo desenvolvedor

Módulos no Node.js são arquivos JavaScript reutilizáveis que encapsulam código, funcionalidades e bibliotecas, organizando a aplicação em partes menores e especializadas. Eles permitem importar (usando require ou import) e exportar funcionalidades, facilitando a manutenção e organização do projeto. 
Os módulos no Node.js dividem-se em três tipos principais: 
Módulos Internos (Core Modules): Já vêm embutidos no Node.js no momento da instalação. Fornecem funcionalidades essenciais sem necessidade de instalação adicional. Exemplos: fs (sistema de arquivos), http (criação de servidores), path.
Módulos Externos (Third-party Modules): São bibliotecas ou frameworks criados pela comunidade, instalados através do npm (Node Package Manager) e armazenados na pasta node_modules. Exemplos: express, mongoose, lodash.
Módulos Criados pelo Desenvolvedor (Locais): São arquivos .js criados pelo próprio desenvolvedor para organizar sua aplicação. Geralmente importados usando caminhos relativos, como ./meuModulo. 

7. Para que serve o arquivo package.json em um projeto Node.js? Cite pelo menos três informações que ele pode conter.
O arquivo package.json é fundamental em qualquer projeto Node.js, servindo como o manifesto ou "coração" do projeto [1]. Ele descreve metadados sobre o projeto, gerencia dependências (bibliotecas de terceiros) e define scripts úteis para o desenvolvimento. 
Principais funções do package.json:
Gerenciamento de Dependências: Lista as bibliotecas que seu projeto precisa para funcionar (dependencies) e as necessárias para desenvolvimento (devDependencies) [2].
Identificação do Projeto: Contém nome, versão e descrição do projeto [1].
Automação: Define scripts personalizados para rodar tarefas (como iniciar o servidor, rodar testes, etc.) [3].

8. O que é o npm? Explique sua função no desenvolvimento de aplicações Node.js.
O npm (Node Package Manager) é o gerenciador de pacotes padrão para o ambiente de execução Node.js. Ele é automaticamente instalado junto com o Node.js e funciona como uma ferramenta de linha de
comando que facilita a instalação, o compartilhamento e a gestão de bibliotecas de terceiros (pacotes) em projetos JavaScript. 
O npm consiste em três componentes principais: o site (para pesquisar pacotes), a linha de comando (CLI) para interagir com eles e o registro (um grande banco de dados público de código open-source). 

9. O que é uma API REST e como o Node.js pode ser usado para desenvolvê-la?Uma API REST (Representational State Transfer) é um estilo arquitetural para projetar aplicações em rede, facilitando a troca de dados entre um cliente
    (como um navegador ou app mobile) e um servidor usando protocolos HTTP.
    Ela se baseia em recursos, onde cada informação é acessada por URLs únicas e manipulada via métodos HTTP padrão (GET, POST, PUT, DELETE).

   10. Cite duas vantagens e duas desvantagens do uso do Node.js em aplicações web.
  O Node.js é amplamente utilizado no desenvolvimento web por ser um ambiente de execução assíncrono baseado em JavaScript.
Abaixo estão duas vantagens e duas desvantagens principais: 
Vantagens
Alta Performance em Aplicações em Tempo Real: Devido à sua arquitetura orientada a eventos e I/O (entrada/saída) não bloqueante,
 o Node.js é extremamente eficiente para aplicações que exigem alta conectividade simultânea, como chats, jogos online e ferramentas de colaboração.
Uso de Linguagem Única (Full-stack JavaScript): Permite que desenvolvedores utilizem JavaScript tanto no frontend (navegador) quanto no backend (servidor).
 Isso unifica a equipe de desenvolvimento e facilita o compartilhamento de código entre as partes. 




    



