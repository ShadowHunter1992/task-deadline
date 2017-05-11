using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp23
{
    public class task
    {
        public person person;
        public int CetinlikDerecesi;
        public int CetinliyeGoreDeadline;
        int[] integer = { 1, 2, 3, 4, 5 };
        string[] stringer = { "ConsoleApp-1", "ConsoleApp-2", "ConsoleApp-3", "ConsoleApp-4", "ConsoleApp-5" };


        public Dictionary<int, string> a = new Dictionary<int, string>();
        public task()
        {
           
            for (var i = 0; i < integer.Length; i++)
            {
                a.Add(integer[i], stringer[i]);

            }
            Console.WriteLine("Cetinlik Derecesine uygun taski secin ");
            foreach(KeyValuePair<int,string> item in a)
            {
                Console.WriteLine(item.Key.ToString());
            }
            CetinlikDerecesi = Convert.ToInt32(Console.ReadLine()) - 1;
            if(CetinlikDerecesi>0&& CetinlikDerecesi<6)
            {
                Console.WriteLine("sizin tapwiriqiniz" +a[a.Keys.ToList()[CetinlikDerecesi]]);
                Console.WriteLine("Cetinliye gore deadlineniz " + (CetinlikDerecesi+1)*2+" saatdir");
            }
            else
            {
                Console.WriteLine("zehmet olmasa 1-5 araliginda reqem daxil edin");
            }

           
            
        }
            
    }
   public  class person
    {
        public static int Deadline;
        
    }
    class Program
    {
       

        static void Main(string[] args)
        {
            var ad = new task();
            Console.ReadKey();
        }
    }
}
