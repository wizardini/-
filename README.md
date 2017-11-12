using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication3
{
    public class operations1
    {
        public void addSugar()
        {
            Console.WriteLine("введите количество сахара которое хотите добавить");
            int d = int.Parse(Console.ReadLine());
            Console.WriteLine("теперь в вашей чашке " + d + " ложек сахара");
        }

        public void Drink()
        {
            Console.WriteLine("Введите любое число для того чтобы выпить вашу чашку ");
            int c = int.Parse(Console.ReadLine());
            Wash();
        }
        public void Wash()
        {
            Console.WriteLine("После того как вы всё выпили, теперь необходимо помыть чашку ");
            Console.WriteLine("Ваша чашка вымыта");
            Console.WriteLine("");
        }

    }

   
    public class CupofTea : operations1
    {
        public CupofTea() { }
      
    }
    public class CupofCoffe : operations1
    {
        public CupofCoffe() { }
  
    }



    class Program
    {
        static void Main()
        {
            for (; ; )
            {
                Console.WriteLine("Вы хотите чай или кофе ");
                int SWG1 = int.Parse(Console.ReadLine());
                CupofCoffe coff = new CupofCoffe();
                CupofTea tea = new CupofTea();
                switch (SWG1)
                {
                    case 1:
                        Console.WriteLine("Выберите чай, который вы хотите ");
                        Console.WriteLine("1 - Черный ");
                        Console.WriteLine("2 - Зеленыый ");
                        Console.WriteLine("3 - Красный ");
                        int SWG2 = int.Parse(Console.ReadLine());
                      
                        switch (SWG2)
                        {
                            case 1:
                                Console.WriteLine("Черный ");
                                tea.addSugar();
                                tea.Drink();
                                break;
                            case 2:
                                Console.WriteLine("Зеленыый ");
                                tea.addSugar();
                                tea.Drink();
                                break;
                            case 3:
                                Console.WriteLine("Красный ");
                                tea.addSugar();
                                tea.Drink();
                                break;
                        }
                        break;
                    case 2:
                        Console.WriteLine("Выберите кофе ");
                        Console.WriteLine("1 - Черный молотый(растворимый) ");
                        Console.WriteLine("2 - Черный молотый(не растворимый) ");
                        int SWG3 = int.Parse(Console.ReadLine());
                        switch (SWG3)
                        {
                            case 1:
                                Console.WriteLine("Черный молотый(растворимый) ");
                                coff.addSugar();
                                coff.Drink();
                                break;
                            case 2:
                                Console.WriteLine("Черный молотый(не растворимый) ");
                                coff.addSugar();
                                coff.Drink();
                                break;
                        }
                        break;
                }
            }
        }
    }
}
