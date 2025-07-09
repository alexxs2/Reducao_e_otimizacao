# **REDUÇÃO DO TEMPO DE ESPERA EM PORTOS: SEGMENTAÇÃO DE TERMINAIS VIA TÉCNICAS DE CLUSTERING**

**Autores**:

**Matheus Henrique de Barros Ileck**

**Alexsandro Da Silva Bezerra**

**Alexandre Da Cunha Fernades**

# 1. **INTRODUÇÃO**

Os portos são fundamentais na logística global, movimentando mais de 80 % do comércio internacional em volume. e funcionando como hubs que conectam mercados, facilitando a distribuição de mercadorias e sustentando economias em escala mundial, para investigar essas possibilidades, o presente estudo se fundamenta em dados históricos de movimentação portuária, de 2005 a fevereiro de 2025.

O objetivo geral consiste em agrupar terminais portuários segundo perfis de movimentação de carga, visando ajudar na otimização logística e a redução do tempo de espera de navios, para atingir tal objetivo, realizamos um pré-processamento, limpeza, tratamento no conjunto de dados, seguindo de uma análise exploratória completa e então aplicar os modelos de agrupamentos, avaliamos a qualidade dos agrupamentos, escolhemos o vencedor e por fim interpretamos os clusters para formular recomendações operacionais e benchmarks entre terminais semelhantes.

# 2. **METODOLOGIA**

a. Coleta de dados: Integramos planilhas históricas de tonelagem, unidades, TEUs e características de terminais.

b. Análise exploratória: Avaliamos tendências anuais, tipos de carga, movimentação, tipos de terminais, destacamos outliers e identificamos os cinco terminais mais ativos.

c. Pré-processamento:

- Tratamento de valores faltantes.

- Tratamento de outliers extremos em toneladas, TEUs e unidades por meio do método de intervalos de confiança.

-  Normalização das variáveis usando escalonamento robusto, que evita distorções causadas por valores extremos.

d. Redução de dimensionalidade com PCA: Aplicamos Análise de Componentes Principais para resumir diversas variáveis em menos “componentes” evitando problemas de multicolinearidade e preservando 100% da variância com apenas 10 componentes.

e. Clusterização: Após comparar dois algoritmos de Agrupamento, decidimos o vencedor atráves de métricas específicas para esses algoritmos, Com o algoritmo vencedor que foi o Hierárquica, utilizamos o método de ligação “weighted” para agrupar os terminais em 4 clusters, escolhendo o número de grupos que melhor mostrava diferenças operacionais claras.

# 3. **RESULTADOS E DISCUSSÕES**

Após atribuir cada terminal a um dos quatro clusters, fizemos médias das principais métricas:

**Cluster 1** – Heavy Bulk: Predominância de carga a granel e alta tonelagem média por operação. Baixa movimentação de contêineres.

**Cluster 2** – Container Hub: Operações quase exclusivas de contêineres, com altos valores de TEUs, ideal para rotas regulares de navios porta-container.

**Cluster 3** – Mix Geral 1: Volume médio de toneladas e unidades, mas baixo fluxo de contêineres. Perfil de terminais que atendem cargas variadas de menor porte.

**Cluster 4** – Mix Geral 2: Menor média de tonelagem, mas variabilidade alta em unidades movimentadas. Indicativo de operações que precisam otimizar triagem e armazenamento.

# 4. **CONCLUSÃO**

Segmentação clara: Diferentes grupos de terminais exigem estratégias operacionais distintas.

Para terminais de granel pesado: Investir em equipamentos de descarga rápidos e áreas dedicadas para evitar acúmulo.

Para hubs de contêineres: Focar em fluxos padronizados e softwares de agendamento para evitar gargalos em berços.

Para terminais de carga geral: Revisar processos de triagem e melhorar layouts de pátio para reduzir tempo de manobra.

Em resumo, a aplicação de algoritmos de agrupamento permitiu agrupar os terminais de forma a direcionar ações específicas visando reduzir o tempo de espera dos navios e aumentar a eficiência portuária.
