# GeneDash
Dashboard Genético 

este projeto simula um pequeno banco de dados genético, incluindo indivíduos, genes, variantes genéticas e níveis de expressão gênica por tecido. 
os dados são gerados com plpgsql e visualizados em um dashboard interativo.

## 🔬 entidades principais

- **genes**: nomes, descrições e sequências simuladas
- **variantes genéticas**: associadas aos genes, com frequência e impacto (alto, moderado, baixo ou neutro)
- **indivíduos**: cada um com idade, sexo e etnia (vinculada a um continente)
- **expressão gênica**: valores numéricos representando o nível de expressão de genes em tecidos como cérebro, fígado, coração, pulmão e rim

## 🧠 geração dos dados

os dados são gerados por um bloco `do $$ ... $$` em plpgsql, com estruturas `loop`, `array`, `random()` e `case`. ao executar o script no postgresql, 30 genes e 20 indivíduos são criados com variantes e dados de expressão.

## 📊 dashboard interativo

os dados foram visualizados no power bi, em um **dashboard dinâmico** que permite a interação entre os gráficos e visões:

- **mapa com grupos étnicos por continente**
- **tabela de expressão gênica por tecido (heatmap)**
- **gráfico de expressão por sexo e tecido**
- **expressão por sexo e idade**
- **contagem de indivíduos**

ao clicar em um item (ex: sexo ou tecido), os demais gráficos são filtrados automaticamente com base na seleção feita.

### exemplo do dashboard:

![dashboard](./Dashboard.gif)

> se quiser testar a versão interativa, é necessário abrir o arquivo `.pbix` no power bi desktop.

## 🚀 como usar

1. crie um banco de dados no postgresql
2. execute o script `script.sql` para criar as tabelas e popular os dados
3. abra o arquivo `.pbix` no power bi desktop para explorar o dashboard

## 📁 arquivos do projeto

- `Script.sql`: script completo para criação e povoamento das tabelas
- `Dashboard.pbix`: arquivo do power bi com o dashboard interativo
- `README.md`: descrição do projeto
- `Dashboard.gif`: gif do dashboard

---

