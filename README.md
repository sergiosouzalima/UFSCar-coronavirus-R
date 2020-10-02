UFSCar-ACIEPE {.title .toc-ignore}
=============

### Análise e visualização de dados do coronavírus usando R. {.subtitle}

#### Sergio Lima {.author}

#### Sep 28, 2020 {.date}

Homework 01
-----------

* * * * *

#### 1) Faca algumas operacoes matemáticas com os operadores listados na aula 1.

-   Escolha pelo menos tres operadores distintos.
-   Faca tambem 3 combinacoes distintas entre os operadores.

``` {.r}
# Operadores Matemáticos
# Soma +
1 + 2
```

    ## [1] 3

``` {.r}
# Multiplicação *
2 * 3
```

    ## [1] 6

``` {.r}
# Resto da divisão %%
10 %% 3
```

    ## [1] 1

* * * * *

#### 2) Suponha que um pesquisador tenha criado o pacote chamado Brasil.

-   Que comando voce utilizaria para instalar tal pacote?

``` {.r}
# install.packages("Brasil")
```

-   Que comando voce utilizaria para carregar tal pacote?

``` {.r}
# library(Brasil)
```

-   Suponha que dentro deste pacote Brasil tenha a funcao SP.
-   Como voce acabou de instalar este pacote, ainda nao esta
    familiarizado com os termos desta nova funcao.
-   De que forma voce poderia descobrir como utilizar este comando
    dentro do R?

``` {.r}
# help("Brasil.SP") ### aparece um quadro explicativo ao lado direito do RStudio.
# Exemplo: help("print.default")
```

-   E fora do R? (Voce pode fazer uma pesquisa para responder essa
    questao).

``` {.r}
# https://www.rdocumentation.org/
```

* * * * *

#### 3) Como e’ possıvel criar um chunk de codigo no R markdown?

``` {.r}
# ```{r}
#   codigo R aqui 
# ```
```

-   Quais as opcoes para usar knit? (Faca uma pesquisa para responder
    essa questao,
-   ou use o card Rmarkdown disponibilizado no AVA - Moodle).

``` {.r}
# INLINE CODE
# O resultado aparece como texto sem o codigo R.
# Exemplo:
#   Versao do R `r getRversion()` ==> Versao do R 3.6.1
```

Versao do R 3.6.1

``` {.r}
# CODE CHUNKS
# Uma ou mais linhas cercadas por ```{r} e ```
# Exemplo:
#   ```{r echo=TRUE}
#      Versao do R getRversion() ==> Versao do R 3.6.1
#   ```
```

Versao do R

    ## [1] '3.6.1'

``` {.r}
## GLOBAL OPTIONS
# Atribuir knitr::opts_chunk$set()
# Exemplo:
# ```{r include=FALSE} 
#   knitr::opts_chunk$set(echo = TRUE)
# ```
```

* * * * *

#### 4) Teste qual a diferenca entre criar um vetor usando a funcao c() e c(””).

``` {.r}
# Cria um vetor com cinco elementos numericos:
c(1,4,6,8,10)
```

    ## [1]  1  4  6  8 10

``` {.r}
# Cria um vetor com cinco elementos tipo caracter:
c("1","4","6","8","10")
```

    ## [1] "1"  "4"  "6"  "8"  "10"

* * * * *

#### 5) Crie um vetor de todos numeros inteiros maiores do que 1 e menores do que 1000.

``` {.r}
c(2:999)
```

    ##   [1]   2   3   4   5   6   7   8   9  10  11  12  13  14  15  16  17  18  19
    ##  [19]  20  21  22  23  24  25  26  27  28  29  30  31  32  33  34  35  36  37
    ##  [37]  38  39  40  41  42  43  44  45  46  47  48  49  50  51  52  53  54  55
    ##  [55]  56  57  58  59  60  61  62  63  64  65  66  67  68  69  70  71  72  73
    ##  [73]  74  75  76  77  78  79  80  81  82  83  84  85  86  87  88  89  90  91
    ##  [91]  92  93  94  95  96  97  98  99 100 101 102 103 104 105 106 107 108 109
    ## [109] 110 111 112 113 114 115 116 117 118 119 120 121 122 123 124 125 126 127
    ## [127] 128 129 130 131 132 133 134 135 136 137 138 139 140 141 142 143 144 145
    ## [145] 146 147 148 149 150 151 152 153 154 155 156 157 158 159 160 161 162 163
    ## [163] 164 165 166 167 168 169 170 171 172 173 174 175 176 177 178 179 180 181
    ## [181] 182 183 184 185 186 187 188 189 190 191 192 193 194 195 196 197 198 199
    ## [199] 200 201 202 203 204 205 206 207 208 209 210 211 212 213 214 215 216 217
    ## [217] 218 219 220 221 222 223 224 225 226 227 228 229 230 231 232 233 234 235
    ## [235] 236 237 238 239 240 241 242 243 244 245 246 247 248 249 250 251 252 253
    ## [253] 254 255 256 257 258 259 260 261 262 263 264 265 266 267 268 269 270 271
    ## [271] 272 273 274 275 276 277 278 279 280 281 282 283 284 285 286 287 288 289
    ## [289] 290 291 292 293 294 295 296 297 298 299 300 301 302 303 304 305 306 307
    ## [307] 308 309 310 311 312 313 314 315 316 317 318 319 320 321 322 323 324 325
    ## [325] 326 327 328 329 330 331 332 333 334 335 336 337 338 339 340 341 342 343
    ## [343] 344 345 346 347 348 349 350 351 352 353 354 355 356 357 358 359 360 361
    ## [361] 362 363 364 365 366 367 368 369 370 371 372 373 374 375 376 377 378 379
    ## [379] 380 381 382 383 384 385 386 387 388 389 390 391 392 393 394 395 396 397
    ## [397] 398 399 400 401 402 403 404 405 406 407 408 409 410 411 412 413 414 415
    ## [415] 416 417 418 419 420 421 422 423 424 425 426 427 428 429 430 431 432 433
    ## [433] 434 435 436 437 438 439 440 441 442 443 444 445 446 447 448 449 450 451
    ## [451] 452 453 454 455 456 457 458 459 460 461 462 463 464 465 466 467 468 469
    ## [469] 470 471 472 473 474 475 476 477 478 479 480 481 482 483 484 485 486 487
    ## [487] 488 489 490 491 492 493 494 495 496 497 498 499 500 501 502 503 504 505
    ## [505] 506 507 508 509 510 511 512 513 514 515 516 517 518 519 520 521 522 523
    ## [523] 524 525 526 527 528 529 530 531 532 533 534 535 536 537 538 539 540 541
    ## [541] 542 543 544 545 546 547 548 549 550 551 552 553 554 555 556 557 558 559
    ## [559] 560 561 562 563 564 565 566 567 568 569 570 571 572 573 574 575 576 577
    ## [577] 578 579 580 581 582 583 584 585 586 587 588 589 590 591 592 593 594 595
    ## [595] 596 597 598 599 600 601 602 603 604 605 606 607 608 609 610 611 612 613
    ## [613] 614 615 616 617 618 619 620 621 622 623 624 625 626 627 628 629 630 631
    ## [631] 632 633 634 635 636 637 638 639 640 641 642 643 644 645 646 647 648 649
    ## [649] 650 651 652 653 654 655 656 657 658 659 660 661 662 663 664 665 666 667
    ## [667] 668 669 670 671 672 673 674 675 676 677 678 679 680 681 682 683 684 685
    ## [685] 686 687 688 689 690 691 692 693 694 695 696 697 698 699 700 701 702 703
    ## [703] 704 705 706 707 708 709 710 711 712 713 714 715 716 717 718 719 720 721
    ## [721] 722 723 724 725 726 727 728 729 730 731 732 733 734 735 736 737 738 739
    ## [739] 740 741 742 743 744 745 746 747 748 749 750 751 752 753 754 755 756 757
    ## [757] 758 759 760 761 762 763 764 765 766 767 768 769 770 771 772 773 774 775
    ## [775] 776 777 778 779 780 781 782 783 784 785 786 787 788 789 790 791 792 793
    ## [793] 794 795 796 797 798 799 800 801 802 803 804 805 806 807 808 809 810 811
    ## [811] 812 813 814 815 816 817 818 819 820 821 822 823 824 825 826 827 828 829
    ## [829] 830 831 832 833 834 835 836 837 838 839 840 841 842 843 844 845 846 847
    ## [847] 848 849 850 851 852 853 854 855 856 857 858 859 860 861 862 863 864 865
    ## [865] 866 867 868 869 870 871 872 873 874 875 876 877 878 879 880 881 882 883
    ## [883] 884 885 886 887 888 889 890 891 892 893 894 895 896 897 898 899 900 901
    ## [901] 902 903 904 905 906 907 908 909 910 911 912 913 914 915 916 917 918 919
    ## [919] 920 921 922 923 924 925 926 927 928 929 930 931 932 933 934 935 936 937
    ## [937] 938 939 940 941 942 943 944 945 946 947 948 949 950 951 952 953 954 955
    ## [955] 956 957 958 959 960 961 962 963 964 965 966 967 968 969 970 971 972 973
    ## [973] 974 975 976 977 978 979 980 981 982 983 984 985 986 987 988 989 990 991
    ## [991] 992 993 994 995 996 997 998 999

-   Em seguida, crie um vetor com as mesmas caracterısticas, contendo
    apenas numeros pares.
-   Dica: obviamente nao espero que voce digite elemento por elemento.

``` {.r}
seq(from=2, to=999, by=2)
```

    ##   [1]   2   4   6   8  10  12  14  16  18  20  22  24  26  28  30  32  34  36
    ##  [19]  38  40  42  44  46  48  50  52  54  56  58  60  62  64  66  68  70  72
    ##  [37]  74  76  78  80  82  84  86  88  90  92  94  96  98 100 102 104 106 108
    ##  [55] 110 112 114 116 118 120 122 124 126 128 130 132 134 136 138 140 142 144
    ##  [73] 146 148 150 152 154 156 158 160 162 164 166 168 170 172 174 176 178 180
    ##  [91] 182 184 186 188 190 192 194 196 198 200 202 204 206 208 210 212 214 216
    ## [109] 218 220 222 224 226 228 230 232 234 236 238 240 242 244 246 248 250 252
    ## [127] 254 256 258 260 262 264 266 268 270 272 274 276 278 280 282 284 286 288
    ## [145] 290 292 294 296 298 300 302 304 306 308 310 312 314 316 318 320 322 324
    ## [163] 326 328 330 332 334 336 338 340 342 344 346 348 350 352 354 356 358 360
    ## [181] 362 364 366 368 370 372 374 376 378 380 382 384 386 388 390 392 394 396
    ## [199] 398 400 402 404 406 408 410 412 414 416 418 420 422 424 426 428 430 432
    ## [217] 434 436 438 440 442 444 446 448 450 452 454 456 458 460 462 464 466 468
    ## [235] 470 472 474 476 478 480 482 484 486 488 490 492 494 496 498 500 502 504
    ## [253] 506 508 510 512 514 516 518 520 522 524 526 528 530 532 534 536 538 540
    ## [271] 542 544 546 548 550 552 554 556 558 560 562 564 566 568 570 572 574 576
    ## [289] 578 580 582 584 586 588 590 592 594 596 598 600 602 604 606 608 610 612
    ## [307] 614 616 618 620 622 624 626 628 630 632 634 636 638 640 642 644 646 648
    ## [325] 650 652 654 656 658 660 662 664 666 668 670 672 674 676 678 680 682 684
    ## [343] 686 688 690 692 694 696 698 700 702 704 706 708 710 712 714 716 718 720
    ## [361] 722 724 726 728 730 732 734 736 738 740 742 744 746 748 750 752 754 756
    ## [379] 758 760 762 764 766 768 770 772 774 776 778 780 782 784 786 788 790 792
    ## [397] 794 796 798 800 802 804 806 808 810 812 814 816 818 820 822 824 826 828
    ## [415] 830 832 834 836 838 840 842 844 846 848 850 852 854 856 858 860 862 864
    ## [433] 866 868 870 872 874 876 878 880 882 884 886 888 890 892 894 896 898 900
    ## [451] 902 904 906 908 910 912 914 916 918 920 922 924 926 928 930 932 934 936
    ## [469] 938 940 942 944 946 948 950 952 954 956 958 960 962 964 966 968 970 972
    ## [487] 974 976 978 980 982 984 986 988 990 992 994 996 998

* * * * *

#### 6) Calcule o numero de ouro no R. Dica: o numero de ouro e’ dado pela expressao:

\\[ \\frac{ 1 + \\sqrt{5} } {2} \\]

``` {.r}
(1 + sqrt(5)) / 2
```

    ## [1] 1.618034

* * * * *

#### 7) Qual o resultado da divisao de 1 por 0 no R?

``` {.r}
1 / 0
```

    ## [1] Inf

-   E de -1 por 0?

``` {.r}
-1 / 0
```

    ## [1] -Inf

* * * * *

#### 8) Verifique quais as diferencas entre NaN, NULL, NA e Inf?

-   Digite expressoes que retornem cada um desses resultados.

``` {.r}
# fonte: https://www.curso-r.com/material/r-base/
# NA
# NA (Not Available) significa dado faltante/indisponível. É o null do SQL.
# ou seja, podemos ter NA numeric, NA character etc.
as.numeric (c("1", "2", "three", "4"))   # Illegal conversion
```

    ## Warning: NAs introduced by coercion

    ## [1]  1  2 NA  4

``` {.r}
# NaN
# NaN (Not a Number) representa indefinições matemáticas, como 0/0 e log(-1). 
# Um NaN é um NA, mas a recíproca não é verdadeira.
0 / 0
```

    ## [1] NaN

``` {.r}
# Inf
# Inf (Infinito) é um número muito grande ou o limite matemático, por exemplo, 
# 1/0 e 10^310. Aceita sinal negativo -Inf.
1/0
```

    ## [1] Inf

``` {.r}
# NULL
# NULL representa a ausência de informação. Conceitualmente, a diferença 
# entre NA e NULL é sutil, mas, no R, o NA está mais alinhado com os 
# conceitos de estatística (ou como gostaríamos que os dados faltantes se 
# comportassem em análise de dados) e o NULL está em sintonia com 
# comportamentos de lógica de programação.
f <- function() if(FALSE) 1
print(f())
```

    ## NULL

* * * * *

#### 9) Verifique o que retorna a expressao 5 + 3 \* 10 %/%3 == 15 retorna no R.

``` {.r}
5 + 3 * 10 %/%3 == 15
```

    ## [1] FALSE

-   Faca a expressao retornar o valor contrario apenas usando parenteses
-   ou seja, se a expressao retornar originariamente TRUE, faca retornar
    FALSE.

``` {.r}
5 + (3 * 10) %/%3 == 15
```

    ## [1] TRUE

-   Explique o que faz a expressao original 5 + 3 \* 10 %/%3.
-   1o.

``` {.r}
10 %/% 3
```

    ## [1] 3

-   2o.

``` {.r}
3 * 3
```

    ## [1] 9

-   3o.

``` {.r}
5 + 9
```

    ## [1] 14

* * * * *

#### 10) Escreva um loop que itere os numeros de 1 a 7 e imprima o cubo de cada numero, usando print().

``` {.r}
print((1:7)^3)
```

    ## [1]   1   8  27  64 125 216 343

* * * * *

#### 11) Verifique qual e’ seu atual diretorio de trabalho com o comando getwd().

-   Lembre-se que para mudar o diretorioo, voce deve usar setwd(”caminho
    da pasta escolhida”).

``` {.r}
getwd()
```

    ## [1] "/home/sergio/R"

* * * * *
