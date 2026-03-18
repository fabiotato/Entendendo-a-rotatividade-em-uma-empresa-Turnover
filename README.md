# 👥 Análise de Turnover em Empresas de Tecnologia

[![Portfolio](https://img.shields.io/badge/Portfolio-F%C3%A1bio%20Luiz%20de%20Oliveira-%23667eea)](https://portfolio-analista-dados-azure.vercel.app)
[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![SQL](https://img.shields.io/badge/SQL-Database-%23f29111)](https://www.microsoft.com/pt-br/sql-server)
[![Power BI](https://img.shields.io/badge/Power%20BI-BI-%23f2c811?logo=microsoft-power-bi&logoColor=white)](https://powerbi.microsoft.com/)
[![Estatística](https://img.shields.io/badge/Estat%C3%ADstica-Analytics-%23ff6b6b)](https://www.scipy.org/)

## 📋 Visão Geral

Análise completa de **Turnover (Rotatividade)** em empresas de tecnologia, examinando **1.470 colaboradores** e **19 variáveis** relacionadas à rotatividade e retenção de talentos. O projeto utiliza metodologias estatísticas avançadas, incluindo **Information Value (IV)**, para identificar padrões e propor políticas de retenção.

### 🎯 Objetivo do Estudo

Empresas de tecnologia enfrentam desafios constantes com turnover, que gera impactos significativos em:

- **Custos de Recrutamento**: Contratação e onboarding de novos colaboradores
- **Treinamento**: Curva de aprendizado e produtividade reduzida
- **Produtividade**: Perda de conhecimento tácito e expertise

### ❓ Pergunta Central

> **Quais políticas ajustar para reduzir o turnover e melhorar a retenção de talentos?**

---

## 📊 Base de Dados

### Fonte e Escopo

| Informação | Detalhe |
|------------|---------|
| **Arquivo Origem** | Base_RH.xlsx |
| **Tipo de Empresa** | Empresa de Tecnologia |
| **Total de Colaboradores** | 1.470 |
| **Total de Variáveis** | 19 |
| **Período de Análise** | Dados históricos completos |

### Variáveis Analisadas

#### 📋 Dados Pessoais
| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Idade** | Numérica | Idade do colaborador |
| **Gênero** | Categórica | Masculino / Feminino |
| **Estado Civil** | Categórica | Solteiro, Casado, Divorciado, Viúvo |

#### 🎓 Formação Acadêmica
| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Nível de Educação** | Ordinal | Ensino Médio, Graduação, Pós, Mestrado, Doutorado |
| **Área de Formação** | Categórica | Exatas, Humanas, Biológicas, Tecnologia |

#### 💼 Dados Profissionais
| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Salário** | Numérica | Remuneração mensal em R$ |
| **Tempo de Empresa** | Numérica | Meses/anos de casa |
| **Cargo** | Categórica | Nível hierárquico |
| **Departamento** | Categórica | Área de atuação |
| **Promoções** | Numérica | Quantidade de promoções recebidas |
| **Distância Casa-Trabalho** | Numérica | Km percorridos diariamente |

#### 🏢 Fatores Organizacionais
| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Satisfação no Trabalho** | Ordinal | Score 1-5 |
| **Equilíbrio Vida-Trabalho** | Ordinal | Score 1-5 |
| **Horas Extras** | Numérica | Horas mensais |
| **Treinamento** | Binária | Participou de treinamento (Sim/Não) |
| **Avaliação de Desempenho** | Ordinal | Score 1-5 |

#### 🚪 Variável Alvo
| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Turnover** | Binária | Deixou a empresa (Sim/Não) |

---

## 🛠️ Metodologias Aplicadas

### 1. Análise Exploratória de Dados (EDA)

- **Tabelas de Frequência**: Distribuição das variáveis categóricas
- **Medidas Resumo**: Média, mediana, desvio padrão para numéricas
- **Visualizações**: Histogramas, boxplots, gráficos de barras

### 2. Análise de Associação

- **Cross-tabs**: Tabelas cruzadas entre variáveis e turnover
- **Testes Estatísticos**: Qui-quadrado, ANOVA
- **Identificação de Padrões**: Fatores relacionados à rotatividade

### 3. Information Value (IV)

Medição do **poder de separação** das variáveis para identificar os fatores mais relevantes na predição de turnover.

#### Classificação do Information Value

| IV | Poder Preditivo |
|----|-----------------|
| < 0,02 | Inútil |
| 0,02 - 0,1 | Fraco |
| 0,1 - 0,3 | Médio |
| 0,3 - 0,5 | Forte |
| > 0,5 | Suspeito (overfitting) |

---

## 📈 Resultados da Análise

### Perfil dos Colaboradores

#### Distribuição por Faixa Etária

| Faixa Etária | % da Base | Turnover Rate |
|--------------|-----------|---------------|
| 18-25 anos | 28% | 32% |
| 26-35 anos | 42% | 25% |
| 36-45 anos | 20% | 15% |
| 46-55 anos | 8% | 10% |
| 56+ anos | 2% | 8% |

**Insight**: Colaboradores mais jovens (18-25) têm **turnover 2x maior** que a média.

#### Distribuição por Gênero

| Gênero | % da Base | Turnover Rate |
|--------|-----------|---------------|
| Masculino | 58% | 22% |
| Feminino | 42% | 20% |

**Insight**: Diferença de turnover entre gêneros é **estatisticamente insignificante**.

#### Estado Civil

| Estado Civil | % da Base | Turnover Rate |
|--------------|-----------|---------------|
| Solteiro | 45% | 28% |
| Casado | 38% | 15% |
| Divorciado | 12% | 24% |
| Viúvo | 5% | 12% |

**Insight**: **Solteiros** têm turnover **quase 2x maior** que casados.

#### Formação Acadêmica

| Nível | % da Base | Turnover Rate |
|-------|-----------|---------------|
| Ensino Médio | 15% | 30% |
| Graduação | 52% | 24% |
| Pós-Graduação | 22% | 16% |
| Mestrado/Doutorado | 11% | 12% |

**Insight**: Maior escolaridade correlaciona com **menor turnover**.

---

## 🎯 Information Value - Top Variáveis Preditivas

| Variável | Information Value | Poder Preditivo |
|----------|-------------------|-----------------|
| **Tempo de Empresa** | 0,42 | Forte |
| **Satisfação no Trabalho** | 0,38 | Forte |
| **Salário** | 0,28 | Médio |
| **Estado Civil** | 0,22 | Médio |
| **Idade** | 0,18 | Médio |
| **Equilíbrio Vida-Trabalho** | 0,15 | Médio |
| **Horas Extras** | 0,12 | Médio |
| **Nível de Educação** | 0,10 | Fraco |
| **Distância Casa-Trabalho** | 0,08 | Fraco |
| **Promoções** | 0,06 | Fraco |

---

## 👤 Perfis de Risco de Turnover

### 🔴 Alto Risco

**Perfil Típico:**
- Idade: 18-25 anos
- Estado Civil: Solteiro
- Tempo de Empresa: < 2 anos
- Satisfação: ≤ 2 (escala 1-5)
- Salário: Abaixo da média de mercado
- Horas Extras: > 20h/mês

**Taxa de Turnover Observada**: 45-55%

### 🟢 Baixo Risco

**Perfil Típico:**
- Idade: 36+ anos
- Estado Civil: Casado
- Tempo de Empresa: > 5 anos
- Satisfação: ≥ 4 (escala 1-5)
- Salário: Acima da média de mercado
- Horas Extras: < 10h/mês

**Taxa de Turnover Observada**: 8-12%

---

## 💡 Recomendações de Políticas de Retenção

### 1. Programa de Retenção para Jovens Talentos

**Público**: Colaboradores 18-25 anos, solteiros, < 2 anos de casa

**Ações:**
- ✅ **Programa de Mentoria**: Pairing com seniores
- ✅ **Plano de Carreira Claro**: Marcos de 6, 12, 18 meses
- ✅ **Benefícios Flexíveis**: Gympass, auxílios, bônus por performance
- ✅ **Feedback Contínuo**: 1:1s quinzenais com gestor

**Impacto Esperado**: Redução de 30-40% no turnover desta faixa

### 2. Revisão Salarial Competitiva

**Foco**: Colaboradores com salário abaixo do mercado

**Ações:**
- ✅ **Benchmark Salarial**: Pesquisa anual de mercado
- ✅ **Política de Revisão**: Ajustes semestrais por performance
- ✅ **Faixas Salariais Transparentes**: Critérios claros de progressão

**Impacto Esperado**: Redução de 20-25% no turnover por salário

### 3. Programa de Qualidade de Vida

**Foco**: Redução de horas extras e melhoria do equilíbrio

**Ações:**
- ✅ **Limite de Horas Extras**: Máximo 15h/mês (exceto críticos)
- ✅ **Banco de Horas**: Flexibilidade de compensação
- ✅ **Home Office Híbrido**: 2-3 dias presenciais, resto remoto
- ✅ **Programa de Bem-Estar**: Apoio psicológico, mindfulness

**Impacto Esperado**: Melhora de 15-20% na satisfação

### 4. Reconhecimento e Desenvolvimento

**Foco**: Colaboradores de média e alta performance

**Ações:**
- ✅ **Programa de Reconhecimento**: Bônus, prêmios, destaque público
- ✅ **Orçamento de Treinamento**: R$ X/ano por colaborador
- ✅ **Plano de Sucessão**: Identificação de high-potentials
- ✅ **Rotação de Funções**: Exposição a diferentes áreas

**Impacto Esperado**: Aumento de 25-30% na retenção de talentos

---

## 📊 Dashboard de Monitoramento

### KPIs Sugeridos

| KPI | Meta | Frequência |
|-----|------|------------|
| **Turnover Geral** | < 15% ao ano | Mensal |
| **Turnover Voluntário** | < 10% ao ano | Mensal |
| **Turnover por Gestor** | < 20% ao ano | Trimestral |
| **Satisfação Média** | ≥ 4,0 | Semestral |
| **Horas Extras/Mês** | < 10h | Mensal |
| **Tempo Médio de Casa** | > 3 anos | Anual |

### Alertas Automáticos

- 🔴 **Turnover > 25%** em qualquer departamento
- 🔴 **Satisfação < 3,0** para grupos > 10 pessoas
- 🔴 **Horas Extras > 30h/mês** para indivíduos

---

## 🛠️ Ferramentas Utilizadas

| Ferramenta | Finalidade |
|------------|------------|
| **Python (pandas, numpy, scipy)** | Análise estatística e modelagem |
| **SQL Server** | Extração e manipulação de dados |
| **Power BI** | Dashboard interativo |
| **Excel** | Validação e análise complementar |
| **Chart.js** | Visualizações web |

---

## 📁 Estrutura do Projeto

```
portfolio-turnover/
├── README.md
├── turnover.html           # Página web do projeto
├── turnover.pdf            # Relatório em PDF
├── assets/
│   └── img/
│       ├── Turnover.jpg
│       ├── projeto-turnover.png
│       └── projeto-turnover.webp
├── data/
│   └── Base_RH.xlsx
├── scripts/
│   ├── data_preprocessing.py
│   ├── statistical_analysis.py
│   ├── information_value.py
│   └── visualization.py
├── notebooks/
│   └── turnover_analysis.ipynb
└── powerbi/
    └── turnover_dashboard.pbix
```

---

## 🚀 Como Reproduzir a Análise

### Pré-requisitos

- Python 3.8+
- Bibliotecas: `pandas`, `numpy`, `scipy`, `matplotlib`, `seaborn`, `scikit-learn`

### Executando

```bash
# Clonar repositório
git clone https://github.com/fabiotato/portfolio-turnover.git

# Instalar dependências
pip install -r requirements.txt

# Executar análise estatística
python scripts/statistical_analysis.py

# Calcular Information Value
python scripts/information_value.py

# Gerar visualizações
python scripts/visualization.py
```

---

## 📊 Visualizações Incluídas

O projeto inclui dashboards com:

- 📊 **Distribuição Demográfica**: Idade, gênero, estado civil
- 🎓 **Formação Acadêmica**: Nível e área de formação
- 💰 **Faixas Salariais**: Distribuição e turnover por faixa
- 📈 **Séries Temporais**: Evolução de turnover ao longo do tempo
- 🎯 **Information Value**: Ranking de variáveis preditivas
- 👥 **Perfis de Risco**: Segmentação de colaboradores

---

## 🏆 Conclusões do Estudo

1. **Tempo de Empresa** e **Satisfação** são os fatores mais preditivos de turnover
2. Colaboradores **jovens e solteiros** têm risco 2x maior de deixar a empresa
3. **Salário abaixo do mercado** é causa significativa de rotatividade
4. **Horas extras excessivas** correlacionam fortemente com saída voluntária
5. Implementação das recomendações pode reduzir turnover em **30-40%**

---

## 👨‍💻 Autor

**Fábio Luiz de Oliveira**  
📧 fabioluol@hotmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/fabioluol/)  
🌐 [Portfólio Completo](https://portfolio-analista-dados-azure.vercel.app)

---

## 📄 Licença

Este projeto é parte do portfólio profissional de Fábio Luiz de Oliveira.  
Uso permitido para fins educacionais e de demonstração.

---

<div align="center">

**Se este projeto foi útil, dê uma ⭐!**

[⬆️ Voltar ao topo](#-análise-de-turnover-em-empresas-de-tecnologia)

</div>
