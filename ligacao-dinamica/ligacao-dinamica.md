

~~~~java
public class Funcionario
{
	protected String matricula;
	protected String nome;
	protected double salario;
	private Endereco endereco;
	
	public void receberSalario()
	{
		salario = 1000;
	}
	
	public void receberSalario(double salarioFuncionario, String nomeFuncionario)
	{
		salario = salarioFuncionario;
		nome = nomeFuncionario;
	}
	
	public String getNome()
	{
		return nome;
	}
	
	public double getSalario()
	{
		return salario;
	}
}
~~~~~


Já a classe Vendendor será implementada da seguinte forma:



~~~~java
public class Vendedor extends Funcionario
{
	double comissao;
	
	public void receberSalario()
	{
		salario = salario + comissao;
	}
	
	public Vendedor(double salarioVendedor, double comissaoFuncionario)
	{
		salario = salarioVendedor;
		comissao = comissaoFuncionario;
	}
}


~~~~
