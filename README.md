# Fibonacci

1. Escriba un programa que reciba como entrada un número entero n, y entregue como salida el n-ésimo número de Fibonacci:

   ```c#
   bool loop = true;
   int number = 0;
   List<int> lista = new List<int>() { 0, 1 };
   int suma = 0;
   while (loop)
   {
   	try
   	{
   		Console.Clear();
   		Console.Write("Ingrese n: ");
   		number = int.Parse(Console.ReadLine());
   		if (number >= 0)
   		{
   			loop = false;
   		}
   		else
   		{
   			Console.Clear();
   			Console.Write("Error. . . ");
   			Console.ReadKey();
   		}
   	}
   	catch (Exception)
   	{
   		Console.Clear();
   		Console.Write("Error. . . ");
   		Console.ReadKey();
   	}
   }
   for (int j = 2; j <= number; j++)
   {
   	suma = lista[j - 1] + lista[j - 2];
   	lista.Add(suma);
   }
   Console.WriteLine($"F{number} = {lista[number]}");
   Console.Write("\nPress Enter To continue. . .");
   Console.ReadKey();
   ```

2. Escriba un programa que reciba como entrada un número entero e indique si es o no un número de Fibonacci:

   ```c#
   bool loop1 = true;
   int number1 = 0;
   List<int> lista1 = new List<int>() { 0, 1 };
   int suma1 = 0;
   while (loop1)
   {
   	try
   	{
   		Console.Clear();
   		Console.Write("Ingrese un numero: ");
   		number1 = int.Parse(Console.ReadLine());
   		if (number1 >= 0)
   		{
   			loop1 = false;
   		}
   		else
   		{
   			Console.Clear();
   			Console.Write("Error. . . ");
   			Console.ReadKey();
   		}
   	}
   	catch (Exception)
   	{
   			Console.Clear();
   			Console.Write("Error. . . ");
   			Console.ReadKey();
   	}
   }
   for (int j = 2; j <= number1; j++)
   {
   	suma1 = lista1[j - 1] + lista1[j - 2];
   	lista1.Add(suma1);
   }
   if (lista1.Contains(number1))
   {
   	Console.WriteLine($"{number1} es numero de Fibonacci");
   	Console.Write("\nPress Enter To continue. . .");
   	Console.ReadKey();
   }
   else 
   {
   	Console.WriteLine($"{number1} no es numero de Fibonacci");
   	Console.Write("\nPress Enter To continue. . .");
   	Console.ReadKey();
   }
   ```

3. Escriba un programa que muestres los m primeros números de Fibonacci, donde m es un número ingresado por el usuario:

   ```c#
   bool loop3 = true;
   int number3 = 0;
   List<int> lista3 = new List<int>() { 0, 1 };
   int suma3 = 0;
   while (loop3)
   {
   	try
   	{
   		Console.Clear();
   		Console.Write("Number: ");
   		number3 = int.Parse(Console.ReadLine());
   		if (number3 >= 0)
   		{
   			loop3 = false;
   		}
   		else
   		{
   			Console.Clear();
   			Console.Write("Error. . . ");
   			Console.ReadKey();
   		}
   	}
   	catch (Exception)
   	{
   		Console.Clear();
   		Console.Write("Error. . . ");
   		Console.ReadKey();
   	}
   }
   for (int j = 2; j <= (number3 - 1); j++)
   {
   	suma3 = lista3[j - 1] + lista3[j - 2];
   	lista3.Add(suma3);
   }
   Console.WriteLine($"Los {number3} primeros numeros de Fibonacci son: ");
   foreach (int x in lista3)
   {
   	Console.Write($"{x} ");
   }
   Console.Write("\n\nPress Enter To continue. . .");
   Console.ReadKey();
   ```