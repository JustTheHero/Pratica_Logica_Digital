# Pratica Logica Digital
Boa tarde a todos, sou o Juan, ou Hero, como preferirem me chamar. Criei este repositório com o intuito de auxiliar vocês, calouros, que enfrentam dificuldades nas disciplinas ministradas pelos professores Delben e Bonato. Reconheço que ambos não são os melhores em explicar os conteúdos, especialmente o Bonato, conhecido como Daibo.

É importante ressaltar que Delben não é o único responsável pelas dificuldades enfrentadas com o Quartus. Na verdade, o ideal seria aprender os conceitos na teoria e depois aplicá-los na prática. Entretanto, muitas vezes não conseguimos absorver os conhecimentos teóricos adequadamente e acabamos tendo que lidar com os desafios diretamente na prática.

Porém, problemas básicos com o incrível programa Quartus, juntamente com dicas úteis de utilização, deveriam ser fornecidos pelo próprio Delben. Portanto, este repositório pode ser uma ferramenta valiosa para ajudá-los a superar as dificuldades encontradas na disciplina.

Funcionamento básico:
- **NÂO COPIEM IGUAL OS PROJETOS**, o professor tem um programa que detecta plágio nos trabalhos
- Os projetos são arquivos .bdf, isso siginifica que são os desenhos de fios e blocos, ao baixar eles vocês só precisam abrir ele pra ver como fazer
- Alguns arquivos são .qar você só precisa executar e o quartus mostra tudo
- blocos serão ensinados para vocês diretamente pelo professor quando for preciso
- Os vídeos do youtube são do professor Wolf, um amor de gente
- Sempre tentem fazer os projetos ou ao menos entenderem como funcionam, são úteis para a aula teórica como também para o próximo semestre
- Não odeiem o Quartus, ele só é mal compreendido
                      
Além disso, estou à disposição para fornecer dicas sobre o uso do Quartus, ou criar um repositório sobre isso no futuro a depender da demanda.

Espero que este recurso possa ser útil e facilite a jornada de vocês na disciplina.

# [Planilha](https://docs.google.com/spreadsheets/d/1EsQdG-ofeiXdWNgFS78QMulvIu50h9WTIs8xf9yYmWk/edit?usp=sharing) com a pinagem das placas Cyclone IV e V

# Projeto 1-3 (Simplificação de Lógica)
Projetos mais básicos na disciplina são valiosos para consolidar o aprendizado e enfrentar desafios que ajudam a compreender os conceitos trabalhados. Às vezes, esses projetos podem parecer confusos no início, levando a discussões intensas com os amigos enquanto tentamos decifrar o sentido por trás de cada detalhe. No entanto, essa jornada de descoberta é parte essencial do processo de aprendizado.

Não considero produtivo disponibilizar esses projetos aqui, pois acredito que todos nós precisamos tomar no boga e superar obstáculos para desenvolvermos nosso caráter e nos acostumarmos com as dificuldades da vida universitária. Essas experiências nos ensinam a manter a sanidade(ou tentar).

Lembre-se, a jornada acadêmica é uma oportunidade para desenvolver habilidades não apenas técnicas, mas também emocionais, de enfrentamento e segurar o choro pra quando faltar 0.1 para passar na matéria.

# Projeto 4 (display de 7 segmentos)

Um display de sete segmentos é um dispositivo de saída usado para exibir números, letras e alguns caracteres especiais. Consiste em sete segmentos de LED (Light Emitting Diode)  disposto na forma de um "8", com um segmento adicional no meio para representar um ponto decimal, se necessário. Cada segmento é denominado de "a" a "g" e pode ser aceso ou apagado independentemente dos outros segmentos.

A lógica por trás de um display de sete segmentos envolve a ativação seletiva dos segmentos necessários para exibir um determinado caractere. Cada caractere (número, letra ou símbolo) pode ser representado pela combinação específica dos segmentos a serem acesos.

Façam a tabela verdade para descobrir qual entrada deve estar ativa para formar um padrão no display, todos os futuros projetos usaram esse display, façam bem feito.

[link projeto 4](https://drive.google.com/file/d/1S8kVGjhhNhjH1L9cxqgI6szF9eO_xgJY/view?usp=sharing)

[vídeo ytb explicando](https://www.youtube.com/watch?v=ZM2W9vT_aHA&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=4)


# Projeto 5-6 (Somador 1 e 4 Bits)
## Somador de 1 Bit:
Um somador de 1 bit é o bloco fundamental usado em somadores de múltiplos bits. Ele executa a adição binária de dois bits de entrada, produzindo uma soma e um bit de transporte.

Um somador de 1 bit pode ser representado por uma tabela verdade da seguinte forma:

| A	| B	| Cin	| S	| Cout |
| :---: | :---: | :---:| :---: | :---: |
| 0	| 0	| 0	| 0	| 0
| 0	| 0	| 1	| 1	| 0
| 0	| 1	| 0	| 1	| 0
| 0	| 1	| 1	| 0	| 1
| 1	| 0	| 0	| 1	| 0
| 1	| 0	| 1	| 0	| 1
| 1	| 1	| 0	| 0	| 1
| 1	| 1	| 1	| 1	| 1

A e B são os bits de entrada que queremos somar.

Cin é o bit de transporte de entrada.

S é a saída, que representa o resultado da soma dos bits A, B e Cin.

Cout é o bit de transporte de saída, que indica se houve ou não um transporte para o próximo bit.

## Somador de 4 Bits:
Um somador de 4 bits é construído combinando quatro somadores de 1 bit em cascata. Os bits de entrada A e B de cada somador correspondem aos bits correspondentes dos números que queremos somar. O bit de transporte de entrada (Cin) do somador menos significativo é geralmente 0, enquanto o bit de transporte de saída (Cout) do somador mais significativo é ignorado ou tratado como overflow, dependendo da aplicação.

Por exemplo, para somar dois números de 4 bits (A3A2A1A0 e B3B2B1B0), podemos conectar quatro somadores de 1 bit em série, de modo que:

A3 e B3 são os bits de entrada para o somador mais significativo.

A2 e B2 são os bits de entrada para o segundo somador.

A1 e B1 são os bits de entrada para o terceiro somador.

A0 e B0 são os bits de entrada para o somador menos significativo.

O resultado da soma é então formado pelos bits de saída (S3S2S1S0) de cada somador. Se houver um overflow (Cout) do somador mais significativo, ele é tratado de acordo com os requisitos da aplicação.

Assim, um somador de 4 bits nos permite somar dois números de até 4 bits cada e produzir um resultado de até 5 bits (4 bits para a soma e 1 bit para o possível overflow).

[link projeto 5](https://drive.google.com/file/d/1jlhHfaqtEYOftN-mse0jo2Ob2_H2ZTDS/view?usp=sharing)

[link projeto 6](https://drive.google.com/file/d/19MzSeGjlwfyy4jfjTf1e4Y7mtMzhWq-q/view?usp=sharing)

[vídeo ytb explicando](https://www.youtube.com/watch?v=kP2PZ3hUDRM&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=5)

# Projeto 7-8 (Subtrator 1 e 4 Bits)
## Subtatrator de 1 Bit:
Um subtrator de 1 bit é semelhante a um somador de 1 bit, mas opera na lógica de subtração. Ele tem duas entradas (A e B) e uma saída (D) que representa a diferença.

O subtrator de 1 bit pode ser implementado de várias maneiras, sendo a mais comum a utilização de portas lógicas como XOR, AND e NOT. Basicamente, a ideia é inverter o bit de subtraendo (B) e somá-lo ao minuendo (A) juntamente com um bit de "empréstimo" (Borrow).

A tabela verdade para um subtrator de 1 bit é a seguinte:

| A |	B	| Borrow	| D |
| :---: | :---: | :---: |:---: |
| 0	| 0	| 0	| 0 |
| 0	| 0	| 1	| 1 |
| 0	| 1	| 0	| 1 |
| 0	| 1	| 1	| 0 |
| 1	| 0	| 0	| 1 |
| 1	| 0	| 1	| 0 |
| 1	| 1	| 0	| 0 |
| 1	| 1	| 1	| 1 |

A e B são os bits de entrada, representando o minuendo e o subtraendo, respectivamente.

Borrow é o bit de "empréstimo" ou "vai-um" que indica se é necessário emprestar do próximo bit superior.

D é a saída, representando o resultado da subtração.

## Subtrator de 4 Bits:

Um subtrator de 4 bits é construído da mesma forma que um subtrator de 1 bit, mas é aplicado em cada par de bits correspondentes dos números de entrada. A operação é realizada em cascata, de forma semelhante a um somador de 4 bits.

A saída de um subtrator de 4 bits consiste em quatro bits, representando o resultado da subtração dos números de 4 bits de entrada. Se houver um "empréstimo" do bit mais significativo, ele pode ser tratado de acordo com as necessidades da aplicação.

Basicamente, um subtrator de 4 bits permite subtrair um número de 4 bits de outro número de 4 bits e produzir um resultado de até 4 bits. O processo é semelhante à subtração manual, mas executado de forma eletrônica e em paralelo para cada par de bits correspondentes.

[link projeto 7](https://drive.google.com/file/d/1eKgN3sSb4LZzXpjX6zlrZS79upnTSEN2/view?usp=sharing)

[link projeto 8](https://drive.google.com/file/d/1Thae6tJ4mf1MVOJo3oTuaCR3w20z258L/view?usp=sharing)

[vídeo ytb explicando](https://www.youtube.com/watch?v=2-XW8rloK-I&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=6)

# Projeto 9 (Subtrator com Complemento de 2)
Um subtrator em complemento de 2 com 4 bits é um circuito lógico que realiza a subtração de números binários usando a representação em complemento de 2. Essa técnica permite realizar a subtração de números com sinal, ou seja, números positivos e negativos, usando a mesma operação de adição.

A representação em complemento de 2 é muito utilizada em computadores para representar números inteiros. Nessa representação, o bit mais significativo (o bit mais à esquerda) indica o sinal do número: 0 para positivo e 1 para negativo. Os números positivos são representados normalmente em binário, enquanto os números negativos são representados pelo complemento de 2 do valor absoluto do número.

Aqui está um exemplo da representação em complemento de 2 para números de 4 bits:

- O número 5 em binário é 0101.
- O número -5 é representado pelo complemento de 2 de 5, que é obtido invertendo todos os bits de 5 e adicionando 1: 1011.

Para subtrair dois números em complemento de 2, podemos usar o mesmo circuito de adição, mas complementar o subtraendo (B) e adicionar 1 ao resultado. Isso é necessário para lidar com o bit de "empréstimo" quando subtraímos um número negativo.

Aqui está o procedimento passo a passo para subtrair dois números em complemento de 2 com 4 bits:

1. Inverta todos os bits do subtraendo (B).
2. Adicione 1 ao resultado da operação de adição entre o minuendo (A) e o complemento de 2 do subtraendo.
3. Ignore qualquer overflow do bit mais significativo (Cout).

O resultado é o resultado da subtração dos dois números em complemento de 2.

Este circuito é implementado em cascata de somadores de 1 bit, assim como um subtrator convencional, mas com um ajuste adicional para lidar com o bit de "empréstimo" e garantir que a operação de subtração funcione corretamente para números positivos e negativos. 

[link projeto 9](https://drive.google.com/file/d/1QkdeMnzof1Sp5TpJ6TSUnuK9-rOwIAkp/view?usp=sharing)

[vídeo ytb explicando](https://www.youtube.com/watch?v=A25zZZK6Zug&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=7)

# Projeto 10 (Multiplicador)
A multiplicação de dois números binários é realizada usando o método convencional de multiplicação, semelhante à multiplicação manual. O multiplicador de 4 bits opera em paralelo, multiplicando cada bit do multiplicando pelo multiplicador e acumulando os resultados.

Aqui está um exemplo passo a passo de como um multiplicador de 4 bits opera:

1. O multiplicador de 4 bits recebe dois números de entrada, o multiplicando (A) e o multiplicador (B), ambos de 4 bits cada.
2. Para cada bit do multiplicador (B), o multiplicador de 4 bits realiza uma multiplicação parcial com o multiplicando (A). Isso é feito multiplicando cada bit do multiplicando por cada bit do multiplicador e acumulando os resultados.
3. Os resultados parciais da multiplicação são somados em um somador de 4 bits para obter o resultado final da multiplicação.
4. O resultado final é um número de 8 bits, representando o produto dos dois números de entrada.

O circuito de um multiplicador de 4 bits é composto por vários blocos de somadores de 4 bits e portas lógicas para realizar as multiplicações parciais e a soma dos resultados. A multiplicação é feita em paralelo para todos os bits do multiplicador, tornando o processo rápido e eficiente.

[link projeto 10](https://drive.google.com/file/d/1Ht0Zu-OWctxdWtsQcDX4aM0ZATDKz9IH/view?usp=sharing)

[vídeo do ytb explicando](https://www.youtube.com/watch?v=5PVTKN-jxA4&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=9)

# Projeto 11 (Divisor)
O processo de divisão binária é semelhante à divisão longa em aritmética decimal. Para dividir dois números binários, o divisor é subtraído repetidamente do dividendo até que o resto seja menor que o divisor. O resultado da divisão é o quociente, e o resto é o resultado final da divisão.

Aqui está um exemplo de como um divisor de 4 bits poderia operar:

1. O divisor de 4 bits recebe dois números de entrada, o dividendo (A) e o divisor (B), ambos de 4 bits cada.
2. O divisor é subtraído repetidamente do dividendo até que o resto seja menor que o divisor.
3. A cada subtração, o quociente é atualizado e o dividendo é deslocado para a esquerda (ou seja, um bit é removido do dividendo e adicionado ao resto).
4. O processo continua até que o resto seja menor que o divisor.
5. O resultado final da divisão é o quociente, e o resto é o resultado da divisão.

Implementar um divisor de 4 bits é mais complexo do que um multiplicador de 4 bits devido à natureza iterativa do algoritmo de divisão. Requer o uso de circuitos lógicos combinacionais e sequenciais, para realizar as operações de subtração e deslocamento necessárias para realizar a divisão.

[link projeto 11](https://drive.google.com/file/d/1stAzpPSj_q1h_woiRgqjR05pTLTPIS9j/view?usp=sharing)

[vídeo do ytb explicando](https://www.youtube.com/watch?v=RZFIhTT7bKM&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=10)

# Projeto 12 (Raiz Quadrada)
Este é o último circuito aritmético da disciplina e, curiosamente, funciona de maneira muito parecida com a Divisão. Se você entendeu o Divisor, a Raiz Quadrada vai ser tranquila!

A lógica que usamos aqui é um algoritmo conhecido como "Restoring Square Root" (Raiz Quadrada com Restauração).

Como funciona a lógica:A ideia é descobrir a raiz bit por bit, do mais significativo para o menos significativo.
Agrupamento: Pegamos o número de entrada e o dividimos em pares de bits, começando da esquerda (MSB).

Adivinhação: Para cada par que "baixamos", tentamos subtrair um valor de teste.

O Valor de Teste: Se a raiz que encontramos até agora é P, o valor que tentamos subtrair do resto atual é formado por $P$ seguido de $01$ (em binário, isso equivale a 4P + 1).

Decisão:Se a subtração for possível (resultado positivo), o bit da raiz é 1 e atualizamos o resto.
Se a subtração não for possível (resultado negativo), o bit da raiz é 0 e mantemos o resto anterior.

[link do projeto 12](https://drive.google.com/file/d/1QdtektYE5kkRdwIs_NKU_x3D5RKJbHUY/view?usp=sharing)

[vídeo do ytb explicando](https://www.youtube.com/watch?v=9qRPtWJ4ONw&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=11)

# Projeto 13 (Comparador)
A base de um comparador é um subtrator de A-B, para o caso de todos os bits de saída sejam 0, o resutado será igual, B é maior que A caso seja negativo, se nenhum dos casos de aplicar A é maior que B
Para checar se todos são zero, basta fazer um nand de todas as saídas
Para checar se o número é negativo basta analizar o bit mais significativo

[link do projeto 13](https://drive.google.com/file/d/1udslxfRdyf20TxoykvsBkVIJv6hRpY6I/view?usp=sharing)

[vídeo do ytb explicando](https://www.youtube.com/watch?v=q-qf01VqWk8&list=PL400nT9WA9li9LjGXqFKlHqRZxryRAomV&index=12)
