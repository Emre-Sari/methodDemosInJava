# methodDemosInJava
### kendisine parametre olarak gelen 3*4 lük 2 boyutlu string dizisindeki en uzun stringi ve yerini bulan metot 
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
### kendisine parametre olarak gelen stringdeki küçük karakterlerin sayısını geri döndüren metot 
```java
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
### kendisine parametre olarak gelen stringdeki küçük harfleri büyüğe büyük harfleri küçüğe çeviren method
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
### kendisine parametre olarak gelen 10 elamanlı tam sayı dizisinin tek elamanlarının ortalamasını bulan method
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
```



