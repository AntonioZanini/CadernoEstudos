# Técnicas Digitais I - Teoria

## Aula 22/02/19

### Sistema Decimal

* É formado por potências de base 10.
* Possui 10 números.
* 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9.

#### Exemplo:

             Base 10
    3971(D)     ↓
    │││└─  1 x 10⁰ =      1
    ││└──  7 x 10¹ =     70
    │└───  9 x 10² =    900
    └────  3 x 10³ =   3000
                       ────
                       3971

### Sistema Binário

* É formado por potências de base 2.
* Possui 2 números.
* 0 e 1.

#### Exemplo:

             Base 2
    1010(B)     ↓
    │││└─   0 x 2⁰ = 0 x 1 =  0
    ││└──   1 x 2¹ = 1 x 2 =  2
    │└───   0 x 2² = 0 x 4 =  0
    └────   1 x 2³ = 1 x 8 =  8
                             ──
                             10

1010(B) = 10(D)

#### Exercício - Converta para decimal:

1. 0011(B) = ?(D)
1. 0101(B) = ?(D)
1. 1110(B) = ?(D)
1. 1111(B) = ?(D)

Resolução:

    8 4 2 1
    ───────
    0 0 1 1 =  3
    0 1 0 1 =  5
    1 1 1 0 = 14
    1 1 1 1 = 15

1. 0011(B) =  3(D)
1. 0101(B) =  5(D)
1. 1110(B) = 14(D)
1. 1111(B) = 15(D)

## Aula 01/03/19

* 17547(D) = ?(B)

Resolução


            
        17547│ 2
          1  └───
             8773 │ 2
               1  └───
                   4386 │ 2
                     0  └───
                         2193 | 2
                           1  └───
                               1096 | 2
                                 0  └───
                                     548 | 2
                                      0  └───
                                          274 | 2
                                           0  └───
                                               137 | 2
                                                1  └───
                                                    68 | 2 
                                                    0  └───
                                                        34 | 2 
                                                         0 └───
                                                            17 | 2
                                                            1  └───
                                                                8 | 2
                                                                0 └───
                                                                   4 | 2
                                                                   0 └───
                                                                      2 | 2
                                                                      0 └───
                                                                         1

Logo, 17547(D) = 100010010001011(B).

Outro método de resolução:

* Escreva valores de bits até chegar ao valor máximo que poderia ser contido no número em questão.
* Indo dos valores de bit maiores para os menores, caso o valor possa ser subtraído do número, assinale com 1 o bit, subtraia e passe para o próximo bit, caso contrário, assinale 0 e passe para o próximo bit.

#### Exemplo:

    4
    8 2 6 8 4
    3 9 9 4 2 2 6 8
    6 1 0 0 0 1 5 2 4 2 6
    1 8 4 2 1 5 2 1 6 3 1 8 4 2 1             17547
                                             -16384
    1 0 0 0 1 0 0 1 0 0 0 1 0 1 1             ─────
                                               1163
                                              -1024
                                              ─────
                                                139
                                               -128
                                              ─────
                                                 11
                                                 -8
                                              ─────
                                                  3
                                                 -2
                                              ─────
                                                  1
                                                 -1
                                              ─────
                                                  0


### Sistema Hexadecimal

* É formado por potências de base 16.
* Possui 16 números.
* 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E e F.

#### Exemplo 1:

    1 A 5 F (H)
    │ │ │ └─   15 x 16⁰ = 15 x    1 =   15
    │ │ └───    5 x 16¹ =  5 x   16 =   80
    │ └─────   10 x 16² = 10 x  256 = 2560
    └───────    1 x 16³ =  1 x 4096 = 4096 +
                                      ────
                                      6751 (D)

#### Exemplo 2:

    6
    9 6
    0 5 6
    4 2 1 1

    F 1 E 9 (H)

    (F x 4096) + (1 x 256) + (E x 16) + (9 x 1)
    (15 x 4096) + 256 + (14 x 16) + 9
    61440 + 256 + 224 + 9 = 61929 (D)

### Conversão de Número Decimal para Hexadecimal

Devemos fazer a mesma forma utilizada na conversão de decimal para binário, mas dividindo por 16.

#### Exemplo 1: 100(D) = ?(H)

    100 | 16
     96 └───
      4  6     ►  64

Logo, 100(D) = 64(H).

#### Exemplo 2: 31(D) = ?(H)

    31 | 16
    16 └───
    15  1     ►  1 15  ►  1F

Logo, 31(D) = 1F.

### Tabela de Valores das Bases 2, 10 e 16

|BIN | DEC |HEX|
|:--:|:---:|:-:|
|0000|  0  | 0 |
|0001|  1  | 1 |
|0010|  2  | 2 |
|0011|  3  | 3 |
|0100|  4  | 4 |
|0101|  5  | 5 |
|0110|  6  | 6 |
|0111|  7  | 7 |
|1000|  8  | 8 |
|1001|  9  | 9 |
|1010|  10 | A |
|1011|  11 | B |
|1100|  12 | C |
|1101|  13 | D |
|1110|  14 | E |
|1111|  15 | F |

### Exercícios

#### Converta para Decimal

1. 1234(H) = ?(D)
1. FACA(H) = ?(D)

Resolução:

    6
    9 6
    0 5 6
    4 2 1 1

    1 2 3 4  = 4096 + 512 + 48 + 4 = 4660

    F A C A  = 15x4096 + 2560 + 12x16 x 10 = 61440

1. 1234(H) = 4660(D)
1. FACA(H) = 61440(D)

#### Converta para Hexadecimal

1. 165(D) = ?(H)
1. 5673(D) = ?(H)

Resolução:

    165 | 16
      5 └───
         10   ►   10 5  ►  A5

    5673 | 16
       9 └───
          354 | 16
           2  └───
               22 | 16
                6 └───
                   1    ►  1629

1. 165(D) = A5(H)
1. 5673(D) = 1629(H)