# Técnicas Digitais I - Prática

## Bases Numéricas

### Sistema Binário

* 0 e 1;

Formação Base 2:

    0111(B)
    │││└─  1 x 2⁰ =      1
    ││└──  1 x 2¹ =      2
    │└───  1 x 2² =      4
    └────  0 x 2³ =      0
                        ───
                         7

* 7(D) = 0111(B)
* 0101(B) = 5(D)

### Sistema Decimal

* 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9;

Formação Base 10:

    MCDU
    1238(D)
    │││└─  8 x 10⁰ =      8
    ││└──  3 x 10¹ =     30
    │└───  2 x 10² =    200
    └────  1 x 10³ =   1000
                       ────
                       1238

### Conversão de Decimal para Binário

* Divisões sucessivas

![images](https://user-images.githubusercontent.com/9437498/53417939-6782cd00-39b5-11e9-95ac-d17d64679494.png)

![conversao-decimal-binario](https://user-images.githubusercontent.com/9437498/53418064-b6c8fd80-39b5-11e9-9a4f-df0c7e1fe1e1.jpg)

* O **Resto** da primeira divisão é o **Dígito Menos Significativo**, podendo adicionar 0 ou 1 e definindo se o número é par ou impar;
* O **Quociente** da última divisão é o **Dígito Mais Significativo**, adicionando o dígito de maior valor do número;
* O número é construído a partir do último Quociente e todos os restos das divisões, sempre montando com os dígitos mais significativos à frete dos dígitos menos significativos;

Exemplo:

* 1238(D) = ?(B)

            │ 2
        1238└───
         0   619 │ 2 
         ↑    1  └───
         │        309 │ 2
         │         1  └───
         └ Dígito      154 │ 2
           Menos        0  └───
       Significativo        77 │ 2
                            1  └───
                                38 │ 2
                                0  └───
                                    19 │ 2 
                                    1  └───
                                        9 │ 2
                                        1 └───
                                           4 │ 2
                                           0 └───
                                              2 │ 2  
                                              0 └───
                                                1
                                                ↑
                                    Dígito Mais Significativo

Logo, 1238(D) = 10011010110(B).

Conferindo:

     1
     0  5  2  1
     2  1  5  2  6  3  1
     4  2  6  8  4  2  6  8  4  2  1
    2¹⁰ 2⁹ 2⁸ 2⁷ 2⁶ 2⁵ 2⁴ 2³ 2² 2¹ 2⁰
     1  0  0  1  1  0  1  0  1  1  0
     │  │  │  │  │  │  │  │  │  │  └─  0 x 2⁰  = 0 x    1 =     0
     │  │  │  │  │  │  │  │  │  └────  1 x 2¹  = 1 x    2 =     2
     │  │  │  │  │  │  │  │  └───────  1 x 2²  = 1 x    4 =     4
     │  │  │  │  │  │  │  └──────────  0 x 2³  = 0 x    8 =     0
     │  │  │  │  │  │  └─────────────  1 x 2⁴  = 1 x   16 =    16
     │  │  │  │  │  └────────────────  0 x 2⁵  = 0 x   32 =     0
     │  │  │  │  └───────────────────  1 x 2⁶  = 1 x   64 =    64
     │  │  │  └──────────────────────  1 x 2⁷  = 1 x  128 =   128 
     │  │  └─────────────────────────  0 x 2⁸  = 0 x  256 =     0
     │  └────────────────────────────  0 x 2⁹  = 0 x  512 =     0
     └───────────────────────────────  1 x 2¹⁰ = 1 x 1024 =  1024
                                                             ────
                                                             1238(D)

Logo, 10011010110(B) = 1238(D).

#### Transforme em Binário:

* 501(D) = ?(B)
* 78(D) = ?(B)
* 93(D) = ?(B)

Resolução:

    501 │ 2
     1  └───
         250 │ 2
          0  └───
              125 │ 2
               1  └───
                   62 │ 2
                   0  └───
                       31 │ 2
                       1  └───
                           15 │ 2
                           1  └───
                               7 │ 2
                               1 └───
                                  3 │ 2
                                  1 └───
                                     1

    78 │ 2
    0  └───
        39 │ 2
        1  └───
            19 │ 2
            1  └───
                9 │ 2
                1 └───
                   4 │ 2
                   0 └───
                      2 │ 2
                      0 └───
                         1

    93 │ 2
    1  └───
        46 │ 2
        0  └───
            23 │ 2
            1  └───
                11 │ 2
                1  └───
                    5 │ 2
                    1 └───
                       2 │ 2
                       0 └───
                          1

* 501(D) = 111110101(B)
* 78(D) = 1001110(B)
* 93(D) = 1011101(B)

#### Transforme em Decimal

* 10110(B) = ?(D)
* 1111(B) = ?(D)
* 1001(B) = ?(D)

Resolução:

      16  8  4  2  1

       1  0  1  1  0  = 22
          1  1  1  1  = 15
          1  0  0  1  =  9

* 10110(B) = 22(D)
* 1111(B) = 15(D)
* 1001(B) = 9(D)

### Sistema Hexadecimal

* 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E e F;
* A = 10, B = 11, C = 12, D = 13, E = 14, F = 15;

Formação Base 16:

    A 3 (H)
    │ └─   3 x 16⁰ =  3 x  1 =   3
    └───  10 x 16¹ = 10 x 16 = 160
                               ───
                               163 (D)

    B 1 A (H)
    │ │ └─   10 x 16⁰ = 10 x   1 =   10
    │ └───    1 x 16¹ =  1 x  16 =   16
    └─────   11 x 16² = 11 x 256 = 2816
                                   ────
                                   2842 (D)

    1 1 (H)
    │ └─   1 x 16⁰ = 1 x  1 =   1
    └───   1 x 16¹ = 1 x 16 =  16
                               ───
                               17 (D)

#### Conversão de Decimal para Hexadecimal

* Divisões sucessivas por 16, de forma semelhante a conversão de decimal para binário;

Exemplos:

A) 163(D) = ?(H)

      163 │ 16
       3  └───
           10=A

Logo, 163(D) = A3(H).

B) 529(D) = ?(H)

      529 │ 16
       1  └───
           33 │ 16
           1  └───
               2

Logo, 529(D) = 211(H).

C) 1000(D) = ?(H)

      1000 │ 16
        8  └───
            62 │ 16
            14 └───
                3

Sendo 14(D) = E(H), Logo 1000(D) = 3E8(H).