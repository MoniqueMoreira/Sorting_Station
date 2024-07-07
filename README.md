Especificação do trabalho:

Uma fábrica busca automatizar o processo de uma estação de classificação, com o objetivo de separar peças numeradas de 1 a 6, conforme ilustrado na figura abaixo. As peças serão direcionadas para três recipientes distintos por meio de separadores em uma esteira transportadora. Esses separadores guiarão as peças até as saídas desejadas. As peças numeradas como 1 e 4 (com suporte Azul/Verde) serão depositadas no recipiente 1 (saída 1), as peças 2 e 5 (com tampa Azul/Verde) serão encaminhadas para a saída 2, e as peças 3 e 6 (com base Azul/Verde) serão destinadas à saída 3.

O processo se inicia quando o botão "Start" no Controlador Lógico Programável (CLP) é pressionado, ativando a “Esteira de entrada” que conduzirá as peças até um “Sensor de visão” responsável por identificar a peça de acordo com seu número. Assim que a peça for identificada, a comporta que estava fechada se abrirá, permitindo que a peça siga para a etapa de triagem na “Esteira de saída”, onde será direcionada pelas divisórias até o recipiente correto.

<div style="display: flex; justify-content: center;">
  <a name="números das Peças"></a>
  <img src="Número das Peças.png" text-align: center;">
</div>

Quando o sensor identificar uma peça numerada como 1 ou 4, o seletor (divisória) Sorter Turn 1 e a esteira Sorter Belt 1 serão acionados simultaneamente por 4 segundos, até que a triagem seja concluída e a peça, seja corretamente direcionada para o recipiente adequado. Da mesma forma, para as peças 2 ou 5, o seletor Sorter Turn 2 e a esteira Sorter Belt 2 serão acionados por 6 segundos. E para as peças 3 ou 6, o seletor Sorter Turn 3 e a esteira Sorter Belt 3 serão acionados por 8 segundos, garantindo o término da triagem. Após cada ciclo de triagem, a comporta será fechada, e a “Esteira de entrada” será reiniciada, aguardando a identificação de uma nova peça pelo sensor.
Além disso, sempre que o botão "Stop" for pressionado, a “Esteira de entrada” será interrompida até que o botão "Start" seja pressionado novamente. Um botão de emergência também foi implementado, o qual parará todo o processo quando pressionado, permanecendo nesse estado até ser desativado e o botão "Start" for pressionado novamente para reiniciar a triagem.

Após a classificação das peças e sua direção para as respectivas saídas, a quantidade de peças passando pela triagem será contabilizada por meio de um contador digital no CLP. O Contador 1 (Cont 1) registrará o número de peças na saída 1, o Contador 2 (Cont 2) na saída 2 e assim por diante. Esses contadores podem ser zerados ao pressionar o botão de “Reset” no CLP.
