🍷Vinheria Agnello – Sistema de Monitoramento com Arduino
📌 Descrição do Projeto

Este projeto foi desenvolvido como parte do Checkpoint 01 da disciplina de Edge Computing

A proposta consiste na criação de um sistema de monitoramento de luminosidade utilizando Arduino, com o objetivo de garantir condições ideais de armazenamento para vinhos na Vinheria Agnello.

A qualidade do vinho pode ser afetada por fatores ambientais, especialmente a luminosidade, que pode causar reações químicas indesejadas. Portanto, o sistema foi projetado para:

Monitorar a luminosidade do ambiente em tempo real
Alertar o usuário quando os níveis estiverem inadequados
Simular um sistema inteligente de controle ambiental
🎯 Objetivo

Desenvolver um sistema embarcado capaz de:

Capturar dados de luminosidade com sensor LDR
Processar os dados usando o Arduino (conversão analógica → digital)
Exibir o status do ambiente com LEDs
Emitir alerta sonoro com buzzer em caso de problema
⚙️ Componentes Utilizados
Arduino Uno
Sensor LDR (Light Dependent Resistor)
Resistores (10kΩ para divisor de tensão)
LED Verde (estado OK)
LED Amarelo (estado de alerta)
LED Vermelho (estado crítico)
Buzzer (alarme sonoro)
Protoboard
Jumpers
🔌 Funcionamento do Sistema
📊 Leitura da Luminosidade

O sensor LDR varia sua resistência de acordo com a luz:

Mais luz → menor resistência
Menos luz → maior resistência

O Arduino lê esses valores através de uma entrada analógica (A0), convertendo-os em valores digitais (0 a 1023).

🚦 Lógica de Monitoramento

Com base nos valores lidos, o sistema classifica o ambiente em três estados:

Estado	Condição de Luz	Ação
🟢 OK	Luminosidade ideal	LED verde aceso
🟡 Alerta	Próximo do limite	LED amarelo aceso
🔴 Problema	Luminosidade alta	LED vermelho + buzzer ativo
🔊 Alarme Sonoro
Quando a luminosidade está em nível crítico:
O buzzer toca por 3 segundos
Se o problema persistir:
O alerta é acionado novamente
🔧 Montagem do Circuito
📍 Conexões principais:
LDR:
Um lado no 5V
Outro lado no A0 + resistor para GND
LEDs:
Cada LED conectado a um pino digital (ex: 8, 9, 10)
Com resistor de proteção (220Ω)
Buzzer:
Pino positivo em pino digital (ex: 7)
Negativo no GND
🧪 Simulação

O projeto pode ser simulado em:

Tinkercad
Wokwi

📌 A simulação permite validar:

Funcionamento dos LEDs
Leitura do sensor
Ativação do buzzer
🎥 Vídeo Explicativo

O vídeo deve conter:

Explicação do funcionamento do sistema
Demonstração prática
Dificuldades encontradas
Soluções adotadas

⏱️ Tempo máximo: 3 minutos

⚠️ Desafios Encontrados
Calibrar corretamente os valores do LDR
Ajustar os limites entre OK, alerta e problema
Controlar o tempo do buzzer sem travar o sistema
Organização do circuito na protoboard
🚀 Melhorias Futuras
Monitoramento de temperatura e umidade
Integração com IoT (dados na nuvem)
Aplicativo mobile para acompanhamento
Sistema automático de controle de luz
👥 Integrantes

Gustavo Braga Araujo 569211
Matheus Carvalho Piorunneck 569454
Nicholas De Lucas 571063
Leonardo Ursini 569812
Henry Gabriel 570063

📚 Referências
Material da disciplina FIAP
Documentação Arduino
Estudos sobre conservação de vinhos****
