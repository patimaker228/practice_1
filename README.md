//Задание 1. часть1.
sing System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Введите четыре числа:");

        // Ввод четырех чисел
        double num1 = Convert.ToDouble(Console.ReadLine());
        double num2 = Convert.ToDouble(Console.ReadLine());
        double num3 = Convert.ToDouble(Console.ReadLine());
        double num4 = Convert.ToDouble(Console.ReadLine());

        // Вычисление среднего значения
        double average = (num1 + num2 + num3 + num4) / 4;

        Console.WriteLine($"Среднее значение: {average}");
    }

}
//Задание 2.
using System;
class Calculator{
    static void Main()    {
        Console.WriteLine("Выберите действие:");        Console.WriteLine("1. Сложение");
        Console.WriteLine("2. Вычитание");        Console.WriteLine("3. Умножение");
        Console.WriteLine("4.Деление");        Console.WriteLine("5. Нахождение остатка");
        int choise = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("Введите первое число:");        double num1 = Convert.ToDouble(Console.ReadLine());
        Console.WriteLine("Введите второе число:");        double num2 = Convert.ToDouble(Console.ReadLine());
        double result = 0;
        switch (choise)        {
            case 1:
                result = num1 + num2;                break;
            case 2:                result = num1 - num2;
                break;            case 3:
                result = num1 * num2;                break;
            case 4:
                result = num1 / num2;                break;
            case 5:                result = num1 % num2;
                break;            default: Console.WriteLine("Неверный выбор действия.");
                break;        }
        Console.WriteLine("Результат:" + result);    }
}
//Задание 3.
using System;
using System.Timers;

namespace TemperatureConverter
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Введите значение температуры:");
            double temperature = Convert.ToDouble(Console.ReadLine());
            Console.WriteLine("Введите единицу температуры ( C для Цельсия, K для Кельвина, F для Фаренгейта):");
            char unit = Convert.ToChar(Console.ReadLine());
            if (unit == 'C')
            {
                Console.WriteLine($"Температура в Кельвинах:{temperature + 273.15}");
                Console.WriteLine($"Температура в Фаренгейтах:{temperature * 9 / 5 + 32}");
            }
            else if (unit == 'K')
            {

                Console.WriteLine($"Температура в Цельсиях:{temperature - 273.15}");
                Console.WriteLine($"Температура в Фаренгейтах:{temperature * 9 / 5 - 459.67}");
            }
            else if (unit == 'F')

            {
                Console.WriteLine($"Температура в Цельсиях:{(temperature - 32) * 5 / 9}");
                Console.WriteLine($"Температура в Кельвинах:{(temperature + 459.67) * 5 / 9}");
            }
            else
            {
                Console.WriteLine("Неверная единицо измерения");

            }
        }
    }
}

           // Задание 4.
            using System;
namespace FileNameExtractor

{
    class Program
    {
        static void Main(string[] args)

        {
            Console.WriteLine("Введите путь к файлу:");
            string path = Console.ReadLine();
            string fileName = GetFileNameFromPath(path);
            Console.WriteLine($"Имя файла:{fileName}");
        }
        static string GetFileNameFromPath(string path)
        {
            string[] parts = path.Split('\\');
            string[] file = parts[parts.Length - 1].Split('.');
            return file[0] + "." + file[1];
        }
    }
}
        //Задание 5.
        using System;
namespace LongestWordlnSentence
{
    class Program
    {
        static void Main(string[] args)
        {
            //Ввод предложения
            Console.WriteLine("Введите предложение:");
            string sentence = Console.ReadLine();
            //Разделение предложения слова
            string[] words = sentence.Split('.');
            //Поиск самого длинного слова
            string longestWord = string.Empty;
            foreach (string word in words)
            {
                if (word.Length > longestWord.Length)
                {
                    longestWord = word;
                }
            }
            //Вывод самого длинного слова
            Console.WriteLine("Самое длинное слово в предложении:" + longestWord);
        }
    }
}

//Задание 6.
using System;
namespace LongestWordlnSentence
{
    class Program
    {
        static void Main(string[] args)
        {
            //Ввод предложения
            Console.WriteLine("Введите предложение:");
            string sentence = Console.ReadLine();
            //Разделение предложения слова
            string[] words = sentence.Split('.');
            //Поиск самого длинного слова
            string longestWord = string.Empty;
            foreach (string word in words)
            {
                if (word.Length > longestWord.Length)
                {
                    longestWord = word;
                }
            }
            //Вывод самого длинного слова
            Console.WriteLine("Самое длинное слово в предложении:" + longestWord);
        }
    }
}

//Задание 7.
using System;

class Program
{
    static void Main()
    {
        int[] numbers = new int[5];
        
        Console.WriteLine("Введите пять чисел:");
        
        for (int i = 0; i < numbers.Length; i++)
        {
            numbers[i] = Convert.ToInt32(Console.ReadLine());
        }
        
        int max = numbers[0];
        int min = numbers[0];
        
        for (int i = 1; i < numbers.Length; i++)
        {
            if (numbers[i] > max)
            {
                max = numbers[i];
            }
            
            if (numbers[i] < min)
            {
                min = numbers[i];
            }
        }
        
        Console.WriteLine("Максимальное число: " + max);
        Console.WriteLine("Минимальное число: " + min);
    }
}
//Задание 8.
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Введите количество уровней пирамиды:");
        int levels = Convert.ToInt32(Console.ReadLine());

        for (int i = 1; i <= levels; i++)
        {
            for (int j = 1; j <= levels - i; j++)
            {
                Console.Write(" ");
            }
            for (int k = 1; k <= 2 * i - 1; k++)
            {
                Console.Write(k);
            }
            Console.WriteLine();
        }

        Console.ReadLine();
    }
}
