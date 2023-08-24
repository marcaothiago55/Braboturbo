# Braçoturbo
Este código controla quatro servos motores usando um joystick analógico e quatro botões. Os servos podem ser movidos para posições diferentes por meio das entradas do joystick e dos botões. Aqui está um resumo passo a passo:

Preparação:

A biblioteca Servo.h é incluída para facilitar o controle dos servos.
São criados quatro objetos do tipo Servo para controlar os quatro servos.
Definição de Pinos:

São definidos os números dos pinos Arduino para os servos, joystick e botões.
Valores e Configurações:

Variáveis são definidas para armazenar valores lidos do joystick e para definir ângulos mínimo, máximo e incremento para os servos.
Função setup():

Os objetos dos servos são "anexados" aos pinos correspondentes usando o método attach().
Os pinos dos botões são configurados como entradas.
Função loop():

Os valores lidos do joystick (eixo X e eixo Y) são armazenados.
Os ângulos atuais dos servos 1 e 2 são lidos.
Controle dos Servos com Botões:

Se o botão D for pressionado, o ângulo do servo 1 aumenta incrementalmente.
Se o botão B for pressionado, o ângulo do servo 1 diminui incrementalmente.
Se o botão A for pressionado, o ângulo do servo 2 aumenta incrementalmente.
Se o botão C for pressionado, o ângulo do servo 2 diminui incrementalmente.
Limitação dos Ângulos:

Os ângulos dos servos 1 e 2 são limitados entre os valores mínimo e máximo usando constrain().
Controle dos Servos com o Joystick:

Os valores do eixo X do joystick são mapeados para o ângulo do servo 3.
Os valores do eixo Y do joystick são mapeados para o ângulo do servo 4.
Aplicação dos Ângulos:

Os ângulos calculados são aplicados aos quatro servos usando os métodos write().
Atraso:

Um pequeno atraso é introduzido para controlar a taxa de atualização dos servos.
O código basicamente lê os valores do joystick e dos botões, calcula os ângulos dos servos com base nas entradas e aplica esses ângulos aos servos para posicioná-los de acordo com as ações do usuário. Isso permite que os servos se movam de forma controlada, seguindo as instruções do joystick e dos botões.
