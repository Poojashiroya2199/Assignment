# Assignment

Decision solutions:-

Problem 1:
Input: [1,5,11,13,8,20]
Output: -18

Solution:-
Used IDE link:- https://my.newtonschool.co/playground/code/zpsogvprkb/

import java.io.*;
import java.util.*;

class Main{
    public static void findDiff(int[] arr, int arrlen){
        int evensum=0;
        int oddsum=0;
        int diff=0;
        for(int i=0;i<arrlen;i++){
          if(i%2==0){
                evensum+=arr[i];
            }
            else{
                oddsum+=arr[i];
            }
        }
        
        diff=evensum-oddsum;
        System.out.println(diff);
    }
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        int evensum=0;
        int oddsum=0;
        int diff=0;
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        findDiff(arr,n);
    }
}


Problem 2:-
String : “Sequence”
Output: S-1
 q-1
 u-1
 n-1
 c-1
 e-3
Solution:-

Used IDE link: - https://my.newtonschool.co/playground/code/75utspjvgh/
import java.io.*;
import java.util.*;
import java.util.Map.Entry;
class Main{
     public static LinkedHashMap<Character, Integer> sortbyvalue(LinkedHashMap<Character, Integer> hm) 
    { 
 List<Map.Entry<Character, Integer> > list = new LinkedList<Map.Entry<Character, Integer> >hm.entrySet()); 
        Collections.sort(list, new Comparator<Map.Entry<Character, Integer> >() { 
            public int compare(Map.Entry<Character, Integer> a,  
                               Map.Entry<Character, Integer> b) 
            { 
                return (a.getValue()).compareTo(b.getValue()); 
            } 
        }); 
        LinkedHashMap<Character, Integer> temp = new LinkedHashMap<Character, Integer>(); 
        for (Map.Entry<Character, Integer> map1 : list) { 
            temp.put(map1.getKey(), map1.getValue()); 
        } 
        return temp; 
    } 
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        String string=sc.next();

        LinkedHashMap<Character,Integer>map=new LinkedHashMap<>();
        for(int i=0;i<string.length();i++){
            char curr=string.charAt(i);
            map.put(curr,map.getOrDefault(curr,0)+1);      
  }
     
   LinkedHashMap<Character,Integer>ans=sortbyvalue(map);
        for(Entry<Character,Integer>entry:ans.entrySet()){
            System.out.println(entry.getKey()+"-"+entry.getValue());
        }  
  } 
 }
//This solution:gives the ans with frequency in sorted order using LinkedHashMap.

Other solution:
Used IDE link:- https://my.newtonschool.co/playground/code/tq0dcmcn8g/
import java.io.*;
import java.util.*;

class Main{
    public static void main(String args[]){
        String str = "Sequence";  
        int[] freq = new int[str.length()];  
        int i, j;  
        char string[] = str.toCharArray();  
          
        for(i = 0; i <str.length(); i++) {  
            freq[i] = 1;  
            for(j = i+1; j <str.length(); j++) {  
                if(string[i] == string[j]) {  
                    freq[i]++;  
                    string[j] = '0';  
                }  
            }  
        }  
        for(i = 0; i <freq.length; i++) {  
            if(string[i] != ' ' && string[i] != '0')  
                System.out.println(string[i] + "-" + freq[i]);  
        }  
    }  
}

But this solution prints only the characters frequency not in sorted order.


Problem 3:-find minimum number of rats to identify poisoned bottles.
Input :4
Output:2

Solution:-
Used IDE link:-https://my.newtonschool.co/playground/code/2cmwab4lh5/
import java.io.*;
import java.util.*;

class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int ans=(int)(Math.round(Math.log(n)/Math.log(2)));
        System.out.println(ans);
    }
}


