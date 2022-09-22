using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.InteropServices.WindowsRuntime;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp2
{
    internal class Program
    {
        const double pi = 3.14159265359;

        static void Main(string[] args)
        {
           
            int num1 = 0;
            int num2 = 0;                      
            int n = 0;
            int siNo = 0;
            int radio = 0;
            char operando = 'a';
            string tipoOperacion = "0";
            bool tipo = false; 
            
            

            //EL BUCLE 

            do
            {
            
                Console.Clear();

                Cabezera();

                Console.WriteLine("Elije entre operacion basica(b) o operar Areas(a)");
                tipoOperacion = (Console.ReadLine());

                if (tipoOperacion == "b") tipo = true;

                if (tipoOperacion == "a") tipo = false;

                if (tipo == true)
                {
                    

                    Console.WriteLine("Introduzca el primer numero entero");

                    num1 = int.Parse(Console.ReadLine());

                    

                    Console.WriteLine("Introduzca el segundo numero entero");

                    num2 = int.Parse(Console.ReadLine());

                    

                    Console.WriteLine("Introduzca la operacion deseada ( + - * / % )");

                    operando = char.Parse(Console.ReadLine());

                    //LA CONDICION

                    if (operando == '+')
                        Console.WriteLine("El resultado de la suma es " + Suma(num1, num2));



                    else if (operando == '-')
                        Console.WriteLine("El resultado de la resta es " + Resta(num1, num2));



                    else if (operando == '*')
                        Console.WriteLine("El resultado de la multiplicacion es " + (num1 * num2));



                    else if (operando == '/')
                        Console.WriteLine("El resultado de la division es " + (num1 / num2));



                    else if (operando == '%')
                        Console.WriteLine("El resultado de el resto de la division es " + (num1 % num2));


                    else
                        Console.WriteLine("No has espedificado el operando");

                    

                }     
                
                else if (tipo == false)
                {

                    Console.WriteLine("Introduzca el radio del circulo para calcular su area");

                    radio = int.Parse(Console.ReadLine());

                    Console.WriteLine("El area es " + AreaCirculo(radio));                 

                                   

                }

                Console.WriteLine("Desea hacer otra operación (1) si / (0) no");

                siNo = int.Parse(Console.ReadLine());                

                if (siNo == 0)
                {         
                    
                    n++;
                    Console.Clear();

                }
                


            } while (n < 1);   
            
        }

        

        static void Cabezera()
        {
            Console.WriteLine("************************CALCULADORA**IKER***************************");
        }

        //LAS FUNCIONES

        static int Suma(int a, int b)
        {
            return (a + b);
        }

        static int Resta(int a, int b)
        {
            return (a + b);
        }

        static double AreaCirculo(int a)
        {
            return (a * a * pi);
        }

    }

}
