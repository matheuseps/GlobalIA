Projeto de Monitoramento IoT com ESP32 e Thinger.io
Este projeto utiliza o microcontrolador ESP32 para monitorar o nível de energia de uma bateria e a temperatura ambiente, além de controlar um atuador (como uma lâmpada). Os dados coletados são enviados para a plataforma Thinger.io, que oferece uma interface para monitoramento e controle de dispositivos IoT.

Índice
Descrição do Projeto
Materiais Necessários
Configuração
Integração com o Thinger.io
Funcionamento do Projeto
Contribuições
Licença
Descrição do Projeto
O projeto foi desenvolvido para explorar as possibilidades da Internet das Coisas (IoT) utilizando o ESP32 como dispositivo principal. Ele é capaz de:

Enviar dados como nível de bateria e temperatura para a plataforma Thinger.io.
Controlar um atuador, como ligar/desligar uma lâmpada remotamente.
Oferecer uma interface amigável no Thinger.io para monitorar as leituras em tempo real.
O projeto é uma introdução prática à IoT, conectando sensores e dispositivos físicos à nuvem para monitoramento e automação.

Materiais Necessários
ESP32: Microcontrolador com suporte a Wi-Fi.
Sensor de Temperatura: Pode ser o DHT11 ou DHT22.
Atuador: Como uma lâmpada ou LED.
Fonte de Energia/Bateria: Para simular o nível de energia monitorado.
Conexão Wi-Fi: Necessária para integrar o ESP32 ao Thinger.io.
Configuração
1. Configuração do Thinger.io
Criar Conta: Acesse o Thinger.io e crie uma conta gratuita.
Adicionar Dispositivo:
Acesse a aba Devices e crie um novo dispositivo (exemplo: bateria2).
Configure os seguintes Properties para o dispositivo:
nivel_energia: Para monitorar o nível da bateria.
temperatura: Para monitorar a temperatura ambiente.
atuador: Para controlar um dispositivo como uma lâmpada.
Gerar Token: No painel do dispositivo, gere um Device Token e copie o valor para usar no código.
2. Configuração do Ambiente de Desenvolvimento
Arduino IDE: Configure a IDE para programar o ESP32.
Adicione a URL para placas ESP32 em Preferences.
Instale a biblioteca para ESP32 através do Boards Manager.
Bibliotecas Adicionais: Certifique-se de ter as bibliotecas de suporte ao ESP32, Wi-Fi e HTTP instaladas.
Integração com o Thinger.io
O ESP32 se conecta ao Thinger.io através de APIs HTTP. Para cada Propriedade configurada no Thinger.io, uma URL correspondente será utilizada para envio ou recebimento de dados. Exemplos de propriedades configuradas no Thinger.io:

Nivel_energia: Monitoramento do nível de bateria.
Temperatura: Leitura do sensor de temperatura.
Atuador: Controle remoto de um dispositivo.
O ESP32 envia dados de nível de energia e temperatura, além de alternar o estado do atuador com base nos comandos recebidos do Thinger.io.

Funcionamento do Projeto
Monitoramento de Dados:

O ESP32 coleta os dados do sensor de temperatura e do nível de energia da bateria.
Estes dados são enviados periodicamente para o Thinger.io.
Controle Remoto:

Um atuador pode ser controlado diretamente pela interface do Thinger.io, permitindo ligar ou desligar dispositivos conectados ao ESP32.
Feedback em Tempo Real:

As leituras e o estado do atuador são exibidos em tempo real no painel da plataforma.
Contribuições
Contribuições são bem-vindas! Se você encontrar problemas ou tiver ideias para melhorias, sinta-se à vontade para:

Abrir um Issue detalhando o problema ou sugestão.
Enviar um Pull Request com melhorias no código ou documentação.
Licença
Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.
