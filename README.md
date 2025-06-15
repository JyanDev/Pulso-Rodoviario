# 📊 Gerador de Relatório de Pulso Rodoviário – Projeto Institucional AGERGS

Este é um sistema desenvolvido sob demanda durante meu período na antiga empresa de fiscalização de energia (AGERGS), com o objetivo de automatizar a coleta e o compartilhamento de informações atualizadas sobre as condições rodoviárias do estado. O programa acessa um site específico com atualizações em tempo real, extrai os dados relevantes e gera um arquivo `.xlsx` (Excel), que é salvo automaticamente em um domínio interno da rede da AGERGS, permitindo o acesso contínuo por parte dos servidores públicos do órgão.

---

## Veja uma demonstração na prática
⚠️ Não realizei a abertura do arquivo excel no video por motivos de privacidade dos dados da empresa.
- Assista a este [Video demonstrativo](https://youtu.be/cdyHAstpvZE)

## 🧩 Visão Geral do Projeto

- **Objetivo:** Automatizar a extração de dados rodoviários em tempo real e distribuí-los via planilhas Excel na rede interna da AGERGS.
- **Ambiente:** Projetado para rodar exclusivamente dentro do domínio da empresa, em um servidor interno configurado para execução periódica automática.
- **Funcionamento:**  
  - Acessa uma página da web de status rodoviário.
  - Extrai as informações de rotas, status e horário da última atualização.
  - Organiza os dados em um DataFrame.
  - Gera e estiliza uma planilha Excel com os dados coletados.
  - Salva a planilha em uma pasta acessível na rede institucional.

---

## ⚙️ Tecnologias Utilizadas

- `Python` – linguagem principal para automação.
- `requests` – para requisições HTTP ao site.
- `BeautifulSoup` – para parseamento HTML.
- `pandas` – estruturação e manipulação dos dados em DataFrame.
- `openpyxl` – geração e formatação do arquivo Excel.
- `tkinter` – interface gráfica simples para feedback visual ao operador.
- `threading` – execução paralela da UI de carregamento.
- `os`, `datetime`, `sys` – operações de sistema, data e caminho de arquivos.

---

## 🛠️ Arquitetura do Programa

- Modularizado em funções claras:
  - `fetch_data`: coleta o HTML da página.
  - `parse_html`: extrai os dados relevantes.
  - `create_excel`: organiza os dados e gera a planilha.
  - `show_loading_screen`: exibe uma janela temporária de carregamento.
  - `main`: orquestra a execução geral.
- Os arquivos são salvos na pasta `Arquivos_Exel/`, com timestamp no nome para controle de versões.
- Pensado para ser utilizado em conjunto com o **PyInstaller**, facilitando a distribuição no ambiente interno da empresa.

---

## 🧠 Considerações Pessoais

Este projeto foi uma experiência real de automação aplicada em ambiente institucional. Além da prática técnica, ele envolveu responsabilidade com dados públicos, integração com a rede interna da empresa e atenção à usabilidade por parte dos colaboradores.

Apesar de simples, foi essencial para facilitar o acesso rápido a informações logísticas importantes. Demonstra capacidade de transformar demandas práticas em soluções técnicas funcionais e confiáveis, mesmo em contextos com restrições como domínio de rede e infraestrutura interna da empresa.
