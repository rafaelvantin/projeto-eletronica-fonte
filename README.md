# Projeto Fonte Retificadora - SSC0180 Eletrônica 

> Clique [aqui](https://tinyurl.com/yfvuvstu) para acessar o circuito no falstad.

## Alunos:
*  **Matheus Giraldi Alvarenga** - 12543669
*  **Rafael Sartori Vantin** - 12543353
*  **Renato Tadeu Theodoro Junior** - 11796750
*  **Thierry de Souza Araújo** - 12681094


## Premissa:

Construir uma fonte reficadora que transforme uma corrente alternada (AC) de 127V e frequência 60Hz em corrente contínua (DC) com tensão ajustável entre 3V a 12V e com corrente igual à 100mA.

## Imagem do circuito:
![Falstad](img/circuito1.jpg)

## Componentes utilizados no projeto:

| Nome               | Quantidade | Valor Unidade | Valor R$ |
| ------------------ |-----------:| -------------:|---------:|
| Diodo              |          5 |        R$0,15 |   [R$0,75](https://www.baudaeletronica.com.br/diodo-1n4001.html?gclid=CjwKCAjwruSHBhAtEiwA_qCppsxkXFUC2Sy_gQdO0vh9f5p9KMD9ftG8ABoKyA15loVwlxWXfckyuBoCdT8QAvD_BwE) |
| Capacitor 470uF    |          1 |        R$0,45 |   [R$,0,45](https://www.baudaeletronica.com.br/capacitor-eletrolitico-470uf-25v.html) |
| Resistor 1.2kΩ     |          1 |        R$0,06 |   [R$0,06](https://www.baudaeletronica.com.br/resistor-1k2-5-1-4w.html?gclid=CjwKCAjwuvmHBhAxEiwAWAYj-JMxW1_w48xKTgLMsiLjybvp2md3GyukdLlqMQBGYN4TzrQlwvzL3RoCTYkQAvD_BwE) |
| Resistor 2.2kΩ     |          1 |        R$0,06 |   [R$0,06](https://www.baudaeletronica.com.br/resistor-2k2-5-1-4w.html?gclid=CjwKCAjwuvmHBhAxEiwAWAYj-HKgVRUoRfebU47qAxI0ci21BxgJWxEbIEHtERoLqJK7TPMF5tKNixoCJfcQAvD_BwE) |
| Potenciometro      |          1 |        R$2,21 |   [R$2,21](https://www.baudaeletronica.com.br/potenciometro-linear-de-5k-5000.html) |
| Diodo Zener (13V)  |          1 |        R$0,21 |   [R$0,21](https://www.baudaeletronica.com.br/diodo-zener-1n4743-13v-1w.html?gclid=CjwKCAjwuvmHBhAxEiwAWAYj-PsVqE9h-xFWbgh-humbM1tzDFbCvfsfjGAQCCMh2e5EPu7xwdN7ARoC6S0QAvD_BwE) |
| Transistor NPN     |          1 |        R$0,22 |   [R$0,22](https://www.baudaeletronica.com.br/transistor-npn-bc337.html) |
| Transformador      |          1 |        R$24,97|   [R$24,97](https://www.baudaeletronica.com.br/transformador-trafo-12v-12v-200ma-110-220vac.html) |

## Funcionamento de cada peça:

* **Transformador**: reduz a tensão.
 
* **Ponte de diodo**: transforma a corrente alternada em corrente contínua variável.  

* **Capacitor**: age como um reservatório, fornecendo corrente para a saída quando a tensão DC varia no retificar (suaviza a tensão).

* **Diodo Zener**: estipula uma tensão máxima, nesse caso 12V.

* **Resistores**: limita a corrente para o funcionamento correto do circuito.

* **Potenciometro**: torna possível variar a tensão de saída (entre 3V e 12V).

* **Transistor**: permite ajustar a passagem da corrente.

## Cálculos
<a href="https://www.codecogs.com/eqnedit.php?latex=Vmax&space;=&space;127&space;*&space;\sqrt{2}&space;\approx&space;180V" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Vmax&space;=&space;127&space;*&space;\sqrt{2}&space;\approx&space;180V" title="Vmax = 127 * \sqrt{2} \approx 180V" /></a>  
<a href="https://www.codecogs.com/eqnedit.php?latex=V1max&space;=&space;180&space;*&space;0,12&space;=&space;21,6V" target="_blank"><img src="https://latex.codecogs.com/gif.latex?V1max&space;=&space;180&space;*&space;0,12&space;=&space;21,6V" title="V1max = 180 * 0,12 = 21,6V" /></a>   
<a href="https://www.codecogs.com/eqnedit.php?latex=V2max&space;=&space;21,6&space;-&space;1,4&space;=&space;20,2&space;V" target="_blank"><img src="https://latex.codecogs.com/gif.latex?V2max&space;=&space;21,6&space;-&space;1,4&space;=&space;20,2&space;V" title="V2max = 21,6 - 1,4 = 20,2 V" /></a>
   
Para um ripple de **10%**:   
<a href="https://www.codecogs.com/eqnedit.php?latex=V2med&space;=&space;V2&space;*&space;[1&space;-&space;(\frac{ripple}{2})]&space;=&space;20,2&space;*&space;[1&space;-(\frac{0,1}{2})]&space;=&space;19,19&space;V" target="_blank"><img src="https://latex.codecogs.com/gif.latex?V2med&space;=&space;V2&space;*&space;[1&space;-&space;(\frac{ripple}{2})]&space;=&space;20,2&space;*&space;[1&space;-(\frac{0,1}{2})]&space;=&space;19,19&space;V" title="V2med = V2 * [1 - (\frac{ripple}{2})] = 20,2 * [1 -(\frac{0,1}{2})] = 19,19 V" /></a>   
<a href="https://www.codecogs.com/eqnedit.php?latex=V2ond&space;=&space;V2&space;*&space;ripple&space;=&space;20,2&space;*&space;0,1&space;=&space;2,02V" target="_blank"><img src="https://latex.codecogs.com/gif.latex?V2ond&space;=&space;V2&space;*&space;ripple&space;=&space;20,2&space;*&space;0,1&space;=&space;2,02V" title="V2ond = V2 * ripple = 20,2 * 0,1 = 2,02V" /></a>
 
 
 ### Correntes
 <a href="https://www.codecogs.com/eqnedit.php?latex=i(carga)&space;=&space;\frac{(Vzenner&space;-Vt)}{Rcarga}&space;=&space;\frac{13-0,7}{120}&space;=&space;0,1025A" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i(carga)&space;=&space;\frac{(Vzenner&space;-Vt)}{Rcarga}&space;=&space;\frac{13-0,7}{120}&space;=&space;0,1025A" title="i(carga) = \frac{(Vzenner -Vt)}{Rcarga} = \frac{13-0,7}{120} = 0,1025A" /></a>   
 <a href="https://www.codecogs.com/eqnedit.php?latex=i(zenner)&space;=&space;\frac{V2med&space;-&space;Vzenner}{R}&space;=&space;\frac{19,19&space;-&space;13}{1200}&space;=&space;0,00516A" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i(zenner)&space;=&space;\frac{V2med&space;-&space;Vzenner}{R}&space;=&space;\frac{19,19&space;-&space;13}{1200}&space;=&space;0,00516A" title="i(zenner) = \frac{V2med - Vzenner}{R} = \frac{19,19 - 13}{1200} = 0,00516A" /></a>  
 <a href="https://www.codecogs.com/eqnedit.php?latex=i(potenc)&space;=&space;\frac{V2med}{R&plus;R&plus;R}&space;=&space;\frac{19,19}{1,2k&plus;5k&plus;2,2k}&space;=&space;0,0023A" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i(potenc)&space;=&space;\frac{V2med}{R&plus;R&plus;R}&space;=&space;\frac{19,19}{1,2k&plus;5k&plus;2,2k}&space;=&space;0,0023A" title="i(potenc) = \frac{V2med}{R+R+R} = \frac{19,19}{1,2k+5k+2,2k} = 0,0023A" /></a>  
 <a href="https://www.codecogs.com/eqnedit.php?latex=i(total)&space;=&space;0,1025&space;&plus;&space;0,00516&space;&plus;&space;0,0023&space;=&space;0,10996A" target="_blank"><img src="https://latex.codecogs.com/gif.latex?i(total)&space;=&space;0,1025&space;&plus;&space;0,00516&space;&plus;&space;0,0023&space;=&space;0,10996A" title="i(total) = 0,1025 + 0,00516 + 0,0023 = 0,10996A" /></a>  
 
 ### Capacitor
 
 <a href="https://www.codecogs.com/eqnedit.php?latex=C&space;=&space;\frac{i(total)}{2*f*V2ond}&space;=&space;\frac{0,10996}{120*2,02}&space;=&space;453*10^{-6}F" target="_blank"><img src="https://latex.codecogs.com/gif.latex?C&space;=&space;\frac{i(total)}{2*f*V2ond}&space;=&space;\frac{0,10996}{120*2,02}&space;=&space;453*10^{-6}F" title="C = \frac{i(total)}{f*V2ond} = \frac{0,10996}{120*2,02} = 453*10^{-6}F" /></a>
 
 Para obter um valor comercial utilizaremos um capacitor de:
 <a href="https://www.codecogs.com/eqnedit.php?latex={\color{Red}&space;470&space;*&space;10^{-6}F}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{\color{Red}&space;470&space;*&space;10^{-6}F}" title="{\color{Red} 470 * 10^{-6}F}" /></a>
 


## Esquemático EAGLE:
![Esquemático](img/esquematico.jpeg)

## Simulação EAGLE:
![Simulação](img/pcb.jpeg)
