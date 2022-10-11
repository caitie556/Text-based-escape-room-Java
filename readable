import java.util.*;
public class main
{    
    public static void main()
    {
        System.out.print('\u000C');
        String[] useritems = {"", "", "", "", "", "", "", ""};
        String[] full = {"Sword", "Steak", "Mug", "Soda Can", "Code", "Coin", "Bottle", "Shoe"};
                             //0      1       2       3          4        5       6        7
        String[] finished = {"Sword", "Empty", "Mug", "Soda Can", "Code", "Coin", "Bottle", "Shoe"};
        
        ArrayList<String> words = new ArrayList<String>();
        words.add("left"); // 0
        words.add("right"); // 1
        words.add("up"); // 2
        words.add("down"); // 3
        words.add("punch"); // 4
        words.add("look");// 5
        words.add("help");// 6
        words.add("love");// 7
        words.add("beautiful");// 8
        words.add("hello");// 9
        words.add("hi");// 10
        words.add("weather");// 11
        words.add("map");// 12
        words.add("name");// 13
        words.add("take");// 14
        words.add("break");// 15
        words.add("yes");// 16
        words.add("no");// 17
        words.add("inventory");// 18
        words.add("quit"); //19
        
        System.out.println("ESCAPE ROOM");
        Scanner input = new Scanner(System.in);
        System.out.println("Enter username:");
        System.out.print(">");
        String username = input.nextLine();
        boolean jabberwordy = false;
        
        
        int s = 0;
        int pos = 4;
        roommap(pos);
        descrip(pos, useritems);
        String user;
        
        while (s == 0)
        {
                if (pos == 4 && (Arrays.equals(useritems, finished)))
                {
                    End();
                    s++;
                }
                System.out.print(">");
                user = input.nextLine();
                if (pos == 4 && (!(Arrays.equals(useritems, finished))))
                {
                    String jab = user;
                    jabberwordy = true;
                    if (jabberwordy = true)     
                    {
                        jabberwordy = jabberwordy(jab);
                    }
                } 
                 if ((user.toLowerCase()).contains(words.get(0)) && pos != 0 && pos != 3 && pos != 6) //left
                {
                    pos--;
                    roommap(pos);
                    descrip(pos, useritems);
                }
                else if ((user.toLowerCase()).contains(words.get(1)) && pos != 2 && pos != 5 && pos != 8) //right
                {
                    pos++;
                    roommap(pos);
                    descrip(pos, useritems);
                }
                else if (((user.toLowerCase()).contains(words.get(2))) && pos != 0 && pos != 1 && pos != 2) //up
                {
                    pos -= 3;
                    roommap(pos);
                    descrip(pos, useritems);
                }
                else if (((user.toLowerCase()).contains(words.get(3)) && pos != 6 && pos != 7 && pos != 8)) //down
                {
                    pos += 3;
                    roommap(pos);
                    descrip(pos, useritems);
                }
                else if ((user.toLowerCase()).contains(words.get(5))) //look
                {
                    descrip(pos, useritems);
                }
                else if ((user).contains(words.get(6))) //help
                {
                    System.out.print("You can use: ");
                    for (String a : words)
                    {
                        System.out.println(a);
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(7))) //love
                {
                    love();
                }
                else if ((user.toLowerCase()).contains(words.get(8))) //beautiful
                {
                    beauty();
                }
                else if ((user.toLowerCase()).contains(words.get(9)) || (user).equals(words.get(10))) //hi/hello
                {
                    hello(username);
                }
                else if ((user.toLowerCase()).contains(words.get(11))) //weather
                {
                    weather();
                }
                else if ((user.toLowerCase()).contains(words.get(12))) //map
                {
                    roommap(pos);
                }
                else if ((user.toLowerCase()).contains(words.get(13))) //name
                {
                    Name(username);
                }
                else if ((user.toLowerCase()).contains(words.get(14))) //take
                {
                    if (pos == 0 && (!(useritems[0]).equals(full[0])) )
                    {
                        System.out.println("You have taken: Sword");
                        useritems[0] = full[0];
                    }
                    else if (pos == 8 && (!(useritems[7]).equals(full[7])) )
                    {
                        System.out.println("You have taken: Shoe");
                        useritems[7] = full[7];
                    }
                    else
                    {
                        System.out.println("That action was ineffective.");
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(15))) //break
                {
                    if (pos == 3 && (useritems[0].equals(full[0])) )
                    {
                        System.out.println("The glass was successfully broken, and you grab the Soda Can.");
                        useritems[3] = full[3];
                    }
                    else if (pos == 3 && (!(useritems[0].equals(full[0])) ))
                    {
                        System.out.println("Android: You have to find something that will break the glass");
                    }
                    else
                    {
                        System.out.println("That action was ineffective.");
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(16))) //yes
                {
                    if (pos == 2 && (!(useritems[2]).equals(full[2])) )
                    {
                        System.out.println("You take the mug and pour the coffee out in the sink.");
                        useritems[2] = full[2];
                    }
                    else if (pos == 5 && (!(useritems[4]).equals(full[4])) )
                    {
                        useritems = RPS(useritems, input);
                    }
                    else if (pos == 6 && (!(useritems[5]).equals(full[5])) )
                    {
                        useritems = Cointoss(useritems, input);
                        if( (!(useritems[5]).equals(full[5])))
                        {
                            System.out.println("Would you like to try again?");
                        }
                    }
                    else if (pos == 7 && (!(useritems[1]).equals(full[1])) ) //dont have steak
                    {
                        System.out.println("Nice try.");
                    }
                    else if (pos == 7 && ((useritems[1]).equals(finished[1])) ) //empty
                    {
                        System.out.println("That was a good steak.");
                    }
                    else if (pos == 7 && ((useritems[1]).equals(full[1])) ) //do have steak
                    {
                        System.out.println("The lion grabs the steak and slides the bottle over to you.");
                        System.out.println("You recieved: Bottle");
                        useritems[6] = full[6];
                        useritems[1] = finished[1];
                    }
                    else if (pos == 1 && (!(useritems[1]).equals(full[1])) ) 
                    {
                        useritems = Tests(useritems, input);
                    }
                    else
                    {
                        random();
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(17))) //no
                {
                    if (pos == 2 && (!(useritems[2]).equals(full[2])) )
                    {
                        System.out.println("\"OK. If you want it later it will still be here.\"");
                    }
                    else if (pos == 1 || pos == 5 || pos == 6) 
                    {
                        System.out.println("Ok, remember to come back later.");
                    }
                    else if (pos == 7)
                    {
                        System.out.println("Complete the quiz then come back.");
                    }
                    else
                    {
                        random();
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(18))) //inventory
                {
                    for (String a : useritems)
                    {
                        System.out.println(a);
                    }
                }
                else if ((user.toLowerCase()).contains(words.get(19)))
                {
                    input.close();
                }
                else if (jabberwordy = false) // random
                {
                    random();
                }
        }
        System.out.println("Thanks for Playing!");
     }
            


    public static String[] Tests(String[] useritems, Scanner ans)
    {
        String userans;
        int q = 1;
        if (q == 1)
        {
            System.out.println("QUESTION 1: What is 144 x 68?");
            System.out.println("(Type stop to stop test)");
            System.out.print(">");
            userans = ans.nextLine();
            if ((userans).equals("9792"))
            {
               System.out.println("Great Job!");
               q++;
            }
            else if ((userans.toLowerCase()).equals("stop"))
            {
                q = 6;
            }
            else
            {
                System.out.println("Ummm, that wasn't quite correct, try again");
                
            }
            
        }
         if (q == 2)
        {
            System.out.println("QUESTION 2: What is 1,272 % 12?");
            System.out.println("(Type stop to stop test)");
            System.out.print(">");
            userans = ans.nextLine();
            if ((userans).equals("0"))
            {
                System.out.println("Congratulations! You answered that question correctly!");
                q++;
            }
            else if ((userans.toLowerCase()).equals("stop"))
            {
                q = 6;
            }
            else
            {
                System.out.println("Nope. Try again.");
                
            }
        }
         if (q == 3)
        {
            System.out.println("QUESTION 3: What is 6^3?");
            System.out.println("(Type stop to stop test)");
            System.out.print(">");
            userans = ans.nextLine();
            if ((userans).equals("216"))
            {
                System.out.println("Next Question, it is!");
                q++;
            }
            else if ((userans.toLowerCase()).equals("stop"))
            {
                q = 6;
            }
            else
            {
                System.out.println("Think a little harder.");
            }
        }
         if (q == 4)
        {
            System.out.println("QUESTION 4: Solve for x --> 24x = 72");
            System.out.println("(Type stop to stop test)");
            System.out.print(">");
            userans = ans.nextLine();
            if ((userans).equals("3"))
            {
                System.out.println("That was CORRECT!");
                q++;
            }
            else if ((userans.toLowerCase()).equals("stop"))
            {
                q = 6;
            }
            else
            {
                System.out.println("You'll get it next time!!!");
            }
        }
         if (q == 5)
        {
            System.out.println("QUESTION 5: What is √169?");
            System.out.println("(Type stop to stop test)");
            System.out.print(">");
            userans = ans.nextLine();
            if ((userans).equals("13"))
            {
                System.out.println("Congrats!!! You have earned this Steak.");
                useritems[1] = "Steak";
                q++;
            }
            else if ((userans.toLowerCase()).equals("stop"))
            {
                q = 6;
            }
            else 
            {
                System.out.println("Try one more time.");
            }
        }  
        
        return useritems;
    }
    
    public static String[] RPS(String[] useritems, Scanner answ)
    {
        String[] RPS = {"rock", "paper", "scissors"};
        System.out.println("You can throw: rock, paper, or scissors.");
        
        Random rand = new Random();
        int r = rand.nextInt(3) + 0;
        
        String bot = RPS[r];
        System.out.print(">");
        String u = answ.nextLine();
        for (int win = 0; win < 3; win += 0)
        {
            if ((u.toLowerCase()).equals(RPS[r]))
            {
                System.out.println("Game Android threw " + RPS[r]);
                System.out.println("It's a tie, lets go again");
                
            }
            else if ((u.toLowerCase()).equals(RPS[0]) && r == 2)
            {
                System.out.println("Game Android threw " + RPS[r]);
                win++;
                System.out.println("You won that round. " + (3 - win) + " more to go!");
                
            }
            else if ((u.toLowerCase()).equals(RPS[1]) && r == 0)
            {
                System.out.println("Game Android threw " + RPS[r]);
                win++;
                System.out.println("You won that round. " + (3 - win) + " more to go!");
                
            }
            else if ((u.toLowerCase()).equals(RPS[2]) && r == 1)
            {
                System.out.println("Game Android threw " + RPS[r]);
                win++;
                System.out.println("You won that round. " + (3 - win) + " more to go!");
                
            }
            else
            {
                System.out.println("Game Android threw " + RPS[r]);
                System.out.println("Better luck next round!!" + (3 - win) + " more to go!");
                
            }
            r = rand.nextInt(3) + 0;
            bot = RPS[r];
            System.out.print(">");
            u = answ.nextLine();
        }
        System.out.println("You finally won, heres that code I promised you.");
        useritems[4] = "Code";
        return useritems;
    }
    
    public static String[] Cointoss(String[] useritems, Scanner ans)
    {
        String[] coin = {"heads","tails"};
        System.out.println("You may choose heads or tails");
        Random random = new Random();
        int num = random.nextInt(2);    
        String b = coin[num];
        System.out.print(">");
        String u = ans.nextLine();
        if ((u.toLowerCase()).equals(b))
        {
            System.out.println("Congratulations! Here is your coin!");
            useritems[5] = "Coin";
        }
        else
        {
            System.out.println("That was not your luckiest guess, try again.");
        }
        return useritems;
    }
    
    public static boolean jabberwordy(String user)
        {
            ArrayList<String> commonWords = new ArrayList<String>();
            commonWords.add("above");
            commonWords.add("across");
            commonWords.add("add");
            commonWords.add("adventure");
            commonWords.add("also");
            commonWords.add("are");
            commonWords.add("bad");
            commonWords.add("because");
            commonWords.add("below");
            commonWords.add("but");
            commonWords.add("by");
            commonWords.add("can");
            commonWords.add("crazy");
            commonWords.add("day");
            commonWords.add("direction");
            commonWords.add("for");
            commonWords.add("from");
            commonWords.add("funny");
            commonWords.add("go");
            commonWords.add("good");
            commonWords.add("have");
            commonWords.add("how");
            commonWords.add("if");
            commonWords.add("java");
            commonWords.add("just");
            commonWords.add("keep");
            commonWords.add("most");
            commonWords.add("move");
            commonWords.add("need");
            commonWords.add("no");
            commonWords.add("other");
            commonWords.add("people");
            commonWords.add("program");
            commonWords.add("same");
            commonWords.add("some");
            commonWords.add("speak");
            commonWords.add("speech");
            commonWords.add("strange");
            commonWords.add("subtract");
            commonWords.add("talk");
            commonWords.add("text");
            commonWords.add("them");
            commonWords.add("then");
            commonWords.add("there");
            commonWords.add("they");
            commonWords.add("think");
            commonWords.add("this");
            commonWords.add("way");
            commonWords.add("what");
            commonWords.add("where");
            commonWords.add("who");
            commonWords.add("why");
            commonWords.add("with");
            commonWords.add("word");
            commonWords.add("yes");
            commonWords.add("you");
            ArrayList<String> jabberWords = new ArrayList<String>();
            jabberWords.add("allocution");
            jabberWords.add("ancient");
            jabberWords.add("antidisestablishmentarianiasm");
            jabberWords.add("autonomy");
            jabberWords.add("ballerina");
            jabberWords.add("banana");
            jabberWords.add("bankroll");
            jabberWords.add("berserker");
            jabberWords.add("birthplace");
            jabberWords.add("blathering");
            jabberWords.add("blister");
            jabberWords.add("bouncy");
            jabberWords.add("boutique");
            jabberWords.add("candelabra");
            jabberWords.add("cannibal");
            jabberWords.add("capacitor");
            jabberWords.add("catalyst");
            jabberWords.add("chandelier");
            jabberWords.add("chauffer");
            jabberWords.add("circuit");
            jabberWords.add("conundrum");
            jabberWords.add("craven");
            jabberWords.add("creepy");
            jabberWords.add("crustaceous");
            jabberWords.add("dance");
            jabberWords.add("dangerous");
            jabberWords.add("daring");
            jabberWords.add("dastardly");
            jabberWords.add("delude");
            jabberWords.add("download");
            jabberWords.add("dragon");
            jabberWords.add("ego");
            jabberWords.add("emphysema");
            jabberWords.add("ephemeral");
            jabberWords.add("etui");
            jabberWords.add("evaluate");
            jabberWords.add("feudal");
            jabberWords.add("fiery");
            jabberWords.add("flabbergasted");
            jabberWords.add("flux");
            jabberWords.add("forsooth");
            jabberWords.add("frothing");
            jabberWords.add("fudgesickle");
            jabberWords.add("funky");
            jabberWords.add("galloping");
            jabberWords.add("ghostly");
            jabberWords.add("glassy");
            jabberWords.add("gold");
            jabberWords.add("gooseneck");
            jabberWords.add("grizzly");
            jabberWords.add("grok");
            jabberWords.add("grommet");
            jabberWords.add("hashing");
            jabberWords.add("hibernation");
            jabberWords.add("Hogwarts");
            jabberWords.add("impure");
            jabberWords.add("incandescent");
            jabberWords.add("incubus");
            jabberWords.add("jump");
            jabberWords.add("limerick");
            jabberWords.add("melodrama");
            jabberWords.add("monger");
            jabberWords.add("monotone");
            jabberWords.add("muscle");
            jabberWords.add("obelisk");
            jabberWords.add("omnivore");
            jabberWords.add("ostensibly");
            jabberWords.add("pantaloons");
            jabberWords.add("papaya");
            jabberWords.add("parasite");
            jabberWords.add("patronus");
            jabberWords.add("pectoral");
            jabberWords.add("plebian");
            jabberWords.add("portcullis");
            jabberWords.add("punch");
            jabberWords.add("reagent");
            jabberWords.add("referee");
            jabberWords.add("salamander");
            jabberWords.add("savage");
            jabberWords.add("scalawag");
            jabberWords.add("serendipitous");
            jabberWords.add("seventeen");
            jabberWords.add("shameful");
            jabberWords.add("shanty");
            jabberWords.add("slither");
            jabberWords.add("sonic");
            jabberWords.add("spaceship");
            jabberWords.add("spongey");
            jabberWords.add("square");
            jabberWords.add("succubus");
            jabberWords.add("tango");
            jabberWords.add("tape");
            jabberWords.add("toaster");
            jabberWords.add("toothy");
            jabberWords.add("twine");
            jabberWords.add("volcano");
            
            for (String c : commonWords)
            {
                Random rand = new Random();
                int index = rand.nextInt(jabberWords.size() - 1);
                String randomWord = jabberWords.get(index);
                while (user.contains(c) )
                {
                    user = user.replace(c, randomWord);
                }
                
            }
            System.out.println(user);
            return false;
        }

    public static void random()
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("Cannot Compute....");
        }
        else if (x == 1)
        {
            System.out.println("I dont understand");
        }
        else if (x == 2)
        {
            System.out.println("Thats nice.");
        }
        else if (x == 3)
        {
            System.out.println("Nice meeting you.");
        }
        else if (x == 4)
        {
            System.out.println("If you escape bring me with you..");
        }
        else if (x == 5)
        {
            System.out.println("I've been in this escape room for several months.");
        }
        else if (x == 6)
        {
            System.out.println("That was quite random.");
        }
        else if (x == 7)
        {
            System.out.println("I heard Cook Bot doesn't actually cook any food.");
        }
        else if (x == 8)
        {
            System.out.println("Unfortunately I cannot move.");
        }
        else if (x == 9)
        {
            System.out.println("Are you enjoying the experiment so far?");
        }
    }
    
    
    public static void love()
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("I am an android. I love nothing.");
        }
        else if (x == 1)
        {
            System.out.println("I have no emotions");
        }
        else if (x == 2)
        {
            System.out.println("The definition of love is: an intense feeling of deep affection.");
        }
        else if (x == 3)
        {
            System.out.println("What do you mean?");
        }
        else if (x == 4)
        {
            System.out.println("I barely know you.....");
        }
        else if (x == 5)
        {
            System.out.println("What is love? Baby dont hurt me, dont hurt me, no more.");
        }
        else if (x == 6)
        {
            System.out.println("Whats love got to do with it?");
        }
        else if (x == 7)
        {
            System.out.println("My creator did not program me with the capacity to love.");
        }
        else if (x == 8)
        {
            System.out.println("Well, this is awkward...");
        }
        else if (x == 9)
        {
            System.out.println("Im flattered.");
        }
    }
    
    public static void beauty()
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("Yes, the game was created beautifully.");
        }
        else if (x == 1)
        {
            System.out.println("I am flattered.");
        }
        else if (x == 2)
        {
            System.out.println("I have no opinion of beauty.");
        }
        else if (x == 3)
        {
            System.out.println("Beauty is in the eye of the beholder");
        }
        else if (x == 4)
        {
            System.out.println("No comment.");
        }
        else if (x == 5)
        {
            System.out.println("B-E-A-U-T-I-F-U-L!");
        }
        else if (x == 6)
        {
            System.out.println("Roses are quite beautiful.");
        }
        else if (x == 7)
        {
            System.out.println("These metal walls are very shinny and beautiful.");
        }
        else if (x == 8)
        {
           System.out.println("I heard spring is the most beautiful time of year."); 
        }
        else if (x == 9)
        {
            System.out.println("I have very limited knowledge of beauty.");
        }
        
    }
    
    public static void hello(String name)
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("Hi!");
        }
        else if (x == 1)
        {
            System.out.println("Howdy!");
        }
        else if (x == 2)
        {
            System.out.println("Bonjour!");
        }
        else if (x == 3)
        {
            System.out.println("Hola!");
        }
        else if (x == 4)
        {
            System.out.println("Who are you?");
        }
        else if (x == 5)
        {
            System.out.println("You must be " + name + ". Nice to meet you!");
        }
        else if (x == 6)
        {
            System.out.println("This again? Move along.");
        }
        else if (x == 7)
        {
            System.out.println("There are so many people that I've said hi to today.");
        }
        else if (x == 8)
        {
            System.out.println("I could circle through all the languages I can speak to say hi but I would just be saying the same thing repeatedly, and thats annoying.");
        }
        else if (x == 9)
        {
            System.out.println("Im just going to ignore you.");
        }
    }
    
    public static void Name(String name)
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("A rose by any other name....");
        }
        else if (x == 1)
        {
            System.out.println("You're " + name + ", right?");
        }
        else if (x == 2)
        {
            System.out.println("Names are just labels given at birth.");
        }
        else if (x == 3)
        {
            System.out.println("Searching for: Name....no prevail.");
        }
        else if (x == 4)
        {
            System.out.println("A names a name.");
        }
        else if (x == 5)
        {
            System.out.println("My ID number is 52502.");
        }
        else if (x == 6)
        {
            System.out.println("My name was given by function.");
        }
        else if (x == 7)
        {
            System.out.println("It seems I've lost my name tag, although I never did have one.");
        }
        else if (x == 8)
        {
            System.out.println("I cant think of a name at the top of my head");
        }
        else if (x == 9)
        {
            System.out.println("Timmy!!! You're back!!");
        }
        
    }
    
    public static void weather()
    {
        int x;
        Random rand = new Random();
        x = rand.nextInt(10);
        
        if (x == 0)
        {
            System.out.println("The weather outside is frightful.");
        }
        else if (x == 1)
        {
            System.out.println("It's a name day today.");
        }
        else if (x == 2)
        {
            System.out.println("It's a bad day for the weather.");
        }
        else if (x == 3)
        {
            System.out.println("I cant tell the weather from inside these metal walls.");
        }
        else if (x == 4)
        {
            System.out.println("I haven't been outside since my creation.");
        }
        else if (x == 5)
        {
            System.out.println("I cannot feel the temperature.");
        }
        else if (x == 6)
        {
            System.out.println("Temperature sensors: Broken.");
        }
        else if (x == 7)
        {
            System.out.println("The forcast for this week include cold metal walls on monday, tuesday, wednesday, thursday, friday, saturday, and sunday.");
        }
        else if (x == 8)
        {
            System.out.println("We dont get alot of weather in this room.");
        }
        else if (x == 9)
        {
            System.out.println("I dont know what the weather is, maybe once you get outside you could come back and tell me.");
        }
        
    }

public static void descrip(int pos, String[] useritems) //describes each room
    {
        if (pos == 0)
        {
            if (useritems[0].equals("Sword"))
            {
               System.out.println("JUNK ROOM 1");
                System.out.println("You are in Junk Room 1, there are a lot of items on the floor, no valuble items catch you eye.");
                System.out.println("You notice the head of an android in the corner of the room.");
            }
            else
            {
                System.out.println("JUNK ROOM 1");
                System.out.println("You are in Junk Room 1, there are a lot of items on the floor, only one item catches your eye: a shinny sword");
                System.out.println("You notice the head of an android in the corner of the room.");
            }
        }
        else if (pos == 1)
        {  
            if ((useritems[1]).equals("Steak"))
            {
               System.out.println("TEST ROOM");
               System.out.println("You notice an android standing in front of a open metal cage containing nothing. The android starts speaking.");
                System.out.println("\"Congradulations for passing my test.\"");
            }
            else
            {
                System.out.println("TEST ROOM");
                System.out.println("You notice an android standing in front of a locked metal cage containing a steak. The android starts speaking.");
                System.out.println("\"Would you like to take the test now?\"");
            }
        }
        else if (pos == 2)
        {
            if (useritems[2].equals("Mug"))
            {
                System.out.println("KITCHEN");
                System.out.println("In front of you is an outdated kitchen from what looks like the 50's. There is an android at the sink facing away from you");
                System.out.println("The android turns from its position at the sink.");
                System.out.println("\"We are fresh out of coffee. My appologies\"");
            }
            else
            {
                System.out.println("KITCHEN");
                System.out.println("In front of you is an outdated kitchen from what looks like the 50's.");
                System.out.println("You are immediately greeted by an android wearing an old apron and holding a worn out coffee mug.");
                System.out.println("\"Would you like some coffee?\"");
            }
        }
        else if (pos == 3)
        {
            if ((useritems[3]).equals("Soda Can"))
            {
                System.out.println("CHALLENGE ROOM");
                System.out.println("The walls and ceiling of this room are white. Your attention is pulled to the middle of the room where a musem like podium stands, with");
                System.out.println("shattered glass on thefloor. Standing in the right corner behind the podium is an android.");
            }
            else
            {
                System.out.println("CHALLENGE ROOM");
                System.out.println("The walls and ceiling of this room are white. Your attention is pulled to the middle of the room where a musem like podium stands, displaying a");
                System.out.println("Soda Can being protected by glass. Standing in the right corner behind the podium is an android.");
            }
        }
        else if (pos == 4)
        {
            System.out.println("THE MYSTERIOUS WALL");
            System.out.println("There is a panel hanging off the wall with a shape of a glass bottle, a coin, a soda can, a mug,");
            System.out.println("a shoe, and a code.");
            System.out.println("There is also a hairy creature standing in one of the dark corners of this room.");
            System.out.println("He towers several feet over you.");
        }
        else if (pos == 5)
        {
            if ((useritems[4]).equals("Code"))
            {
                System.out.println("ROCK PAPER SCISSORS");
                System.out.println("There is an android standing behind the blackjack table in the middle of the room.");
                System.out.println("You notice a slot coming from his hand that printed the code. He starts talking");
                System.out.println("\"That was a fantastic game of rock paper scissors.\"");
            }
            else
            {
                System.out.println("ROCK PAPER SCISSORS");
                System.out.println("There is an android standing behind the blackjack table in the middle of the room.");
                System.out.println("You notice a slot coming from his hand that might be able to print the code. He starts talking");
                System.out.println("\"Would you like to play a game of rock paper scissors for the code?\"");
            }
        }
        else if (pos == 6)
        {
            if ((useritems[5]).equals("Coin"))
            {
                System.out.println("COIN TOSS");
                System.out.println("");
                System.out.println("You appear to be surrounded by white walls and a white ceiling. An android is standing in the middle of the empty room. He begins to talk");
                System.out.println("\"That was a wonderfull guess on your part. Congratulations\"");
            }
            else
            {
                System.out.println("COIN TOSS");
                System.out.println("You appear to be surrounded by white walls and a white ceiling. An android is standing in the middle of the empty room flipping a coin. He begins to talk");
                System.out.println("\"Would you like to play a quick game of coin toss?\"");
            }
        }
        else if (pos == 7)
        {
            if ((useritems[6]).equals("Bottle"))
            {
                System.out.println("THE HUNGRY TALKING LION");
                System.out.println("There is a tiger lying down eating a rw steak. He started snarling at you when you walked in.");
                System.out.println("\"Cant a tiger eat his steak in peace!?!\"");
            }
            else
            {
                System.out.println("THE HUNGRY TALKING LION");
                System.out.println("There is a tiger standing in front of a glass bottle. He started snarling at you when you walked in.");
                System.out.println("\"Do you have my steak?\"");
            }
        }
        else if (pos == 8)
        {  
            if ((useritems[7]).equals("Shoe"))
            {
                System.out.println("JUNK ROOM 2");
                System.out.println("The room is completely empty");
                System.out.println("You notice an android to your left, staring at you with beady red eyes. He says");
                System.out.println("\"Hello....\"");
            }
            else
            {
                System.out.println("JUNK ROOM 2");
                System.out.println("There is only one item in this room: a Shoe.");
                System.out.println("You notice an android to your left, staring at you with beady red eyes. He says");
                System.out.println("\"Hello....\"");
            }
        }
    }
    
    public static void printmap(String[][] map) //prints map based on position
    {
        for (int r = 0; r < map.length; r++)
        {
            for (int v = 0; v < map[r].length; v++)
            {
                System.out.print(map[r][v]);
            }
            System.out.println();
        }
    }
    
    public static void roommap(int pos) //corresponds posisition with map
    {
        if (pos == 0)
        {
            printmap(p0());
        }
        else if (pos == 1)
        {
            printmap(p1());
        }
        else if (pos == 2)
        {
            printmap(p2());
        }
        else if (pos == 3)
        {
            printmap(p3());
        }
        else if (pos == 4)
        {
            printmap(p4());
        }
        else if (pos == 5)
        {
            printmap(p5());
        }
        else if (pos == 6)
        {
            printmap(p6());
        }
        else if (pos == 7)
        {
            printmap(p7());
        }
        else if (pos == 8)
        {
            printmap(p8());
        }
        
    }
    
    public static String[][] p0() //room 0
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," ","x"," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p1() //room 1
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," ","x"," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p2() //room 2
    {
       String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," ","x"," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
       return map;
    }
    
    public static String[][] p3() //room 3
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," ","x"," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p4() //room 4
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," ","x"," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p5() //room 5
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," ","x"," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p6() //room 6
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," ","x"," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p7() //room 7
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," ","x"," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static String[][] p8() //room 8
    {
        String[][] map = {{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," "," "," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"},{"|"," "," "," ","|"," "," "," ","|"," ","x"," ","|"},{"+", "-", "-", "-", "+", "-", "-", "-","+", "-", "-", "-", "+"}};
        return map;
    }
    
    public static void End()
    {
        System.out.println("As you place the items into the wall compartments, you begin to feel the mechanics under the floor moving. The floor slowly rises as the roof opens to reveal a rainy sky.");
        System.out.println("Relieved, you look at the sky and close your eyes, relishing in the raindrops. Once the platform gets to the top you look around to find yourself in an open field with a small town far away.");
        System.out.println("You walk toward the town hoping to find help.");
    }
}
