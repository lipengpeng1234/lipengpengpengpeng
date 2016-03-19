import java.io.*;
import java.util.Scanner;


public class Suiji {

	public static void main(String args[])
	{
		
		int y,o,p;int a,b,c,d;
		char  x[]={42,43,45,47};//定义+-*/
		char m[]={42,47};//*/
		char n[]={43,45};//+-
		int []arr={};
		
		Scanner scanner =new Scanner(System.in);
		System.out.print("请输入一个你想要的运算的个数：");
		int h1=scanner.nextInt();
		
		
		System.out.println("请输入运算的数的个数：");  //定义有多少个数运算
	    int  h=scanner.nextInt();   //运算式的个数
	System.out.println("请输入你的范围：");
	int j=scanner.nextInt();
	y=(int)(Math.random()*x.length+0);
	o=(int)(Math.random()*m.length+0);
	p=(int)(Math.random()*n.length+0);
	System.out.println("*************请选择你需要的功能***************");
	System.out.println("1:整数的加减运算,2:分数的加减运算,3:整数有负数，4：整数无负数");
	int L=scanner.nextInt();
	

	System.out.println("********************************");
	  //保证其不重复
	  for(int i=1;i<=h1;i++)
	  {
		  int z[]=new int [h1+1];
		  int v[]=new int [h1+1];
		  int r[]=new int [h1+1];
		  a=(int)(Math.random()*j+1);
		  b=(int)(Math.random()*j+1);
		  y=(int)(Math.random()*x.length+0);
		  z[i]=a;
		  v[i]=b;
		  r[i]=y;
		  for(int a1 =1;a1<i-1;a1++)
		  {
			  if(z[i]==z[a1]&&v[i]==v[a1]&&r[i]==r[a1])
			  {
				do
				{
					a=(int)(Math.random()*j+1);
					  b=(int)(Math.random()*j+1);
					
				}
				  while(z[i]==z[a1]&&v[i]==v[a1]&&r[i]==r[a1]);
			  
			  
			  }
			  }
			  
		  }
	  

	for(int i=0;i<h1;i++)
	{
	
		  a=(int)(Math.random()*j+1);
			b=(int)(Math.random()*j+1);
			c=(int)(Math.random()*j+1);
			d=(int)(Math.random()*j+1);
			
			p=(int)(Math.random()*n.length+0);
			
			  //分母不为零
			  if(b!=0){b++;}
			  if(d!=0){d++;}
			  //为最简式
			  for(int f=a;f>0;f--)
			  {  
				  if(a%f==0&&b%f==0)
				  {
				  a=a/f;
				  b=b/f;
				  }
			  }
			  for(int g=c;g>0;g--)
			  {  
				  if(c%g==0&&d%g==0)
				  {
				  c=c/g;
				  d=d/g;
				  }
			  }
		
				
	  switch(L)
			  {
	  case 1:
	  {
		  System.out.println("("+a+n[p]+c+")"+"=");
		  }
		  break;
	 
		  
		  
		  
		  
	  case 2:{
		  System.out.println("("+a+"/"+b+")"+n[p]+"("+b+"/"+d+")"+"=");
		  }
		  break;
		  
	  
		  
			  
	  
	  
	  
	  case 3:
	  {
		  System.out.println(a+"-"+c+"=");}
	  break;
		  
	  case 4:
		  if(a<c)
		  {
			  int temp;
			  temp=a;
			  a=c;
			  c=temp;
			  System.out.println(a+"-"+c+"=");
			  
			  
		  }break;
			  
	  
	  }
	 
	}
	  
	  
	  
	  
	  
		
	System.out.println("*************请选择你需要的功能***************");
	System.out.println("1:整数的乘除运算,2:分数的乘除运算，3：整数有余数，4：整数无余数"
			);
	int M =scanner.nextInt();

	System.out.println("********************************");
	
	
       for(int i=0;i<h1;i++)
       {			 a=(int)(Math.random()*j+1);
				b=(int)(Math.random()*j+1);
				c=(int)(Math.random()*j+1);
				d=(int)(Math.random()*j+1);
				
				p=(int)(Math.random()*n.length+0);
				  //分母不为零
				  if(b!=0){b++;}
				  if(d!=0){d++;}
				  //为最简式
				  for(int f=a;f>0;f--)
				  {  
					  if(a%f==0&&b%f==0)
					  {
					a=a/f;
					b=b/f;
					  }
				  }
				  for(int g=c;g>0;g--)
				  {  
					  if(c%g==0&&d%g==0)
					  {
		             c=c/g;
		             d=d/g;
					  }

				  
				  }
		switch(M)
		{
		case 1:
		{
			System.out.println("("+a+m[o]+c+")"+"=");
			}
			break;
			
		case 2:
			
			
		{
		
			System.out.println("("+a+"/"+b+")"+m[o]+"("+c+"/"+d+")"+"=");
			}
			break;
			
	
		case 3:
			{    if(a<b)
			{
				int temp;
				temp=a;
				a=b;
				b=temp;
			}
				System.out.println(a+"/"+b+"=");}
			break;
		case 4:
		{if(a%b==0)

			
			
		  
			  System.out.println(a+"/"+b+"=");
		  
		else{h1--;break;}
		
			
		
		
		}break;
		
		}
   
		
		try { FileOutputStream fos = new FileOutputStream("C:/a.txt");
		PrintStream stream = new PrintStream(fos); 
		stream.print("("+a+m[o]+c+")"+"="); 
		

	
	    }  catch(Exception e)
		{
	    	e.printStackTrace();
	    	
		} 
		}
       
	}

	
	}
	

	
		
		
		
        
	
	
	
	
	
	
	
	
	
	
	
	
	   
	   
	   
	   
	   
		
	
