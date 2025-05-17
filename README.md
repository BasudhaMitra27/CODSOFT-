import java.util.scanner;
class range{
    public int genrate(int max, int min){
        return (int) (Math.random()*(max-min+1)+min);
    }
}

public class Number_Game{
     public static void main(string[] args){
     scanner s=new scanner(system.in);
     range rg=new range();
     int TA=0;
     int win=0;

     while(true){
         system.out.println(" Enter the minimum number:");
         int min=s.nextInt();
         system.out.println("Enter the maximum number:");
         int max=s.nextInt();
         s.nextLine();
         int c=rg.genrate(max,min);
         int A=0;

         while(true){
          system.out.println("Guess a number between "+min" and "+max);
          int g=s.nextInt();
          A++;

          if(g>c){
            system.out.println("Its Greater");
            }
          else if(g<c){
            system.out.println("Its lower");

              }
              else{
        system.out.println("correct guess");
        win++;
        break;
      }
    }
    TA=TA+A;
    system.out.println("Attempt="+A);
    system.out.println("wins="+win);

    double winrate=(double) win/TA*100;
    system.out.printf("your winrate is %.2f%%\n",winrate);
    system.out.println("Do you want to play again (y / n)");
    string PA=s.next();
    if(!PA.equalsIgnoreCase("y")){
      s.close();
      system.exit(0);

      }
    s.nextLine();
    }
  }
}
  
    
