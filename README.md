file Point.java
package OOP;

public class Poin {
	private int x,y;

	public int getX() {
		return x;
	}

	public void setX(int x) {
		this.x = x;
	}

	public int getY() {
		return y;
	}

	public void setY(int y) {
		this.y = y;
	}
	public Poin() {
		x=0;
		y=0;
	}
//	public Poin(int x,int y) {
//		this.x=x;
//		this.y=y;
//	}

	public Poin(int x, int y) {
		super();
		this.x = x;
		this.y = y;
	}
	public Poin(Poin p) {
		this.x=p.x;
		this.y=p.y;
	}
	public double Distance() {
		double d=Math.sqrt(Math.pow(y, 2) + Math.pow(y, 2));
		return d;
	}
	public double Distance(Poin q) {
		double d=Math.sqrt(Math.pow(x-q.x,2) + Math.pow(y-q.y, 2));
		return d;
	}
	public static double Distance(Poin p,Poin q) {
		double d=Math.sqrt(Math.pow(p.x-q.x,2) + Math.pow(p.y-q.y, 2));
		return d;
	}
	@Override
	public String toString() {
		// TODO Auto-generated method stub
		return String.format("(%d, %d)", x,y);
	}
	
}
file main.java
package project1;

import OOP.Poin;
public class Main {
	
	public static void main(String[] args){
//		float a = 3,b = -4,c =1;
//		int n=20;
//		basic.PTB2(a,b,c);
//		
//		long rs=basic.GT(n);
//		System.out.printf("%d!=%d\n",n,rs);
//		rs = basic.Fibo(n);
//		System.out.printf("Fibo(%d)=%d\n",n,rs);
//		for(int i=0;i<n;i++) {
//			if(basic.SoNguyenTo(i)) {
//				System.out.print(i+" ");
//			}
//		}
//		int k=29;
//		basic.LietKeSNT(k);
		OOP();
		
	}

	static void OOP() {
		// TODO Auto-generated method stub
		Poin p= new Poin();
		System.out.println("P" +p.toString());
		Poin p2= new Poin(5,10);
		System.out.println("P2" +p2.toString());
		Poin p3= new Poin(p2);
		System.out.println("P2" +p3.toString());
		double p2p=p2.Distance(p);
		double pp2=Poin.Distance(p, p2);
		System.out.printf("\n%f= %f",p2p,pp2);
	}
	static void Basic() {
		
	}
}

BTmang.java
package project1;

import java.util.Scanner;

public class BTMang {
	public static float[] Nhapmang() {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Nhập độ dài của mảng: ");
        int n = scanner.nextInt();
        float[] arr = new float[n];
        for (int i = 0; i < n; i++) {
            System.out.printf("Nhập phần tử thứ %d: ", i);
            arr[i] = scanner.nextFloat();
        }
        scanner.close();
        return arr;
    }

    public static void Xuatmang(float[] mang) {
        System.out.print("Các phần tử trong mảng: ");
        for (int i = 0; i < mang.length; i++) {
            System.out.print(mang[i] + " ");
        }
        System.out.println();
    }
    public static float TongMang(float mang[]) {
    	float tong = 0;
        for (int i = 0; i < mang.length; i++) {
            tong += mang[i];
        }
        return tong;
    }
    public static float[] MinMax(float mang[]) {
    	float min = mang[0];
    	float max = mang[0];
        for (int i = 1; i < mang.length; i++) {
            if (mang[i] < min) {
                min = mang[i];
            }
            if (mang[i] > max) {
                max = mang[i];
            }
        }

        // Tìm tất cả các vị trí có giá trị bằng giá trị nhỏ nhất
        int count = 0;
        int count1 = 0;
        for (int i = 0; i < mang.length; i++) {
            if (mang[i] == min) {
                count++;
            }
            if (mang[i] == max) {
                count1++;
            }
        }

        // Tạo một mảng mới chứa các vị trí có giá trị bằng giá trị nhỏ nhất
        float[] result = new float[count];
        float[] result1 = new float[count1];
        int index = 0;
        int index1 = 0;
        for (int i = 0; i < mang.length; i++) {
            if (mang[i] == min) {
                result[index++] = i;
            }
            if (mang[i] == max) {
                result1[index1++] = i;
            }
        }

        return result;
        	
    	
    }
    	
}
basic.java
package project1;

public class basic {
	
	static boolean SoNguyenTo(long n) {
		if(n<2)
			return false;
        for (long i = 2; i <= (int) Math.sqrt(n); i++) 
            if (n % i == 0) 
                return false;                 
        return true;
	}
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
circle.java
package OOP;

public class Circle {
	private String color;
	private double radius;
	
	public  Circle() {
		radius =1;
		color="red";
	}
	public  Circle(double r) {
		radius =r;
		color="red";
	}
	public double getRadius() {
		return radius;
	}
	public void setRadius(double radius) {
		this.radius = radius;
	}
	
}
employee.java
package OOP;

public class Employee {
	int id,sakary;
	String firstName,lastName;
	public Employee(int id, int sakary, String firstName, String lastName) {
		this.id = id;
		this.sakary = sakary;
		this.firstName = firstName;
		this.lastName = lastName;
	}
	
	
}
