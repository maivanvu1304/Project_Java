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

public class Main {
	public static void main(String[] args){
		float a = 3,b = -4,c =1;
		int n=5;
		Basic.PTB2(a,b,c);
		
		long rs=Basic.GT(n);
		System.out.printf("%d!=%d\n",n,rs);
		rs = Basic.Fibo(n);
		System.out.printf("Fibo(%d)=%d\n",n,rs);
	}
}
Trường
Nguyễn Đăng Phước Trường
public class Basic {
	static void PTB2(float a,float b, float c){
		double delta = Math.pow(b,2) - 4*a*c;
		if (delta <0)
			System.out.println("Vô nghiệm");
		else if(delta ==0){
			double x=-b/2*a;
			System.out.println("Có nghiệm kép: "+x);
		}
		else{
			double x1= (-b-Math.sqrt(delta))/2*a;
			double x2= (-b+Math.sqrt(delta))/2*a;
			String s = String.format("Nghiệm của PT là: x1= %f,x2= %f",x1,x2);
			System.out.println(s);
		}
	}
	static long GT(long n){
			 long rs=1;
			 for(long i=1;i<=n;i++)
				 rs*=i;
			 return rs;
		}
	static long GT2(long n) {
		if(n==0)
			return 1;
		return n*GT2(n-1);
	}
	static long Fibo(long n){
			long F0 = 0, F1 = 1,F2 = 1;
			if(n==0)
				return 0;
			for(long i=2;i<=n;i++) {
				F2=F1+F0;
				F0=F1;
				F1=F2;
			}
			return F2;
		}
	}
