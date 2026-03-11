📊 Case: Análise de Dados do Cartão Corporativo (CPGF) - Presidência da República

Objetivo: Analisar a eficiência e transparência dos gastos da Unidade Gestora 20101 (Presidência) em 2025, utilizando Python e Pandas.

🔍 Principais Descobertas:

* Composição do Gasto: Ao todo, 30,4% do volume financeiro (R$ 35,4 mil) é destinado a Saques e Gastos Sigilosos. Embora protegidos por lei, esses valores representam uma "sombra" da operação logística. o SESI foi a instituição que recebeu o maior valor no ano, provavelmente relacionado à realização de eventos.
  
* O gasto total foi de R$ 116.493,43, somando 365 transações. O ticket médio geral foi de R$ 319,16. Separando por categorias, contudo, o TM dos gastos que têm fornecedores identificados foi de R$ 247,69. Já o TM dos gastos sigilosos foi de R$ 961,76 e, dos saques R$ 900 (perfis parecidos, aliás).

* Picos de gastos, que ocorrem em quintas e sextas, provavelmente antecedem visitas presidenciais em residência particular no estado Paulista ou agenda de eventos na região.

* Logística em SP: Apesar da sede em Brasília, o maior fornecedor identificado foi o Auto Posto Parque Villa Lobos (SP), com mais de 100 transações. Isso evidencia a operação do Escalão Avançado em apoio às agendas presidenciais na capital paulista.

* Perfil Operacional: Dez servidores têm posse do cartão corporativo. Os maiores desembolsos são para manutenção da frota de veículos. Um servidor em específico parece ser responsável pela gestão dos saques.

🛠️ Stack Técnica:

* Extração: Consumo da API do Portal da Transparência com tratamento de paginação via requests.

* Tratamento: Limpeza de strings, normalização de CNPJs e conversão de tipos (BRL para Float).

* Análise Temporal: Criação de colunas de Day of Week para identificar padrões de gastos em fins de semana, Is Sigiloso para identificar gastos em CNPJs não identificados; e Is Saque para identificar valores sacados em espécie.

* Visualização: Gráficos de Pizza e Barras utilizando Matplotlib e Seaborn.
