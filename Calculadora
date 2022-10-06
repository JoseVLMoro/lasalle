#include <stdio.h>

/*Nome do usuario github:JoseVLMoro Este programa tenta fazer uma calculadora utilizando C, iniciamos colocando as variaveis em main, depois iniciamos um loop do...while para facilitar a realização de operações em sequência,*/
int main(void) {
  char formula;//para ler qual operação será realizada
  char palavras[20];//permite a utilização de fgets
  int count = 0;//para no caso de uma falha prevista o sistema pode reiniciar ou desligar
  int erro = 0;//variavel para não aparecer a opção de desligar em caso de erro
  float num1,num2 = 0;//primeiro número (se atribuir qualquer letra o sistema fica louco) //segundo número (se atribuir qualquer letra o sistema fica louco)
do{//o sistema foi feito em looping para facilitar o uso
  num1=0;//num1 e num2 são resetados para zero só para manter um padrão previsivel no caso do usuario cometer algum erro como colocar só 5^ neste caso ele retornará 5^0
  num2=0;
  formula='erro';// depois do primeiro loop sem resetar o valor de formula para erra possivel colocar valores invalidos
    erro = 0;//retorna erro a 0 caso tenha passado um loop no default
  printf("Calculadora de José Vicente Lobo Moro.\nCurso: Analise e desenvolvimento de sistema.\nUniversidade La Salle.\nMatricula: 201931577\nSinais utilizados:\n");//informações pedidas pelo professor da cadeira
  printf("/ = Dividir\n* = Multiplicar\n^ = Potenciação\nr = Raiz Quadrada\n+ = Somar\n- = Subtrair\nExemplo: 2+2, 2/4, 5r, 5.3-4.7, 5^2, etc\nEnvie o cálculo que deseja:");//informações de uso
  fgets(palavras,sizeof(palavras),stdin);// le uma string do usuario
  sscanf(palavras,"%f%*s",&num1);//le o primeiro numero da operação e ignora o resto salvando em num1
  sscanf(palavras,"%*f%c",&formula);//ignora o primeiro numero e salva o char que é apresentado na formula
  sscanf(palavras,"%*f%*c%f",&num2);//le o segundo numero da operação e ignora o resto salvando em num2
  switch(formula){
    case '^'://potência
      printf("Resultado da potência: %f\n\n", pow(num1,num2));
      break;
    case 'r'://raiz quadrada
      printf("Sua raiz quadrada é: %f\n\n", sqrt(num1)); 
      break;
    case '-'://subtração
      printf("Resultado da subtração: %f\n\n", num1-num2); 
      break;
    case '+'://soma
      printf("Resultado da soma: %f\n\n", num1+num2); 
      break;
    case '/'://divisão
      if(num2==0){
        printf("Não é possivel dividir por zero.\n\n");
      }else{
      printf("Resultado da divisão: %f\n\n", num1/num2); 
        }
      break;
    case '*'://multiplicação
      printf("Resultado da multiplicação: %f\n\n", num1*num2); 
      break;
        default://erros
      system("clear");
      printf("Opção invalida.\nApresente um cálculo suportado.\n");
      sleep(3);//pequeno delay para que o usuario possa ler a falha
      system("clear");//limpa o console para facilitar a leitura
      erro = 1;
      count = 0;// garante que se mantenha o loop
  }
  if(erro !=1){//se não ocorer erro perguntar se quer resetar a calculadora
  printf("Deseja iniciar um novo cálculo?\nEnviando o valor 0(ZERO) iniciará um novo cálculo\nQualquer outro valor desligará a calculadora\nO que deseja fazer?");
  scanf("%f", &count);//se for introduzido um char faz o sistema ler 0 e causa um erro onde o sistema pula diversos passos e vai para o default do switch
  getchar();//scanf cria um comando de trocar de linha que o fgets estava lendo, colocando getchar aqui resolve um problema que fazia fgets não permitir entrada do usuario
system("clear");//limpa o console
    }
}while(count<1);//mantem a calculadora rodando
  printf("Desligando...");
} 
