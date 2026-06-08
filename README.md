# **Conteúdo do README.md**
# Equipe
- Enzo Miguel de Oliveira Silva - rm571639
- Gabriel da Silva Amaral - rm570421
- Giovanni Dutra Dias - rm572671
- Pedro Aulicino Corrêa Coelho - rm570804
- Pedro Henrique Benício Santana Braga - rm572066

# Introdução ao Problema
Criar um simulador de um painel de controle para uma missão espacial.

# Dados Utilizados

O arquivo "dados.csv" contém informações organizadas em cinco categorias principais:

1. **Status dos Módulos:** Indica se cada sistema crítico está ativo ou inativo.

2. **Telemetria de Energia:** Registra consumo e geração de energia durante diferentes fases da missão.

3. **Variáveis Ambientais:** Reúne dados como temperatura, oxigênio, CO₂, comunicação e ventos.

4. **Log de Eventos:** Lista alertas e falhas para análise de erros e decisões.

5. **Reserva de Energia:** Porcentagem de energia disponível, usada para prever a tendência de queda.

# Regras Lógicas do Sistema
Para avaliar a segurança e definir o estado operacional da missão, o sistema aplica testes lógicos baseados nos dados coletados:

O programa cruza dados de atmosfera e temperatura usando operadores lógicos como AND, OR e NOT.

Uma falha é detectada se o suporte à vida desligar, se os gases saírem da faixa segura ou se algum motor falhar.

O sistema analisa a Pilha de Críticos e a previsão de bateria para definir o status final como NORMAL, ALERTA ou CRÍTICO.


# Técnica de Previsão
Para prever a tendência de queda da reserva de energia, foi usado um algoritmo simples de regressão linear:
- Os valores históricos de reserva são extraídos do arquivo dados.csv.
- A regressão calcula a taxa média de variação da energia a cada medição.
- Com base nessa tendência, o algoritmo estima o percentual de energia disponível em medições futuras.

# Recomendações do Sistema
Com base no status geral definido pelas regras, o painel gera ações automáticas.

Status Crítico: Ordena o corte imediato de energia de setores secundários (como laboratórios) e exige manutenção urgente no erro do topo da pilha.

Status de Alerta: Prescreve ações preventivas, como ativar modos de economia de bateria e monitorar sensores mais de perto.

Status Normal: Autoriza a tripulação a manter o plano de voo padrão e a rotina normal de pesquisas científicas.

# Como Executar o Código
 - Clique no botão "play" na primeira célula para gerar os dados.
 - Clique no botão "play" na segunda célula para gerar a interface da telemetria.

# Link para o Vídeo

# Conclusão
O desenvolvimento deste sistema inteligente de monitoramento demonstrou a importância do pensamento computacional e das estruturas de dados em cenários de missão crítica. Através da divisão correta de responsabilidades entre listas, dicionários, filas e pilhas, o software foi capaz de processar telemetrias espaciais complexas em tempo real. A integração do algoritmo de regressão linear provou como a análise preditiva pode antecipar falhas de energia e guiar recomendações técnicas automatizadas, garantindo de forma ética e segura a integridade dos equipamentos e a sobrevivência da tripulação.
