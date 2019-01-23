package c0708855;

import java.util.Random;

public class C0708855{

public static void main(String[] args) {
        jungle j1 = new jungle();
        j1.launch();
        System.out.println("Number of Lion winners is " + jungle.NumberOfLionWinners);
        System.out.println("Number of Tiger winners is " + jungle.NumberOfTigerWinners);
    }
}

// let's make a Super Class called FELINE
class Feline{
    public String name;
    public int Strength;

    public Feline(){
         Strength = SetStrength();
     }
    
    public int SetStrength(){
        Random rand = new Random(); 
        return rand.nextInt(10000);
    }
}
 class lion extends Feline{

 }  

class tiger extends Feline{
  public tiger(){
         
  }
     }
 
class jungle {
    // these are Class Instance Variables:
    // because they are declared at the Class Level
    // here is where the TYPE is defined
    public static int NumberOfLionWinners = 0;
    public static int NumberOfTigerWinners = 0;
    
     lion LION1;
     tiger TIGER1;
         
     public void launch(){
         // HERE is where the OBJECT IS CREATED
            LION1 = new lion();
            TIGER1 = new tiger();
            
            doCompetition(LION1, TIGER1);
            
     }
     
     public void doCompetition(Feline lion, Feline tiger){
            
         if (lion.Strength > tiger.Strength){
             jungle.NumberOfLionWinners++;
         } else
            {
             jungle.NumberOfTigerWinners++;
         } else
             {
               if(tiger.Strength == lion.Strength){  
                   {jungle.NumberOfDraws++;}}
         }
     }
}
