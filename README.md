# Calculo-de-aldiencia-TV-codigo-Java

Considere o seguinte problema:

Foi feita uma pesquisa sobre a audiência de canal de TV em várias casas de uma cidade, em determinado dia. Para cada casa consultada foi fornecido o número do canal (4, 5, 7, 12) e o número de pessoas que estavam assistindo àquele canal. Se a televisão estivesse desligada, nada era anotado, ou seja, essa casa não entrava na pesquisa. Faça um programa que:

leia um número indeterminado de dados (número do canal e número de pessoas que estavam assistindo);
calcule e mostre a percentagem de audiência de cada canal.
Para encerrar a entrada de dados, digite o número do canal ZERO.

Complete o programa abaixo de forma que implemente corretamente o problema acima.



public class PesquisaAudiencia {
	public static void main(String[] args) {
		[int canal, cont = 1, canal4 = 0, canal5 = 0, canal7 = 0, canal12 = 0, totalPessoas = 0;]
		[do] {
			System.out.printf("------------------------ CASA %02d ------------------------\n", cont);
			[System.out.print("Canal que estavam assistindo (4, 5, 7 ou 12): ");]
			[canal = Integer.parseInt(System.console().readLine());]
			if(canal != 0) {
				System.out.print("Numero de pessoas assistindo o canal: ");
				int numPessoas = Integer.parseInt(System.console().readLine());
				[switch(canal)] {
					case 4: canal4 += numPessoas; break;
					case 5: canal5 += numPessoas; break;
					case 7: canal7 += numPessoas; break;
					case 12: canal12 += numPessoas; break;
				}
				cont++;
				[totalPessoas += numPessoas;]
			}
		} [while(canal != 0)];
		
		double percCanal4 = canal4 * 100.0 / totalPessoas;
		double percCanal5 = canal5 * 100.0 / totalPessoas;
		double percCanal7 = canal7 * 100.0 / totalPessoas;
		double percCanal12 = canal12 * 100.0 / totalPessoas;
		
		System.out.printf("\nPERCENTUAL DE AUDIENCIA DO CANAL 4 = %.1f%%\n", percCanal4);
		System.out.printf("\nPERCENTUAL DE AUDIENCIA DO CANAL 5 = %.1f%%\n", percCanal5);
		System.out.printf("\nPERCENTUAL DE AUDIENCIA DO CANAL 7 = %.1f%%\n", percCanal7);
		System.out.printf("\nPERCENTUAL DE AUDIENCIA DO CANAL 12 = %.1f%%\n", percCanal12);
	}
}
