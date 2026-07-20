🚀 Minhas Atividades de Java com Spring Boot e Manipulação de Arquivos
Este repositório foi criado para centralizar e organizar todas as atividades práticas desenvolvidas durante as aulas de desenvolvimento web com Java e Spring Boot. O objetivo principal destes exercícios é evoluir conceitos de Orientação a Objetos (como encapsulamento e herança) e manipulação de arquivos locais (TXT e CSV), integrando-os diretamente a uma API REST com retornos em formato JSON.

📌 Índice de Projetos
Abaixo estão listados todos os sistemas e APIs desenvolvidos, com a descrição do que foi aprendido e os conceitos aplicados em cada um.

🎵 1. A API da Playlist (playlistapi)
O que faz: Transforma um programa de terminal em um servidor local. A API lê um arquivo de texto local com músicas salvas, converte as informações em objetos Java e os envia para o navegador ou Postman em formato JSON. Também permite adicionar novas músicas de forma dinâmica.

Endpoints desenvolvidos:

GET /playlist/listar: Abre e lê o arquivo minha_playlist.txt, convertendo as linhas em uma lista de objetos exibida como JSON.

POST /playlist/adicionar: Recebe uma nova música no corpo da requisição (@RequestBody) e a salva no fim do arquivo de texto sem apagar os dados anteriores.

Conceitos aplicados: Criação de APIs REST com @RestController, manipulação de arquivos de texto com FileReader, BufferedReader, FileWriter (com modo append ativo) e BufferedWriter.

⚔️ 2. O Catálogo de Personagens Web (Catalogo_De_Personagens)
O que faz: Simula o backend de uma tela de seleção de personagens de jogos. O servidor lê uma base de dados no formato CSV, interpreta a herança dos guerreiros e entrega uma lista completa ou filtrada conforme a escolha do usuário na URL.

Endpoints desenvolvidos:

GET /personagens/todos: Lê o arquivo personagens_db.csv.txt, separa os campos usando split(";") e instancia a classe filha correta (LutadorCorpoACorpo ou Atirador).

GET /personagens/categoria/{tipo}: Filtra os personagens diretamente durante a leitura, retornando apenas os guerreiros da categoria especificada na URL.

Conceitos aplicados: Herança de classes, manipulação de arquivos estruturados (CSV), uso de variáveis de caminho (@PathVariable), filtros com listas e o operador instanceof.

🏆 3. O Portal do Hackathon (Portal_Do_Hackathon)
O que faz: Atua como o painel de controle de uma organização de Hackathon. Ao receber o comando via web, o servidor processa em lote um arquivo de inscrições brutas, valida as regras de negócio de cada participante, gera arquivos locais de resultados (aprovados e pendências) e retorna um relatório estatístico em tempo real.

Endpoints desenvolvidos:

POST /hackathon/processar: Aciona a leitura de inscricoes_brutas.txt, valida as idades permitidas (14 a 21 anos) e gera simultaneamente os arquivos aprovados_hackathon.txt e pendencias_inscricoes.txt. Retorna um objeto JSON customizado com o resumo do processamento.

Conceitos aplicados: Validação de regras de negócio, leitura e escrita concorrente de múltiplos arquivos, e criação de DTOs (Data Transfer Objects) para formatação de respostas JSON complexas (RelatorioProcessamento).

🛠️ Tecnologias Utilizadas Geral
Linguagem de Programação: Java

Framework Principal: Spring Boot (Spring Web)

Gerenciador de Dependências: Maven / Gradle

Formatos de Dados: JSON, TXT e CSV

Ferramentas de Teste: Navegador web e Postman
