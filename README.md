<h1 align="center"> WaterWorkers🚰 -- Monitoramento de Bueiros ⚫</h1>
A WaterWorkers é uma startup inovadora dedicada a aprimorar a infraestrutura de escoamento de água em áreas urbanas afetadas por alagamentos e enchentes recorrentes. Nosso objetivo é desenvolver soluções inteligentes e sustentáveis que reduzam os impactos das chuvas intensas, promovendo cidades mais resilientes, seguras e preparadas para os desafios climáticos do futuro.


## 🔴 Problema
As enchentes no Brasil não são fenômenos inesperados, mas consequências de falhas estruturais persistentes. Além das mudanças climáticas, que intensificam os eventos extremos, o problema está enraizado na falta de políticas públicas eficazes, no planejamento urbano precário e na ausência de infraestrutura adequada para o escoamento da água. A ocupação desordenada do solo, o descaso com áreas de risco e a baixa capacidade de prevenção tornam as tragédias inevitáveis e recorrentes.


## 💡 Solução
A mitigação de alagamentos em áreas urbanas exige um controle rigoroso da qualidade dos sistemas de drenagem e a identificação precisa das regiões que demandam intervenções estruturais. Essa análise deve levar em consideração não apenas o volume pluviométrico, mas também as características topográficas locais, uma vez que áreas situadas em regiões de depressão apresentam maior propensão a inundações.
Diante desse cenário, propomos a implementação de um sistema composto por duas frentes de atuação complementares:
1. Módulo de alerta em tempo real, voltado à segurança de pedestres e motoristas que transitam por áreas com risco iminente de alagamento;
2. Sistema de monitoramento inteligente, responsável por captar e transmitir informações sobre a localização e as condições operacionais dos bueiros diretamente às autoridades municipais, permitindo uma gestão mais eficaz da infraestrutura urbana e subsidiando a formulação de políticas públicas mais assertivas.

Os principais resultados dessas medições indicarão se o bueiro está comprometido durante períodos de chuva e se o volume de água direcionado a ele está dentro da sua capacidade de escoamento. Esses dados serão enviados à prefeitura, que poderá tomar as medidas necessárias para aprimorar a infraestrutura local por meio de políticas públicas adequadas.


## 🛠️ Detalhes Técnicos
Para medir o nível da água dentro de bueiros ou o fluxo de água em sarjetas, utilizaremos o sensor ultrassônico HC-SR04. Esse sensor funciona emitindo pulsos sonoros e medindo o tempo que esses pulsos levam para retornar após atingirem a superfície. A partir disso, ele calcula a distância entre o sensor e o nível da água.

O funcionamento do sensor se dá por meio de dois pinos principais: TRIG e ECHO. Para iniciar uma medição, o pino TRIG deve ser ativado com um pulso de pelo menos 10 microssegundos. Em seguida, o pino ECHO permanecerá em nível alto pelo tempo correspondente à ida e volta do sinal ultrassônico. A duração desse pulso é diretamente proporcional à distância medida. O sensor é capaz de medir distâncias entre 2 cm e 400 cm com boa precisão.

Com essas medições, é possível determinar com exatidão se o nível da água está dentro dos padrões esperados. A partir desses dados, podemos criar alertas para pedestres em caso de risco, além de enviar relatórios detalhados para a prefeitura, contribuindo para o monitoramento e a manutenção eficiente dos sistemas de drenagem urbana.


## 🖲️ Requisitos Funcionais
1. Será feita uma leitura da distância entre o topo do poste e o chão, utilizando um sensor ultrassônico, para calcular o nível de água na rua. 
2. Será feita uma leitura da base do poste até a profundidade do bueiro, também usando um sensor ultrassônico, para calcular o volume de água acumulada no bueiro. 
3. As leituras são feitas a cada segundo e, após 5 leituras, é calculada a média para definir o nível de água no bueiro e na sarjeta. 
4. Caso o volume de água no bueiro esteja entre 0 e 30 cm, o LED verde deve acender, indicando situação normal. 
5. Caso o volume de água na sarjeta esteja entre 0 e 2 cm, o monitor deve imprimir —> *"Fluxo de água: Inexistente"*
6. Caso o volume de água no bueiro esteja entre 30 e 60 cm, o LED amarelo deve permanecer aceso, indicando um alerta. 
7. Caso o volume de água na sarjeta esteja entre 2 e 6 cm, o Serial deve imprimir —> *"Fluxo de água: Baixo"*
8. Caso o volume de água na sarjeta esteja entre 7 e 10 cm, o Serial deve imprimir —> *"Fluxo de água: Médio*"
9. Caso o volume de água no bueiro ultrapasse 60 cm, o LED vermelho deve acender, indicando perigo. 
10. Caso o volume de água na sarjeta ultrapasse 10 cm, o Serial deve imprimir: *"Fluxo de água: Elevado"*
11. *Como função futura, todos os status impressos no Serial devem ser enviados à prefeitura para monitoramento e controle desses dados*

## 🧭 Material
- 01 Arduino UNO = Para controlar o sistema
- 01 Breadboard = Para montagem do circuito
- Cabos Jumper = Para realizar as conexões na breadboard
- 03 Resistores = 220 Ohms para os Leds
- 01 LED Verde 🟢 = Indicar que o status do bueiro está dentro dos parâmetros
- 01 LED Amarelo 🟡 = Indicar que o status do bueiro está fora dos parâmetros
- 01 LED Vermelho 🔴 = Indicar que o bueiro está a ponto de alagar
- 02 Sensores HC-SR04 = Medir as distâncias do poste até o bueiro e do poste até a sarjeta


## 🔗Como acessar o projeto
Para acessar o diagrama do projeto [clique aqui](https://wokwi.com/projects/432402831622526977)

Link para o vídeo sobre o projeto: [clique aqui]()

## 🧰 Tecnologias utilizadas
- Linguagem de programação: C
- Microcontrolador: Arduino R3 UNO
- Prototipagem: Wokwi
- Repositório Remoto: Github


## 🧑‍💻 Equipe
<table>
  <tr><th><span>Integrantes</span></th><th><span>Tarefas</span></th></tr>
  <tr>
    <td align = "center">
      <img src="https://avatars.githubusercontent.com/u/73716198?v=4" width="100px" alt= "Adrian de Souza Profile Image" /><p><a href = "https://github.com/AdrianSouz">Adrian de Souza</a></p><span><b>RM:562959</b></span>
    </td>
    <td>
      <ul>
        <li>Montagem da protoboard</li>
        <li>Declaração dos sensores e variaveis</li>
      </ul>
    </td>
  </tr>
    <tr>
    <td align = "center">
      <img src="https://avatars.githubusercontent.com/u/202196268?v=4" width="100px" alt= "Camila Martins Profile Image"/><p><a href = "https://github.com/dev-camila">Camila Martins</a></p><span><b>RM:561492</b></span>
    </td>
    <td>
      <ul>
        <li>Setup da leitura dos Sensores</li>
      </ul>
    </td>
  </tr>
    <tr>
    <td align = "center">
      <img src="https://avatars.githubusercontent.com/u/80047823?v=4" width="100px" alt= "Gabriel Amara Profile Image"/><p><a href = "https://github.com/gabrielamara98">Gabriel Amara</a></p><span><b>RM:561403</b></span>
    </td>
    <td>
      <ul>
        <li>Gestão do README e repositório</li>
        <li>Condicionais do código</li>
        <li>Revisão e melhoria do código</li>
      </ul>
    </td>
  </tr>
</table>

## 📓 Notas:
Projeto: WaterWorkers

Repositório que servirá como Global Solution na disciplina de Edge.

Professor avaliador: Lucas Demetrius Augusto


