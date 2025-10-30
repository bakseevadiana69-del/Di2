public int UserId { get; set; } 
    public string Username { get; set; } 
    public string DisplayName { get; set; } 
    public string Email { get; set; } 
    public DateTime RegistrationDate { get; set; } 
    public bool IsActive { get; set; } 

   
    public User(int userId, string username, string displayName, string email)
    {
        UserId = userId;
        Username = username;
        DisplayName = displayName;
        Email = email;
        RegistrationDate = DateTime.Now;
        IsActive = true;
    }
    public void DisplayUserInfo()
    {
    
        Console.WriteLine($"Имя пользователя: {Username}");
        Console.WriteLine($"Отображаемое имя: {DisplayName}");
        Console.WriteLine($"Email: {Email}");
       
    }
}
public class UtilityMethods
{
   
    public int AddNumbers(int num1, int num2)
    {
        Console.WriteLine($"Выполняется сложение: {num1} + {num2}");
        return num1 + num2;
    }
    public void DisplayGreeting(string userName)
    {
        string greetingMessage = (userName);
        Console.WriteLine(greetingMessage);
    }
}

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine(" Демонстрация методов и класса Пользователь ");

        UtilityMethods utils = new UtilityMethods();

        int sum = utils.AddNumbers(15, 25);
        Console.WriteLine($"Результат сложения: {sum}");
        Console.WriteLine(); 

        utils.DisplayGreeting("Алиса");
        Console.WriteLine(); 
        User user1 = new User(1, "alice_wonder", "Алиса Чудесная", "alice@gmail.com");
        User user2 = new User(2, "bob_builder", "Боб Строитель", "bobi@gmail.com");

        user1.DisplayUserInfo();
        user2.DisplayUserInfo();
        Console.WriteLine("\nНажмите любую клавишу для выхода...");
        Console.ReadKey();
    }
}
}
