📊 Projeto de Análise e Automação de Relatórios de Vendas com Python no Google Colab
Este projeto marca o início da minha jornada em automação com Análise de Dados utilizando Python, de forma totalmente online com Google Colab. A proposta é transformar dados brutos de vendas em relatórios e dashboards automáticos, otimizando tempo e facilitando a tomada de decisões.

✅ Benefícios Reais para Empresas
Empresas que lidam com grandes volumes de dados de vendas podem obter ganhos significativos com este tipo de automação:

🚀 Geração automática de relatórios e dashboards em segundos

⏱️ Economia de tempo e aumento da produtividade

📊 Análise clara do desempenho por vendedor ou equipe

🔁 Processos replicáveis com código limpo e reutilizável

👨‍💼 Profissionais com domínio de Python, pandas e Colab agregam valor ao time de dados

💡 Maior autonomia para obter insights, sem depender de planilhas manuais

🎯 Objetivos do Projeto
Ler uma base de dados de vendas em formato .xlsx

Agrupar os dados por vendedor e somar os valores de venda

Criar e exportar um relatório automático em Excel

Gerar um dashboard visual interativo em segundos

Garantir que todo o código seja comentado, didático e fácil de entender

🌐 Ambiente Utilizado
Ferramenta	Finalidade
💻 Google Colab	Execução 100% online, sem necessidade de instalação
🐍 Python 3.11	Linguagem principal do projeto
📦 pandas	Manipulação de dados tabulares
📊 Plotly Express	Criação de dashboard visual interativo
📁 Excel (.xlsx)	Entrada e saída de dados

🧰 Bibliotecas Utilizadas
Biblioteca	Função Principal
pandas	Carregar, tratar, agrupar e exportar os dados
plotly.express	Criar o dashboard visual automático
openpyxl	Exportar para o formato Excel (.xlsx)

📂 Estrutura da Base de Dados
Coluna	Descrição
Data	Data da venda
Produto	Produto vendido
Estado	Estado onde ocorreu a venda
Vendedor	Nome do(a) vendedor(a) responsável
Valor	Valor monetário da venda
mes	Mês extraído da data (gerado no script)

ℹ️ A análise é baseada no total de Valor vendido por vendedor. A coluna Quantidade não estava presente na base original.

🧾 Etapas da Automação – Totalmente Comentadas
Todas as partes do código foram comentadas para facilitar o entendimento e a replicação.

1. Carregamento e visualização dos dados
import pandas as pd
df = pd.read_excel('vendas.xlsx')
df.head()
2. Agrupamento de vendas por vendedor
vendas_por_vendedor = df.groupby('Vendedor')['Valor'].sum()
3. Exportação do relatório
vendas_por_vendedor.to_excel('vendas_por_vendedor.xlsx')
4. Geração automática do dashboard visual
import plotly.express as px

fig = px.bar(
    vendas_por_vendedor,
    x=vendas_por_vendedor.index,
    y='Valor',
    title='Total de Vendas por Vendedor'
)
fig.show()
📈 O gráfico é gerado automaticamente, permitindo uma análise visual clara e instantânea.

📤 Resultado Final
✅ Arquivo vendas_por_vendedor.xlsx com totais por vendedor

📊 Dashboard interativo com gráfico de barras

💡 Código limpo, comentado e reutilizável

🧪 Como Executar
Acesse o Google Colab

Importe o notebook .ipynb para seu Colab

Faça upload do seu arquivo .xlsx

Execute as células (ícones de play à esquerda)

O relatório será gerado e o gráfico será exibido automaticamente

✅ Nenhuma instalação é necessária. Tudo é feito direto no navegador.

👨‍💻 Sobre o Autor
Rafael Agra
📍 Florianópolis – SC
🎓 Estudante de Análise de Dados
🔄 Em transição de carreira para a área de tecnologia
🔧 Focado em resolver problemas com dados e automações práticas
🔗 https://www.linkedin.com/in/rafael-agra-201005355/

💬 Contribuições
Sugestões, melhorias ou feedbacks são sempre bem-vindos!
Abra uma issue ou faça um fork para contribuir.

📌 Observação Final
Este é meu primeiro projeto prático de automação com análise de dados. Foi criado com foco em simplicidade e utilidade, tanto para estudo quanto para aplicação real em empresas que valorizam decisões baseadas em dados. 🚀

