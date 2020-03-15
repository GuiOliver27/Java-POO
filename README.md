package banco;
public class banco 
{
	public static void main(String[] args)
	{
		conta c1 = new conta (1111);
		conta c2 = new conta (2222, 500);
		
		c1.depositar(1000);
		c1.sacar(100);
		System.out.println("Saldo c1: " + c1.getSaldo());
			c2.sacar(501);
	}
}
