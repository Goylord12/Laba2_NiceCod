class Program
{
    static void Main(string[] args)
    {
        int[] arr = GetArray();

        Console.WriteLine("Выберите тип сортировки:\n1 - по возрастанию\n2 - по убыванию");
        int choice = int.Parse(Console.ReadLine());
        while (choice != 1 && choice != 2)
        {
            Console.WriteLine("Некорректный выбор! Попробуйте ещё раз:");
            choice = int.Parse(Console.ReadLine());
        }

        if (choice == 1)
        {
            InsertionSortAsc(arr);
            Console.WriteLine("Массив отсортирован по возрастанию:");
        }
        else
        {
            InsertionSortDesc(arr);
            Console.WriteLine("Массив отсортирован по убыванию:");
        }

        PrintArray(arr);
    }

    static int[] GetArray()
    {
        Console.WriteLine("Введите длину массива:");
        int n = int.Parse(Console.ReadLine());
        int[] arr = new int[n];

        Console.WriteLine($"Введите {n} элементов массива:");
        for (int i = 0; i < n; i++)
        {
            arr[i] = int.Parse(Console.ReadLine());
        }

        return arr;
    }

    static void InsertionSortAsc(int[] arr)
    {
        int n = arr.Length;
        for (int i = 1; i < n; ++i)
        {
            int key = arr[i];
            int j = i - 1;

            while (j >= 0 && arr[j] > key)
            {
                arr[j + 1] = arr[j];
                j = j - 1;
            }
            arr[j + 1] = key;
        }
    }

    static void InsertionSortDesc(int[] arr)
    {
        int n = arr.Length;
        for (int i = 1; i < n; ++i)
        {
            int key = arr[i];
            int j = i - 1;

            while (j >= 0 && arr[j] < key)
            {
                arr[j + 1] = arr[j];
                j = j - 1;
            }
            arr[j + 1] = key;
        }
    }

    static void PrintArray(int[] arr)
    {
        Console.WriteLine("Отсортированный массив:");
        for (int i = 0; i < arr.Length; i++)
        {
            Console.Write(arr[i] + " ");
        }
        Console.WriteLine();
    }
}