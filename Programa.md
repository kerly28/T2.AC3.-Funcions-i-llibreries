using System;
//Pre: 
namespace MyProject
{
    public class Super4
    {
        public static int checkInput(int min,int  max,string message)
        {
            string ERROR_MSG = "Error. Formato incorrecto.";
            int a;
            bool isError = false;
            do
            {
                if (isError == false)
                {
                    Console.WriteLine(ERROR_MSG);
                }
                Console.WriteLine(message);
                a = Convert.ToInt32(Console.ReadLine());
                isError = true;

            } while (a > max || a < min);
            return a;
        }
        public static void Main()
        {
            string CHOOSE_AVATAR = "Escoge el avatar entre 1 i 4: ";
            string CHOOSE_EVIL = "Escoge la maldad del avatar entre 1000 i 5000: ";
            string CHOOSE_NAME = "Escoge el nombre de tu avatar: ";
            string ESPURNA_ATTACK = "Espurna ha atacado!";
            string ERROR_MSG = "Error. Formato incorrecto.";
            string[] arrayVowels = ["a", "e", "i", "o", "u"];
            int numUser, avatar, evil, power = 0, vowels = 0; /*i = 0, j = 0; Puesto como comentario */
            string nameAvatar;
            bool isError = false;//Esto no estaba

            avatar = checkInput(1, 4, CHOOSE_AVATAR);
            evil = checkInput(1000, 5000, CHOOSE_EVIL);
            do
            {
                if (isError == false)
                {
                    Console.WriteLine(ERROR_MSG);
                }
                Console.WriteLine(CHOOSE_NAME);
                nameAvatar = Convert.ToString(Console.ReadLine());
                isError = true;

            } while (nameAvatar.Length > 25 || nameAvatar.Length < 2);

            for (int i = 0; i < nameAvatar.Length; i++)
            {
                for (int j = 0; j < arrayVowels.Length; j++)
                {
                    if (nameAvatar[i] == arrayVowels[j])
                    {
                        vowels++;
                        if (vowels == 2)
                        {
                            i = nameAvatar.Length;
                        }
                    }
                }
            }
            Console.WriteLine(ESPURNA_ATTACK);
            if (vowels == 2)
            {
                power = power + evil / 4;
                evil = evil % 4;
            }    
            else
            {
                power = power + (evil * 5 / 100) / 4;
                evil = evil - (evil * 5 / 100);
            }
            Console.WriteLine("El poder de cada Super4 es" + power);
            Console.WriteLine("Al avatar le queda" + evil + "de maldad.");
        }
    }
}
//Post: 
