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

package banco;

public class conta 
{
	private int numero;
	
	private double saldo;
	
	public conta(int numero) 
	{
		this.numero = numero;
	}
	
	public conta(int numero, double saldo) 
	{
		this.numero = numero;
		this.saldo = saldo;
	}
	
	public void depositar(double valor) 
	{
		saldo += valor;
	}
	
	public void sacar(double valor) 
	{
		if (saldo >= valor)
			saldo -= valor;
		else
			System.out.println("Saldo insuficiente");
	}
	
	public int getNumero() 
	{
		return numero;
	}
	
	public double getSaldo() 
	{
		return saldo;
	}
}
