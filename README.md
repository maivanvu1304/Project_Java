# Project_Java
public class main {
	public static void main(String[] args){
		float a = 5,b = 6,c =7;
		int n=5;
		Main.PTB2(a,b,c);
	
		Main m = new Main();
		m.GT(n);
		m.Fibo(n);
	}
	
	static void PTB2(float a,float b, float c){
		double denta = Math.pow(b,2) - 4*a*c;
		if (delta <0)
			System.out.println("Vô nghiệm");
		else if(delta ==0){
			double x=-b/2*a;
			System.out.println("Có nghiệm kép: "+x);
		}
		else{
			double x1= (-b-Math.sqrt(delta))/2*a;
			double x2= (-b+Math.sqrt(delta))/2*a;
			String s = String.format("Nghiệm của PT là: x1= %f,x2=%f",x1,x2);
			System.out.println(s);
		}
	}
	long GT(int n){
		return 0;
	}
	long Fibo(int n){
		return 0;
	}
}
