import java.util.*;

public class Encrypt

{
	
	public static void main(String[] args)
  
  {
		
		Scanner input = new Scanner(System.in);
		char letters;
		int click;
		do
		{
			System.out.println("Enter 1 for encrypt character  or 2 for encrypt character number or 3 for exite");
			click = input.nextInt();

			switch(click)
			{
			case 1:
			 {
				System.out.println("Enter any word to encrypt ");
				String sentence = input.next();
				for (int i=0; i < sentence.length();i++ )
				{
					letters = sentence.charAt(i);
					int ascii = encrypt(letters);
					System.out.print((char)ascii);
				}
			 }
			 case 2:
			{
				System.out.println("Enter any word to encrypt ");
				String sentence = input.next();
				for (int i=0; i < sentence.length();i++ )
				{
					letters = sentence.charAt(i);
					int ascii = encrypt(letters);
					System.out.print(ascii);
				}	
			}
			 default:
			   {
				 System.exit(0);
			   }
			}
		}while(click!=3);
	}
	public static int encrypt(int i) 
	{
		return (char)(i + 1) ;
	}

}
