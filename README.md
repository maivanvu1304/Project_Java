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
	}//giải bằng đệ quy
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
	static long UCLN(long a,long b) {
		while (a!=b) {
			if (a>b)
				a=a-b;
			else
				b=b-a;
		}
		return a;
	}
	static long DQ_UCLN(long a,long b) {
		if(a==b)
			return a;
		else if(a>b)
			return DQ_UCLN(a-b,b);
		return DQ_UCLN(a,b-a);
	}//ước chung lớn nhất bằng đệ quy
	static long BCNN(long a,long b) {
		return a*b/BCNN(a,b);
	}
	static boolean SoNguyenTo(long n) {
		if(n<2)
			return false;
        for (long i = 2; i <= n; i++) 
            if (n % i == 0) 
                return false;                 
        return true;
	}
	static void LietKeSNT(long n) {
		String s= "";
		for(long i=2;i<n;i++)
			if(SoNguyenTo(i))
				s=s+i+" ";
		System.out.println(s);
	}
	static void LietKe_N_SNT(long n) {
		String s="";
		int dem =0;
		long i=2;
		while (dem!=n) {
			if(SoNguyenTo(i)) {
				s=s+i+" ";
				dem ++;
			}
			i++;
		}
		System.out.println(s);
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
