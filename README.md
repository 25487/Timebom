# Timebom

Bonus B2:L6 TimeBomb 
Ookal was deze opdracht bonus, het leek ons leuk om hem te maken.
Bij deze opdracht heb ik samen gewerkt met Sohil. We kregen een beetje hulp van Joshua

CODE:

import java.util.Timer;
import java.util.TimerTask;

public class timebom {
   public static int beginTime = 10;
   public static void main(String[] args) {
       Timer timer = new Timer();

        System.out.println("Few Seconds Remaining!");
       timer.schedule(new TimerTask() {
           public void run() {

               if (beginTime == 0) {
                   System.out.println("Boom!");
                   System.out.println("GAMEOVER!");
                   timer.cancel();

               } else {
                   beginTime--;
                   System.out.println(beginTime);
               }
           }

       }, 100, 500);
   }
}
