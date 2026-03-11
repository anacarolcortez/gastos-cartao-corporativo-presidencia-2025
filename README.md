📊 Case: Análise de Dados do Cartão Corporativo (CPGF) - Presidência da República

Objetivo: Analisar a eficiência e transparência dos gastos da Unidade Gestora 20101 (Presidência) em 2025, utilizando Python e Pandas.

🔍 Principais Descobertas:

    Composição do Gasto: Ao todo, 30,4% do volume financeiro (R$ 35,4 mil) é destinado a Saques e Gastos Sigilosos. Embora protegidos por lei, esses valores representam a "fatia de sombra" da operação logística.

    Logística em SP: Apesar da sede em Brasília, o maior fornecedor identificado foi o Auto Posto Parque Villa Lobos (SP), com mais de 100 transações. Isso evidencia a operação do Escalão Avançado em apoio às agendas presidenciais na capital paulista.

    Perfil Operacional: Através do cruzamento de portador.nome e categoria_id, mapeou-se a especialização dos servidores: enquanto alguns focam na manutenção da frota (alto volume de abastecimento), outros centralizam a gestão de numerário (saques).

🛠️ Stack Técnica:

    Extração: Consumo da API do Portal da Transparência com tratamento de paginação via requests.

    Tratamento: Limpeza de strings, normalização de CNPJs e conversão de tipos (BRL para Float).

    Análise Temporal: Criação de colunas de Day of Week para identificar padrões de gastos em fins de semana, Is Sigiloso para identificar gastos em CNPJs não identificados; e Is Saque para identificar valores sacados em espécie.

    Visualização: Gráficos de Pizza e Barras utilizando Matplotlib e Seaborn.
