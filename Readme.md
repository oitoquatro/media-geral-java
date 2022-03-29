import java.util.Scanner;

//Criar um programa que calcule a média geral de uma turma, de acordo com os seguintes requisitos:
//    a) Criar uma sub-rotina que preencha um vetor de números decimais, passado como argumento, utilizando entrada padrão (Scanner);
//    b) Criar uma sub-rotina chamada calcularMediaGeral() que:
//        ◦ receba um vetor preenchido de números decimais;
//        ◦ processe o somatório dos valores do vetor;
//        ◦ calcule a média geral com base no somatório e na quantidade de elementos do vetor;
//        ◦ e retorne o resultado do somatório.
//    c) O método principal (main) deverá: 
//        ◦ solicitar o tamanho da turma (quantidade de alunos);
//        ◦ criar um vetor de números decimais com o tamanho solicitado;
//        ◦ Em seguida, deverá efetuar o preenchimento das médias no vetor criado;
//        ◦ E por fim, deverá calcular a média geral e imprimir o resultado.

public class exercicios05 {

	public static void main(String[] args) {
		Scanner leitor = new Scanner(System.in);
		
		System.out.print("Didite a quantidade de elementos do vetor: ");
		int n = leitor.nextInt();
		
		double medias[] = new double[n];
		
		preencherVetor(medias);
		
		double mediaGeral = calcularMediaGeral(medias);
		
		System.out.printf("Média geral da turma: %.2f", mediaGeral);
		
		leitor.close();
	}
	
	public static void preencherVetor(double v[]) {
		Scanner leitor = new Scanner(System.in);
		
		for (int i = 0; i < v.length; i ++) {
			System.out.printf("v[%d] = ", i);
			v[i] = leitor.nextInt();		
					
			
		}
		
		leitor.close();
		
	}
	
private static double calcularMediaGeral(double[] medias) {
		
		double somatorio = 0;
		double mediaGeral;
		
		for (int i = 0; i < medias.length; i++) {
			somatorio += medias[i];
		}
		
		mediaGeral = somatorio / medias.length;
		
		return mediaGeral;
		
	}

}

