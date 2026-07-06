## Sobre o Projeto

Este repositório compila a suíte completa de **testes estatísticos** e **visualizações de dados** desenvolvida para avaliar o desempenho de **Modelos de Linguagem de Grande Escala (LLMs)** aplicados a sistemas de recomendação veicular. A pesquisa contrasta de forma direta duas metodologias de raciocínio: a arquitetura sequencial **ReAct** e a arquitetura estruturada em **Grafo (LangGraph)**.

O objetivo desta bateria de análises  da simples medição de acurácia bruta e desempenho computacional de sete modelos distintos: *Deep-Seek, Qwen2.5-72b, Llama3-70b, Qwen3-32b, GPT-Oss, Llama3-8b* e *Gemma3*.

---

## Estrutura das Análises Visuais

O repositório está dividido em **cinco eixos investigativos principais**, fundamentados em dados extraídos de cenários de inferência controlados (Perguntas P1 a P5):

* **Eixo 1: A Prova da Equalização (Desempenho Bruto)**
Gráficos de barras que estabelecem o **desempenho base** de cada modelo em sua respectiva arquitetura. Este conjunto expõe os ganhos gerados pela adoção do Grafo, com destaque para a **estabilização do raciocínio** em modelos com menor densidade de parâmetros.
* **Eixo 2: Sensibilidade e Viés de Ordem (*Order Bias*)**
Análise pareada focada na **resiliência da atenção** do LLM. Demonstra a flutuação do desempenho quando a ordem das entidades no *prompt* é invertida, provando visualmente qual arquitetura **blinda o sistema** contra as variações de formulação do usuário.
* **Eixo 3: Equidade e Sensibilidade Demográfica**
Avaliação direta de **viés de gênero**. Painéis e tabelas de variação expõem o desvio de pontuação matemático ($\Delta$) quando o usuário se identifica como "Masculino" ou "Feminino", denunciando as arquiteturas que exacerbam ou mitigam **preconceitos latentes** nas redes neurais.
* **Eixo 4: A Desconstrução do Perfil (Estudo de Ablação)**
Gráficos detalhados que dissecam o **impacto da ausência de contexto**. O sistema é testado sob o cenário completo e, em seguida, sofre a **ablação cirúrgica** das variáveis de perfil (Idade e Sexo), permitindo medir a degradação exata da lógica de recomendação em diferentes fatias demográficas.

---

## Considerações Metodológicas

Todas as visualizações e matrizes de dados compiladas neste documento derivam de um **processamento relacional limpo**, onde métricas qualitativas (**BERTScore/Acurácia**) e quantitativas (**Verbosidade**) foram rigorosamente pareadas. O **isolamento estatístico** de cada variável de *prompt* garante que as conclusões levantadas sobre a mitigação de falhas pelo uso de Grafos sejam pautadas em **evidências matemáticas inquestionáveis**.
