# methodDemosInJava
### kendisine parametre olarak gelen sayı kadar 8 karakterli rastgele harflerden oluşan şifreler oluşruran method;
### Password method consisting of 8-character letters as much as the number that comes as a parameter;
```java
public class createRandomPassword {

    public static void main(String[] args) {
        create(5);
    }
    public static String create(int number) {
        String str = "";
        for (int i = 0; i < number; i++) {
            Random random_number = new Random();
            for (int j = 0; j <= 7; j++) {
                char karakter = (char) random_number.nextInt(97, 122);
                str += karakter;
            }
            System.out.println(str);
            str = "";
        }
        return str;
    }
}
```
### kendisine parametre olarak gelen diziyi bir sağa çeviren method;
### the method that turns the string that comes as a parameter to the right;
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
### kendisine parametre olarak gelen 3*4 lük 2 boyutlu string dizisindeki en uzun stringi ve yerini bulan method;
### The longest string in the 3*4 2-dimensional string array that comes as a parameter and its location method;
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
### method that returns the number of lowercase characters in the string that comes as a parameter;
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
### method that finds how many words are in the string that comes to it as a parameter;
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
### The method that converts the string that comes as a parameter to lowercase, uppercase, uppercase;
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
### The method that finds the average of the single elements of the 10-element integer array that comes as a parameter;

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
### method that returns the biggest and smallest value in the 10-element array that comes to it as a parameter;
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
### kendisine parametre olarak gelen dizinin sıralı olup olmadığını bulan method;
### method that finds whether the array that comes to it as a parameter is sequential;
```java
public class serialMethods {
    public static void main(String[] args) {
        System.out.println(isserial(create_array(4)));
        
    }public static int[] create_array(int each){
        int arrays[]=new int[each];
        Scanner s = new Scanner(System.in);
        for(int i=0;i<each;i++){
            int number=s.nextInt();
            arrays[i]=number;
        }return arrays;
    }
    public static boolean isserial(int[] array){
        for(int i=0;i<array.length-1;i++){
            if(array[i]>array[i+1]){
                return false;
            }
        }return true;
    }public static void check(boolean a){
        if(a==false){
            
            System.out.println("it is a serial array");
        }else{
            System.out.println("it is not a serial array");
        }        

    }
}
```
### kendisine parametre olarak gelen iki stringden büyük olanı döndüren method;
### method that returns the larger of the two strings that come to it as a parameter;
```java
public class whichStringBiggest {

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str1 = s.next();
        String str2 = s.next();
        whichStringBiggest w = new whichStringBiggest();
        String enb = w.biggest(str1, str2);
        System.out.println(enb);
    }

    public static String biggest(String str1, String str2) {
        if (str1.length() > str2.length()) {
            return str1;
        } else {
            return str2;
        }
    }
}
```
### kendisine parametre olarak gelen onluk tabandaki sayıyı ikilik tabana çeviren method;
### the method that converts the decimal number that comes as a parameter to binary;
```java
public class decimalNumberToBinaryNumber {

    public static void main(String[] args) {
        System.out.println(convert(21));

    }

    public static String convert(int number) {
        int binary[] = new int[40];
        String str = "";
        int index = 0;
        while (number > 0) {
            binary[index] = number % 2;
            index += 1;
            number = number / 2;
        }
        for (int i = index - 1; i >= 0; i--) {
            str += binary[i];
        }
        return str;
    }
}
```
### kendisine parametre olarak gelen ikilik tabandaki tamsayıyı onluk tabana çeviren method;
### The method that converts the binary integer to decimal that comes as a parameter;
```java
public class binaryNumberToDecimalNumber {

    public static void main(String[] args) {
        System.out.println(convert(1110));
    }
    public static int convert(int number) {
        int sum = 0;
        String str = String.valueOf(number);
        int sayac = 0;
        for (int i = str.length() - 1; i >= 0; i--) {
            if (str.charAt(i) == '1') {
                double islem = Math.pow(2, sayac);
                sum += islem;
            } else {
            }
            sayac += 1;
        }
        return sum;
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisini küçükten büyüğe sıralayan method;
### The method that sorts the integer array that comes as a parameter from smallest to largest;
```java
public class selectionInShort {

    public static void main(String[] args) {

        int dizi[] = {3, 17, 86, -9, 7, -11, 38};

        write(short_by(dizi));
    }

    public static int[] short_by(int[] array) {
        for (int i = 0; i < array.length; i++) {
            int index = i;
            for (int j = i + 1; j < array.length; j++) {
                if (array[j] < array[index]) {
                    index = j;
                }
            }
            int yedek = array[i];
            array[i] = array[index];
            array[index] = yedek;
        }
        return array;
    }

    public static void write(int[] array) {
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }
    }
}
```
### kendisine parametre olarak gelen Stringi tersten yazan method;
### method that writes the String that comes as a parameter in reverse;
```java
public class oppositeOfString {

    public static void main(String[] args) {
        System.out.println(opposite_write("polis"));

    }

    public static String opposite_write(String str) {
        String opposite = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            opposite += str.charAt(i);
        }
        return opposite;
    }

}
```
### kendisine parametre olarak gelen stringin polindrom olup olmadığını döndüren method;
### method that returns whether the string that comes as a parameter is a polyndrome;
```java
public class isİtPolindrom {

    public static void main(String[] args) {
        System.out.println(polindrommu("kabak"));
    }

    public static boolean polindrommu(String str) {
        for (int i = 0, j = str.length() - 1; i < str.length(); i++, j--) {
            if (str.charAt(i) != str.charAt(j)) {
                return false;
            }
        }
        return true;
    }
}
```
### kendisine parametre olarak gelen sayının asal olup olmadığını bulan method;
### method that finds whether the number that comes as a parameter is prime or not;
```java
public class isItPrimeNumber {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int sayi=s.nextInt();
        control(is_prime(sayi));
        
    }public static boolean is_prime(int number){
        for(int i=2;i<number;i++){
            if(number%i==0){
                return false;
            }
        }return true;
    }public static void control(boolean a){
        if(a == true){
            System.out.println("sayı asaldır");
            
        }else{
            System.out.println("sayı asal değildir");
        }
    }
}
```
### kendisine parametre olarak gelen string içinde kaç adet "aa" olduğunu bulan method;
### method that finds how many "aa" there are in the string that comes as a parameter;
```java
public class howManyThereİsAA {

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        howManyThereİsAA k = new howManyThereİsAA();
        String name = s.next();
        int a = k.count(name);
        System.out.println(a);
    }

    public static int count(String str) {
        int counter = 0;
        for (int i = 0; i < str.length() - 1; i++) {
            if (str.charAt(i) == 'a' && str.charAt(i + 1) == 'a') {
                i++;
                counter += 1;
            }
        }
        return counter;

    }
}
```
### kendisine parametre olarak gelen tamsayı dizisindeki en büyük elamanın yerini bulan method;
### method that finds the location of the largest element in the integer array that comes to it as a parameter;
```java
public class findPlaceOfLongestString {

    public static void main(String[] args) {
        find(create_array(4));
    }

    public static String[] create_array(int each) {
        Scanner s = new Scanner(System.in);
        String array[] = new String[each];
        for (int i = 0; i < each; i++) {
            String str = s.next();
            array[i] = str;
        }
        return array;
    }

    public static int find(String[] array) {
        int enb = array[0].length();
        int indis = 0;
        for (int i = 1; i < array.length; i++) {
            if (array[i].length() > enb) {
                indis = i;
                enb = array.length;
            }
        }
        System.out.println(indis);
        return indis;
    }
}
```
### kendisine parametre olarak gelen tam sayının basamakları ekrana yazan method;
### method that writes the digits of the integer that comes as a parameter to the screen;
```java
public class findDigitNumber {
    public static void main(String[] args) {
        read(789);
    }

    public static void read(int number) {
        int each = 0;
        int digit;
        while (number > 0) {
            each++;
            digit = number % 10;
            System.out.println(digit);
            number = number / 10;
        }
        System.out.println(each + " basamaklı");

    }
}










