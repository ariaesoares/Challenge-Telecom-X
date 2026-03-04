# Challenge-Telecom-X

Análise de Churn TelecomX

Este projeto tem como objetivo principal analisar a evasão de clientes (Churn) na TelecomX, identificando os principais fatores que levam os clientes a cancelar seus serviços. Através de uma abordagem orientada por dados, buscaremos desvendar padrões de Churn para fundamentar a proposição de estratégias eficazes de retenção de clientes.

A compreensão do Churn é de suma importância para qualquer empresa de telecomunicações. A alta taxa de evasão impacta diretamente a receita e lucratividade, pois os custos de aquisição de novos clientes são significativamente mais altos do que os de retenção. Ao mitigar o Churn, a TelecomX pode garantir uma base de clientes mais estável e rentável, otimizando investimentos em marketing e melhorando a percepção de valor dos seus serviços.


🎯 Objetivo
Identificar os principais fatores que levam à evasão de clientes (Churn) na TelecomX.
Propor estratégias de retenção baseadas em dados para reduzir o Churn e otimizar a lucratividade.

🗂️ Preparação de Dados

Extração: Carregamento de dados JSON aninhados do GitHub.
Normalização: Achatamento de colunas aninhadas (cliente, telefone, internet, conta) para um DataFrame plano usando pd.json_normalize.
Limpeza: Remoção de valores vazios em 'Churn' e conversão de para numérico, tratando nulos.
Transformação: Criação de 'contas diárias', renomeação de colunas e tradução de valores categóricos para português.

📊 Principais Descobertas 

Taxa Geral de Churn: 26.58% dos clientes evadem, enquanto 73.4% permaneceram.
<img width="471" height="470" alt="image" src="https://github.com/user-attachments/assets/7c8cd32d-c6d6-4fba-89e0-8db0a5d9631e" />

Tipo de Contrato:  Clientes com contratos 'Mês a mês' apresentaram uma taxa de Churn alarmante de 23.53%, em contraste com os contratos de 'Um ano' (2.36%) e 'Dois anos' (0.68%). A flexibilidade desses contratos permite que os clientes cancelem facilmente ao menor sinal de insatisfação ou ao encontrar uma oferta mais atraente da concorrência.
<img width="859" height="701" alt="image" src="https://github.com/user-attachments/assets/50dd47e0-b317-4cb7-8411-7c35fd43b6e8" />


Tempo de Contrato: O risco de Churn é exponencialmente maior nos primeiros meses de serviço. O pico de Churn ocorre no primeiro mês (61.99%), seguido de altas taxas nos meses subsequentes (2 meses: 51.68%, 3 meses: 47.00%). Isso indica que a experiência inicial do cliente é um fator crítico para a retenção, e qualquer falha nesse período leva a uma evasão rápida. diminuindo drasticamente com a permanência.

<img width="1539" height="470" alt="image" src="https://github.com/user-attachments/assets/56b72318-37bc-406a-b632-8c252a988eb4" />


Serviços (Fibra Óptica): Observou-se que 'Fibra óptica' é um tipo de internet de alta demanda. A satisfação e a performance dos serviços de internet são cruciais, e problemas nesse setor podem levar ao Churn, especialmente em contratos de curto prazo.
<img width="859" height="702" alt="image" src="https://github.com/user-attachments/assets/e8b6143b-091a-4f8a-b9a1-26364aa3ef9c" />



Pagamento (Cheque Eletrônico): Clientes que utilizam 'Cheque eletrônico' como método de pagamento tendem a ter uma taxa de churn ligeiramente maior (45.31%) em comparação com outros métodos de pagamento. Isso pode indicar uma menor lealdade ou uma facilidade maior para cancelar o serviço.
<img width="979" height="590" alt="image" src="https://github.com/user-attachments/assets/843eb5e0-b952-4825-af63-7c9938177af2" />

Em resumo, o mapa de calor confirma que as métricas financeiras (Valor Mensal, total cobrado e contas diarias) e a duração do contrato (Tempo de contrato) estão interligadas, e o comportamento de Tempo de contrato é crucial para entender o Churn. Já a Senioridade parece não ser um fator forte entre as variáveis numéricas.

<img width="762" height="590" alt="image" src="https://github.com/user-attachments/assets/ba57e32d-23b4-4ed1-a545-eec0c2b53a4c" />

*O mapa de calor mostra a relação entre as variáveis numéricas. Valores próximos de 1 ou -1 indicam forte correlação (positiva/negativa), enquanto valores próximos de 0 indicam pouca relação.*

🚀 Recomendações Estratégicas


1.  **Incentivar Contratos de Longo Prazo:** Oferecer benefícios exclusivos (descontos, upgrades, meses grátis) para clientes migrarem de contratos Mês a Mês para planos de 1 ou 2 anos.
2.  **Melhorar a Experiência nos Primeiros Meses (Onboarding):** Implementar um programa robusto de 3-5 meses com suporte proativo, verificações de satisfação e comunicação simplificada para resolver problemas rapidamente e fortalecer a lealdade.
3.  **Reavaliar Precificação/Valor Percebido (Contratos Mês a Mês):** Analisar a estrutura de preços e considerar pacotes flexíveis com incentivos de fidelidade ou ajustes de preço para direcionar a escolha do cliente para planos mais estáveis.
4.  **Otimizar Suporte (Internet e Pagamento):** Investigar causas de insatisfação entre usuários de Fibra Óptica e Cheque Eletrônico para aprimorar a qualidade da conexão, tempo de resposta do suporte e facilidade de uso do método de pagamento.

### Conclusão

A TelecomX enfrenta um desafio considerável com sua taxa de Churn. Os esforços de retenção devem ser direcionados primordialmente para a transição de clientes de contratos 'Mês a mês' para opções de longo prazo e para aprimorar drasticamente a experiência do cliente durante os primeiros meses de serviço. Ao implementar essas sugestões, a TelecomX estará em uma posição muito mais forte para estabilizar sua base de clientes e garantir um crescimento sustentável.




