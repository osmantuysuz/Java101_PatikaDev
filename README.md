# Java 101 - PatikaDev

[Patika.dev](https://app.patika.dev/egitimler) adresindeki "Java ile Backend Web Development Patikası" eğitiminde kullandığım kaynak kodları içeren bir repo.

Bu README dosyasında bu eğitimdeki pratik ve ödevlerin cevaplarını bulacaksınız.

--------------------------------------------------------------------------------------------------------------------------------------
| PRATİK | ÖDEV |
|-----|-----|
| [PRATİK 1](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-1---not-ortalaması) - Not Ortalaması | [ÖDEV 1](https://github.com/osmantuysuz/Java101_PatikaDev#brain-ödev-1---vücut-kitle-i̇ndeksi-hesaplama) - Vücut Kitle Endeksi Hesaplama |
| [PRATİK 2](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-2---kdv-hesaplama) - Kdv Hesaplama | [ÖDEV 2](https://github.com/osmantuysuz/Java101_PatikaDev#brain-ödev-2---manav-kasa) - Manav Kasa |
| [PRATİK 3](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-3---hipotenüs-bulma) - Hipotenüs Bulma | [ÖDEV 3]() - Uçak Bileti Fiyatı Hesaplama |
| [PRATİK 4](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-4---taksimetre) - Taksimetre | [ÖDEV 4]() - Çin Zodyağı Hesaplama |
| [PRATİK 5](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-5---daire--alan--çevre) - Daire & Alan & Çevre | [ÖDEV 5]() - Artık Yıl Hesaplama |
| [PRATİK 6](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-6---hesap-makinesi) - Hesap Makinesi | [ÖDEV 6]() - Girilen Sayılardan Min ve Max Değerli Bulan Program |
| [PRATİK 7](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-7---kullanıcı-girişi) - Kullanıcı Girişi | [ÖDEV 7]() - Mükemmel Sayı Bulan Program |
| [PRATİK 8]() - Sınıfı Geçme Durumu | [ÖDEV 8]() - Ters Üçgen Yapımı |
| [PRATİK 9]() - Hava Sıcaklığına Göre Etkinlik Önerme | [ÖDEV 9]() -  1-100 Arasındaki Asal Sayıları Bulan Program |
| [PRATİK 10]() - Sayıları Büyükten Küçüğe Sıralayan Program | [ÖDEV 10]() - Fibonacci Serisi |
| [PRATİK 11]() - Burç Bulan Program | [ÖDEV 11]() - Üs Hesabı Yapan Program (Recursive Metot) |
| [PRATİK 12]() - Girilen Sayılardan Çift Sayıları Bulan Program | [ÖDEV 12]() - Asal Sayı Bulan Program (Recursive Metot) |
| [PRATİK 13]() - Tek Sayıların Toplamını Bulan Program | [ÖDEV 13]() - Desene Göre Metot Oluşturma (Recursive Metot) |
| [PRATİK 14]() - Girilen Sayıdan Küçük 2'nin Kuvvetlerini Bulan Program |
| [PRATİK 15]() - Faktöriyel Hesaplayan Program |
| [PRATİK 16]() - Üslü Sayı Hesaplayan Program |
| [PRATİK 17]() - Armstrong Sayıları Bulan Program |
| [PRATİK 18]() - Harmonik Sayıları Bulan Program |
| [PRATİK 19]() - Yıldız ile Üçgen Yapımı |
| [PRATİK 20]() - ATM Projesi |
| [PRATİK 21]() - EBOB ve EKOK Bulan Program |
| [PRATİK 22]() - Palindrom Sayılar |
| [PRATİK 23]() - Recursive ile Fibonacci Serisi |
| [PRATİK 24]() - Gelişmiş Hesap Makinesi |
| [PRATİK 25]() - Öğrenci Bilgi Sistemi |
| [PRATİK 26]() - Boks Oyunu |
--------------------------------------------------------------------------------------------------------------------------------------

## :brain: PRATİK 1 - Not Ortalaması

### :question: SORU 
Java dili ile 'Not Ortalaması Hesaplama' adında program yazalım. İçerisinde Matematik, Fizik, Kimya, Biyoloji, Türkçe ve Tarih dersleri olan öğrencinin aldığı notları girmesi sağlayarak derslerin not ortalamasını ona söyleyelim. 

:warning: İf-Else kullanmadan sadece koşullu ifadeler ileortalaması 60'tan büyük ise ona 'Başarılı' değil ise 'Başarısız' cevabı verelim.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {
        //Değişkenleri oluştur.
        int matematik, fizik, kimya, biyoloji, turkce, tarih;
        int toplam;
        double sonuc;
        boolean kosul

        //Kullanıcıdan değerleri al.
        Scanner input = new Scanner(System.in);
        System.out.print("Matematik puanınızı giriniz: ");matematik=input.nextInt();
        System.out.print("Fizik puanınızı giriniz: ");fizik=input.nextInt();
        System.out.print("Kimya puanınızı giriniz: ");kimya=input.nextInt();
        System.out.print("Biyoloji puanınızı giriniz: ");biyoloji=input.nextInt();
        System.out.print("Türkçe puanınızı giriniz: ");turkce=input.nextInt();
        System.out.print("Tarih puanınızı giriniz: ");tarih=input.nextInt();

        //Hesaplamaları yap
        toplam=(matematik + fizik + kimya + biyoloji + turkce + tarih);
        sonuc=toplam/6;

        //Ekrana çıktıları yazdır
        System.out.println("Ders ortalamanız: " + sonuc);


        //Ekstra koşul ile uygulamamızı yazarsak.
        kosul = sonuc>=60;
        System.out.println("Durum: " + (kosul==true ? "Başarılı" : "Başarısız"));
    }
}
```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 2 - Kdv Hesaplama

### :question: SORU 
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın.

:warning: Eğer girilen tutar 0 ve 1000 TL arasında ise KDV oranı %18 , tutar 1000 TL'den büyük ise KDV oranını %8 olarak KDV tutarı hesaplayan programı yazınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double tutar, kdvliTutar, fark, kdvTutar1=0.18, kdvTutar2=0.08;
        boolean kosul1;

        //Kullanıcıdan Kdv hesaplanacak miktarı isteyelim
        Scanner input=new Scanner(System.in);
        System.out.print("Lütfen Kdv hesaplanacak miktarı girin: ");
        tutar=input.nextDouble();

        //Koşullarımızı yazalım.
        kosul1=tutar>1000;

        //Sonuçları ekrana yazdıralım
        System.out.println("KDV oranı: "+ (kosul1==true ? kdvTutar2 : kdvTutar1));
        System.out.println("KDV Tutarı: " + (kosul1==true ? tutar*kdvTutar2 : tutar*kdvTutar1));
        System.out.println("KDV'li Tutar: " + (kosul1==true ? tutar+(tutar*kdvTutar2) : tutar+(tutar*kdvTutar1)));
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 3 - Hipotenüs Bulma

### :question: SORU 
Java ile kullanıcıdan dik kenarlarının uzunluğunu alan ve hipotenüsü hesaplayan programı yazın.

:warning: Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan programı yazınız.

:pill: Formül Üçgenin çevresi = 2u

:pill: Formül u = (a+b+c)/2

:pill: Formül Alan * Alan = u* (u-a) * (u-b) * (u-c)

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        int a,b;
        double c;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("Birinci kenarı giriniz: ");
        a=input.nextInt();
        System.out.print("İkinci kenarı giriniz: ");
        b=input.nextInt();

        //Hipotenüs hesaplayalım.
        c=Math.sqrt((a*a)+(b*b));

        //Sonuçları ekrana yazalım.
        System.out.println("Hipotenüs: "+c);

        //--------------------------------------------------------
        //Ödev olarak verilen kısım.
        //Değişkenleri oluşturalım.
        double alan, u;

        //Kullanıcıdan 3 kenar uzunluğu alalım.
        System.out.println("Bir üçgenin alanının hesaplanması.");
        System.out.print("Üçgenin 1. kenarını giriniz: ");
        a=input.nextInt();
        System.out.print("Üçgenin 2. kenarını giriniz: ");
        b=input.nextInt();
        System.out.print("Üçgenin 3. kenarını giriniz: ");
        c=input.nextInt();

        //Hesaplamaları yapalım
        u=(a+b+c)/2;
        alan = Math.sqrt(u* (u-a) * (u-b) * (u-c));

        //Sonucu ekrana yazdıralım.
        System.out.println("Girdiğiniz kenar değerlerine göre alan: " + alan);
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 4 - Taksimetre

### :question: SORU 
Java ile gidilen mesafeye (KM) göre taksimetre tutarını ekrana yazdıran programı yazın.

:warning: Şartlar

:pill: Taksimetre KM başına 2.20 TL tutmaktadır.

:pill: Minimum ödenecek tutar 20 TL'dir. 20 TL altında ki ücretlerde yine 20 TL alınacaktır.

:pill: Taksimetre açılış ücreti 10 TL'dir.


### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double gidilecekKm, kmBasinaTutar=2.20, acilisUcret=10, odenecekTutar;

        boolean kosul1;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("Kaç Km yol gideceksiniz: ");
        gidilecekKm=input.nextInt();


        //Taksimetre tutarı hesaplayalım.
        kosul1=gidilecekKm>20;

        //Sonuçları ekrana yazalım.
        System.out.println("Taksimetre Tutar: " + ((kosul1) ? 10+(gidilecekKm*kmBasinaTutar) : 20));
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 5 - Daire & Alan & Çevre

### :question: SORU 
Java ile yarı çapını kullanıcıdan aldığınız dairenin alanını ve çevresini hesaplayan programı yazın.

:warning: Yarıçapı r, merkez açısısının ölçüsü 𝛼 olan daire diliminin alanı bulan programı yazınız.

:pill: Alan Formülü : π * r * r;

:pill: Çevre Formülü : 2 * π * r;

:pill: 𝜋 sayısını = 3.14 alınız.

:pill: Formül : (𝜋 * (r*r) * 𝛼) / 360

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double  pi=3.14, yaricap, cevre, alan, merkezAci, daireDilimi;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("Yarıçapı giriniz: ");
        yaricap=input.nextDouble();
        System.out.print("Merkez açıyı giriniz: ");
        merkezAci=input.nextDouble();

        //Hesaplamaları yapalım.
        cevre=2*pi*yaricap;
        alan=pi*yaricap*yaricap;
        daireDilimi=((pi*(yaricap*yaricap)*merkezAci)/360);

        //Sonuçları ekrana yazalım.
        System.out.println("Dairenin Alanı: " + alan);
        System.out.println("Dairenin Çevresi: " + cevre);
        System.out.println("Daire Dilim Ölçüsü: " + daireDilimi);
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 6 - Hesap Makinesi

### :question: SORU 
Java koşullu ifadeler ile basit hesap makinesi yapımı.

:warning: Videodaki hesap makinesini switch-case kullanarak yapınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double  sayi1, sayi2, sonuc;
        char islem;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("1. Sayıyı Giriniz: ");
        sayi1=input.nextDouble();
        System.out.print("2. Sayıyı Giriniz: ");
        sayi2=input.nextDouble();

        //Kullanıcıya bilgiler verelim
        System.out.println("");
        System.out.println("+ (Toplama)");
        System.out.println("- (Çıkarma)");
        System.out.println("* (Çarpma)");
        System.out.println("/ (Bölme)");
        System.out.println("Hangi işlemi yapmak istiyorsunuz");

        //Kullanıcıdan yapacağı işlemi alalım
        islem=input.next().charAt(0);

        //Sonucu ekrana yazdıralım.
        switch (islem){
            case '+':
                sonuc=sayi1+sayi2;
                System.out.println("Toplama sonucu: " + sonuc);
                break;
            case '-':
                sonuc=sayi1-sayi2;
                System.out.println("Çıkarma sonucu: " + sonuc);
                break;
            case '*':
                sonuc=sayi1*sayi2;
                System.out.println("Çarpma sonucu: " + sonuc);
                break;
            case '/':
                if (sayi2==0){
                    System.out.println("Bir sayı sıfıra bölünemez!");
                    break;
                }else {
                    sonuc=sayi1/sayi2;
                    System.out.println("Bölme sonucu: " + sonuc);
                    break;
                }
            default:
                System.out.println("Yanlış bir işlem seçtiniz?");
                break;
        }
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 7 - Kullanıcı Girişi

### :question: SORU 
Java koşullu ifadeler ile kullanıcı adı ve şifreyi kontrol eden program yapımı.

:warning: Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişken tanımlamaları
        String userName, passWord;
        char sifreCevap;

        Scanner input = new Scanner(System.in);

        // Kullanıcıdan username ve password girişinin istenmesi
        System.out.print("Lütfen kullanıcı adınızı giriniz: ");
        userName = input.nextLine();

        System.out.print("Lütfen şifrenizi giriniz: ");
        passWord = input.nextLine();

        // Alınan bilgilerin kontrolü ve hatalı işlem cevapları
        if (userName.equals("patika")) {
            if (passWord.equals("dev")) {
                System.out.println("Sisteme başarılı bir şekilde giriş yaptınız.");
            } else {
                System.out.println("Hatalı şifre girişi !!!");
                System.out.print("Şifrenizi sıfırlamak ister misiniz? E/H : ");
                sifreCevap = input.next().charAt(0);

                if (sifreCevap == 'E') {

                    System.out.print("Lütfen yeni şifrenizi giriniz: ");
                    // Eğer String newPassword = input.nextline(); olarak yazılmış olsaydı sistem bu kodu atlayacaktı.
                    // Bu nedenle input.next(); olarak değer aldırıldı.
                    String newPassword = input.next();

                    if (newPassword.equals(passWord) || newPassword.equals("dev")) {
                        System.out.print("Şifre oluşturulamadı");
                    } else {
                        System.out.print("Şifre oluşturuldu.");
                    }
                } else if (sifreCevap == 'H') {
                    System.out.print("Şifre oluşturma işlemi iptal edildi..");

                } else {
                    System.out.print("Lütfen geçerli bir parametre giriniz. E (Evet) veya H (Hayır) !!!");
                }
            }
        } else {
            System.out.println("Hatalı kullanıcı adı girişi !!!");
        }
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: PRATİK 8 - Sınıfı Geçme Durumu

### :question: SORU 
Java koşullu ifadeler ile kullanıcının not durumuna göre sınıfı geçme durumunu hesaplayan program yapımı.

:pill: Dersler: Matematik, Fizik, Türkçe, Kimya, Müzik
:pill: Geçme Notu: 55

:warning: Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişken tanımlamaları
        int turkce, matematik, fizik, kimya, muzik, ortalama, dersSayisi=5;



        // Kullanıcıdan ders notlarını isteyelim.
        Scanner input = new Scanner(System.in);
        System.out.print("Türkçe: ");
        turkce = input.nextInt();
        System.out.print("Matematik: ");
        matematik = input.nextInt();
        System.out.print("Fizik: ");
        fizik = input.nextInt();
        System.out.print("Kimya: ");
        kimya = input.nextInt();
        System.out.print("Müzik: ");
        muzik = input.nextInt();


        // Alınan ders notlarının 0 ile 100 arasında olduğunu kontrol edelim.
        //0-100 arasında değilse ortalama hesabına katılmayacak
        if (turkce>100 || turkce<0){
            dersSayisi--;
            turkce=0;
        } if (matematik>100 || matematik<0){
            dersSayisi--;
            matematik=0;
        } if (fizik>100 || fizik<0){
            dersSayisi--;
            fizik=0;
        } if (kimya>100 || kimya<0){
            dersSayisi--;
            kimya=0;
        } if (muzik>100 || muzik<0){
            dersSayisi--;
            muzik=0;
        }

        //Ortalama hesabını yapalım
        ortalama=(turkce+matematik+fizik+kimya+muzik)/dersSayisi;

        //Sonucu yazdıralım
        if (ortalama<55)
            System.out.println("Kaldınız. Ortalamanız: " + ortalama);
        else if (ortalama>=55 && ortalama<=100)
            System.out.println("Geçtiniz. Ortalamanız: " + ortalama);
    }
}
```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: ÖDEV 1 - Vücut Kitle İndeksi Hesaplama

### :question: SORU 
Java ile kullanıcıdan boy ve kilo değerlerini alıp bir değişkene atayın. Aşağıda ki formüle göre kullanıcının "Vücut Kitle İndeks" değerini hesaplayıp ekrana yazdırın.

:warning: Formül Kilo (kg) / Boy(m) * Boy(m)

:heavy_check_mark: Çıktısı
```
Lütfen boyunuzu (metre cinsinde) giriniz : 1,72
Lütfen kilonuzu giriniz : 105
Vücut Kitle İndeksiniz : 35.49215792320173
```
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double  boy, kilo, kitleIndeks;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("Boyunuzu (metre cinsinden) Giriniz: ");
        boy=input.nextDouble();
        System.out.print("Kilonuzu Giriniz: ");
        kilo=input.nextDouble();

        //Hesaplamaları yapalım.
        kitleIndeks=kilo/(boy*boy);

        //Sonuçları ekrana yazalım.
        System.out.println("Vücut Kitle Endeksiniz: " + kitleIndeks);
    }
}
```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
## :brain: ÖDEV 2 - Manav Kasa

### :question: SORU 
Java ile kullanıcıların manavdan almış oldukları ürünlerin kilogram değerlerine göre toplam tutarını ekrana yazdıran programı yazın.

:pushpin: Meyveler ve KG Fiyatları
- Armut: 2,14 TL
- Elma: 3,67 TL
- Domates: 1,11 TL
- Muz: 0,95 TL
- Patlıcan: 5,00 TL

:heavy_check_mark: Örnek Çıktı
```
Armut Kaç Kilo ? :0
Elma Kaç Kilo ? :1
Domates Kaç Kilo ? :1
Muz Kaç Kilo ? :2
Patlıcan Kaç Kilo ? :3
Toplam Tutar : 21.68 TL
```


### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import java.util.Scanner;

public class test {
    public static void main(String[] args) {

        //Değişkenleri oluşturalım.
        double  armutKG=2.14, elmaKG=3.67, domatesKG=1.11, muzKG=0.95, patlicanKG=5.00, tutar, armut, elma, domates ,muz ,patlican;

        //Kullanıcıdan verilerimizi alalım
        Scanner input = new Scanner(System.in);
        System.out.print("Armut Kaç Kilo?: ");
        armut=input.nextDouble();
        System.out.print("Elma Kaç Kilo?: ");
        elma=input.nextDouble();
        System.out.print("Domates Kaç Kilo?: ");
        domates=input.nextDouble();
        System.out.print("Muz Kaç Kilo?: ");
        muz=input.nextDouble();
        System.out.print("Patlıcan Kaç Kilo?: ");
        patlican=input.nextDouble();

        //Hesaplamaları yapalım.
        tutar=(armut*armutKG)+(elma*elmaKG)+(domates*domatesKG)+(muz*muzKG)+(patlican*patlicanKG);

        //Sonuçları ekrana yazalım.
        System.out.println("Toplam Tutar: " + tutar);
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
