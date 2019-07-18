# equals-hashCode
Implementation of equals and hashCode (Java)


public class Konto {

	private int ktoId;
	private double saldo;
	private Kunde kd;
	
	public Konto(){
		
	}
	
	public Konto(int ktoId, double saldo){
		this.ktoId = ktoId;
		this.saldo = saldo;
	}
	
	public void setKtoId(int ktoId){
		this.ktoId = ktoId;
	}
	
	public int getKtoId(){
		return ktoId;
	}
	
	public void setSaldo(double saldo){
		this.saldo = saldo;
	}
	
	public double getSaldo(){
		return saldo;
	}
	
	
	public void setKunde(Kunde kd){
		this.kd = kd;
	}
	
	public Kunde getKunde() {
		return kd;
	}
	
	public void add(double betrag){
		saldo += betrag;
	}
	
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (!(obj instanceof Konto))
			return false;
		final Konto other = (Konto) obj;
		if(ktoId != other.ktoId)
			return false;
		return true;
	}
	
	public int hashCode(){
		return ktoId;
	}
}
