# dsa7
#infytq
#Password Generator
#java_code


import java.io.*;
import java.util.*;
public class Main
{
	public static void main(String[] args) {
		
		String str="Anchal:23581,Aman:57568,Sonakshi:34848,Ria:14585";
		ArrayList<String>name=new ArrayList<>();
		ArrayList<String>code=new ArrayList<>();
		String abc="";
		for(String s:str.split(","))
		{
		    String arr[]=s.split(":");
		    name.add(arr[0]);
		    code.add(arr[1]);
		}
		for(int i=0;i<name.size();i++)
		{
		    String a=name.get(i);
		    String b=code.get(i);
		    
		    int len=a.length();
		    int index=0;
		    for(String ans:b.split(""))
		    {
		        int x=Integer.parseInt(ans);
		        if(x<=len && x>index)
		        index=x;
		    }
		    if(index==0)
		    abc+="X";
		    else
		    abc+=a.charAt(index-1);
		    
		}
		System.out.println(abc);
	}
}
