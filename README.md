# Comandos-Break-e-Continue-no-java

Anotações dos Comandos Break e Continue no java

                                                                   Comandos Break e Continue

Agenda

.Comandos break e continue
.rótulos

                                                                         Comando Break

.Usado para saída de loops.
.Pode ser usado juntamente com um rótulo (label)

Sair de loop

int num = 100;

for (int i=0; i<num; i++){
    if (i*i >= num){
       break;
    }
    system.out.println("Valor de i: " + i);
}

Exemplo com break

Ex1:

package com.madu.Break.e.Continue;

import java.util.Scanner;

public class BreakContinue {

	public static void main(String[] args) {
		
		Scanner scan = new Scanner(System.in);
		
		System.out.println("Entre com um número");
		int num = scan.nextInt();
		
		System.out.println("Entre com um limite");
		int max = scan.nextInt();
		
		for (int i=num; i<=max; i++) {
			System.out.println(i);
			if (i % 7 == 0) {
				System.out.println("O valor de i é: " + i);
				break;
			}
		}
	}

}


Console:
Entre com um n?mero
8
Entre com um limite
30
8
9
10
11
12
13
14
O valor de i ?: 14


break com rótulos - gato

for (int i=0; i<4; i++){
     rotulo1:{
          rotolo2:{
              rotulo3:{
                  if (i == 1) break rotulo1;
                  if (i == 2) break rotulo2;
                  if (i == 3) break rotulo3;
                  System.out.println("rotulo3");
              }
              System.out.println("rotulo2");
          }
          System.out.println("rotulo1");
      }
      System.out.println("valor de i: " + i);
}
System.out.println("saiu do loop.");

A segunda utilização do break seria ccom leibholz next que seria com rótulos e muitas linguagens de programação o break com rótulos é conhecido como go to
o go to não é uma boa prática de programação você útilizar o go to.
Os rótulos são apenas uma identificação e eles estão apenas identificando ese bloco de código aqui como um rótulo.

Ex;

package com.madu.Break.e.Continue;

import java.util.Scanner;

public class BreakContinue {

	public static void main(String[] args) {
		
		for (int i=0; i<=4; i++) {
			rotulo1: {
				rotulo2: {
					rotulo3: {
						if (i == 1) {
							break rotulo1;
						}
						if (i == 2) {
							break rotulo2;
						}
						if (i == 3) {
							break rotulo3;
						}
						System.out.println("rotulo3");
					}
					System.out.println("rotulo2");
				}
				System.out.println("rotulo1");
			}
			System.out.println(i);
		}
		
	}

}


Console:

rotulo3
rotulo2
rotulo1
0
1
rotulo1
2
rotulo2
rotulo1
3
rotulo3
rotulo2
rotulo1
4


                                                                         Comando continue

.Complemento o break
.continue o loop na próxima iteração

