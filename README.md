# methodDemosInJava
### kendisine parametre olarak gelen diziyi bir sağa çeviren method;
```java
public class toOneRightReturnMethod {
    public static void main(String[] args) {
        read_arrays(to_one_right(create_array()));
        
    }public static int[] create_array(){
        Scanner s = new Scanner(System.in);
        int dizi[]=new int[10];
        for(int i=0;i<dizi.length;i++){
            int number=s.nextInt();
            dizi[i]=number;
        }return dizi;
    }public static int[] to_one_right(int[] a){
      int yedek=a[a.length-1];
      for(int i=8;i>=0;i--){
          a[i+1]=a[i];}
      a[0]=yedek;
      return a;
      }public static int[] read_arrays(int[] m ){
          for(int i=0;i<m.length;i++){
              System.out.println(m[i]);
          }return null;
}
    }```
### kendisine parametre olarak gelen 3*4 lük 2 boyutlu string dizisindeki en uzun stringi ve yerini bulan method;
```java
public class fındLongestStringİnArrays {
    public static void main(String[] args) {
       Scanner s = new Scanner(System.in);
       String dizi[][]=new String[3][4];
       for(int i=0;i<3;i++){
           for(int j=0;j<4;j++){
               String isim=s.next();
               dizi[i][j]=isim;
           }
       }
       fındLongestStringİnArrays a = new fındLongestStringİnArrays();
       a.bul(dizi);  
    }public static String bul(String[][]a){
        int enb=a[0].length;
        String str="";
        int satir,sutun;
        for(int i=0;i<3;i++){
            for(int j=0;j<4;j++){
                if(a[i][j].length()>enb){
                    enb=a[i][j].length();
                    satir=i;
                    sutun=j;       
                    str=a[i][j];
                }if(i==2 &&j==3){
                    System.out.println("en büyük string : "+str+
                            " bu stringin "+i+". satır "+j+". sütunda");
                }
            }
        }return str;
        
    }
}
```
### kendisine parametre olarak gelen stringdeki küçük karakterlerin sayısını geri döndüren method;
public class countLowerCase {
    public static void main(String[] args) {
        count("emRe");
    }public static int count(String str){
        int sayac=0;
        for(int i=0;i<str.length();i++){
            if(str.charAt(i)>='a' && str.charAt(i)<='z'){
                sayac+=1;
            }
        }
        System.out.println(sayac);
        return sayac;
        
    }
    
}
```
### kendisine parametre olarak gelen string içinde kaç adet kelime olduğunu bulan method;
```java
public class howManyThereİsWord {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str=s.nextLine();
        howManyThereİsWord w = new howManyThereİsWord();
        int adet=w.count(str);
        System.out.println(adet);
        
    }public static int count(String str){
        int counter=0;
        for(int i=0;i<str.length();i++){
            if(str.charAt(i)==' '){
                counter+=1;          
        }
        }return counter+1;
    }
}
```
### kendisine parametre olarak gelen stringdeki küçük harfleri büyüğe büyük harfleri küçüğe çeviren method;
```java
public class lowCharactertoUpCharacteANDupCharactertoLowCharacter {
    public static void main(String[] args) {
        String str=convert("ikTiSaT");
        System.out.println(str);
    }
    public static String convert(String str) {
        String yeni = "";
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) <= 'z' && str.charAt(i) >= 'a') {
                char c = str.charAt(i);
                String s = String.valueOf(c);
                String k = s.toUpperCase();
                yeni += k;
            } else {
                char c = str.charAt(i);
                String s = String.valueOf(c);
                String k = s.toLowerCase();
                yeni += k;
            }
        }
        return yeni;
        
    }

}
```
### kendisine parametre olarak gelen 10 elamanlı tam sayı dizisinin tek elamanlarının ortalamasını bulan method;
```java
public class sumOfoddNumberInArray {
    public static void main(String[] args) {
        
        System.out.println(calculate_sum_of_add_numbers(create_array()));
        
    }public static int[] create_array(){
        Scanner s = new Scanner(System.in);
        int dizi[]= new int[10];
        for(int i=0;i<dizi.length;i++){
            int number=s.nextInt();
            dizi[i]=number;
        }return dizi;
    }public static int calculate_sum_of_add_numbers(int[] array){
        int total=0;
        int mean=0;
        for(int i=0;i<array.length;i++){
            if(array[i]%2!=0){
                mean+=1;
                total+=array[i];
            }
        }int calculater=total/mean;
        return calculater;
    }
}
```
### kendisine parametre olarak gelen 10 elamanlı dizideki en büyük ve en küçük değeri döndüren method;
```java
public class theBiggestAndTheShortest {
    public static void main(String[] args) {
        Scanner s =new Scanner(System.in);
        int dizi[]=new int[10];
        for(int i=0;i<dizi.length;i++){
            int sayi=s.nextInt();
            dizi[i]=sayi;
        }
        bul(dizi);
    }public static int[] bul(int[] a) {
        int dizi[] = new int[2];
        int enb = a[0];
        int enk = a[0];
        for (int i = 1; i < a.length; i++) {
            if (a[i] > enb) {
                enb=a[i];
            } else if (a[i] < enk) {
                enk=a[i];
            }
        }
        dizi[0] = enb;
        dizi[1] = enk;
        System.out.println("dizinin enk değeri : "+enk);
        System.out.println("dizinin enb değeri : "+enb);
        return dizi;

    }
    
}
```
### kendisine parametre olarak gelen diziyi bir sağa çeviren method;
```java
public class toOneRightReturnMethod {
    public static void main(String[] args) {
        read_arrays(to_one_right(create_array()));
        
    }public static int[] create_array(){
        Scanner s = new Scanner(System.in);
        int dizi[]=new int[10];
        for(int i=0;i<dizi.length;i++){
            int number=s.nextInt();
            dizi[i]=number;
        }return dizi;
    }public static int[] to_one_right(int[] a){
      int yedek=a[a.length-1];
      for(int i=8;i>=0;i--){
          a[i+1]=a[i];}
      a[0]=yedek;
      return a;
      }public static int[] read_arrays(int[] m ){
          for(int i=0;i<m.length;i++){
              System.out.println(m[i]);
          }return null;
}
    }
```
```



