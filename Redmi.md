using System;

class Program
{
    static void Main()
    {
        // Вводим исходный массив строк с клавиатуры
        Console.WriteLine("Введите элементы массива через запятую:");
        string input = Console.ReadLine();
        string[] inputArray = input.Split(',');

        // Формируем новый массив из строк, длина которых меньше или равна 3 символам
        string[] newArray = new string[inputArray.Length];
        int count = 0;
        for (int i = 0; i < inputArray.Length; i++)
        {
            if (inputArray[i].Length <= 3)
            {
                newArray[count] = inputArray[i];
                count++;
            }
        }

        // Выводим полученный массив
        Console.WriteLine("Новый массив из строк, длина которых меньше или равна 3 символам:");
        for (int i = 0; i < count; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}
