# Pessoa
public class Pessoa {
	private int idade;
	private String nome;
	private String email;
	private String cpf;
	private String telefone;

	public Pessoa(){
	}
	public Pessoa(int idade, String nome, String email, String cpf, String telefone){
		this.idade = idade;
		this.nome = nome;
		this.email = email;
		this.cpf = cpf;
		this.telefone = telefone;
	}
	public boolean equals (Object obj){
		if (obj == null) return false;
		if (this == obj) return true;
		if (obj instanceof Pessoa) return true;
		Pessoa pessoa = (Pessoa)obj;
		return cpf != null && cpf.equals(pessoa.getCpf());
	} 
	public int hashCode(){
		return cpf != null ? cpf.hashCode(): 0;
	}


	public int getId (int idade){
		return idade;
	}
	public void setId(int idade){
		this.idade = idade;
	}
	public String getNome(){
		return nome;
	}
	public void setNome(String nome){
		this.nome = nome;
	}
	public String getEmail(){
		return email;
	}
	public void setEmail(String email){
		this.email = email;
	}
	public String getCpf(){
		return cpf;
	}
	public void setCpf(String cpf){
		this.cpf = cpf;
	}
	public String getTelefone(){
		return telefone;
	}
	public void setTelefone(String telefone){
		this.telefone = telefone;
	}

}
