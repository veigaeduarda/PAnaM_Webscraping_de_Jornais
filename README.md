# 📰 Políticas de Alimentação na Mídia: Extração de Dados Jornalísticos

## 📝 Descrição do Projeto
Este repositório contém os scripts em Python desenvolvidos para a extração automatizada de matérias jornalísticas nos portais **Gazeta do Povo**, **O Joio e o Trigo**, **MyJoyOnline** e **Ghana News**. O objetivo principal é estruturar a coleta de dados da cobertura midiática sobre políticas públicas relacionadas à alimentação, saúde e regulação, criando uma base sólida para análise de conteúdo.

## 🛠️ Tecnologias Utilizadas
O projeto foi desenvolvido em linguagem Python, utilizando as seguintes bibliotecas para automação, raspagem e estruturação de dados:

* **[BeautifulSoup]** - Para análise e extração de dados do HTML estruturado.
* **[Selenium]** - Para automação da navegação e extração em páginas dinâmicas.
* **[urllib]** - Para o manuseio e requisição das URLs dos portais.
* **[Pandas]** - Para a estruturação, limpeza e exportação dos metadados extraídos.

## ⚙️ Metodologia de Extração
O processo de raspagem (Web Scraping) foi desenhado para ser contínuo e resiliente. Durante a execução do script:
- Se determinado elemento da página não for encontrado, o campo é registrado como `ausente`, o que evita a interrupção do código e garante a continuidade da coleta. 
- URLs inválidas, páginas inacessíveis ou sites fora do escopo são automaticamente descartados. 
- A editoria da matéria é inferida, sempre que possível, a partir da própria estrutura da URL.

### 📊 Dados Coletados
Para cada notícia processada, o método extrai as seguintes informações e metadados:
- [x] Site e URL original
- [x] Autor(a)
- [x] Data de publicação
- [x] Título da matéria
- [x] Texto na íntegra
- [x] Editoria e Origem
- [x] Palavras-chave localizadas no texto
- [x] Entrevistados e instituições mencionadas

## 🔍 Estratégia de Busca e Recorte Temático
O levantamento utilizou um dicionário de palavras-chave com termos adaptados para português, inglês e espanhol. O foco da coleta abrange a cobertura das seguintes políticas públicas:

1. Alimentos ultraprocessados
2. Rotulagem de alimentos
3. Publicidade de alimentos
4. Alimentação escolar
5. Agrotóxicos e pesticidas

Para aumentar a precisão e reduzir a extração de matérias irrelevantes (falsos positivos), o script utiliza um sistema de **truncagem**. As palavras-chave são combinadas cruzando um "eixo central" com um "assunto", refinando os resultados para que atendam estritamente aos objetivos da pesquisa. 

> 💡 **Nota:** Todas as palavras-chave utilizadas para a extração e os seus respectivos scripts, separados por portal, encontram-se disponíveis no **COLOCAR ONDE** deste projeto.
