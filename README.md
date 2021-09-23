# Java 101 - PatikaDev

[Patika.dev](https://app.patika.dev/egitimler) adresindeki "Java ile Backend Web Development Patikası" eğitiminde kullandığım kaynak kodları içeren bir repo.

Bu README dosyasında bu eğitimdeki pratik ve ödevlerin cevaplarını bulacaksınız.

--------------------------------------------------------------------------------------------------------------------------------------
| PRATİK | ÖDEV |
|-----|-----|
| [PRATİK 1](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-1---not-ortalaması) - Not Ortalaması | [ÖDEV 1]() - Vücut Kitle Endeksi Hesaplama |
| [PRATİK 2](https://github.com/osmantuysuz/Java101_PatikaDev#brain-prati̇k-2---kdv-hesaplama) - Kdv Hesaplama | [ÖDEV 2]() - Manav Kasa |
| [PRATİK 3]() - Hipotenüs Bulma | [ÖDEV 3]() - Uçak Bileti Fiyatı Hesaplama |
| [PRATİK 4]() - Taksimetre | [ÖDEV 4]() - Çin Zodyağı Hesaplama |
| [PRATİK 5]() - Daire & Alan & Çevre | [ÖDEV 5]() - Artık Yıl Hesaplama |
| [PRATİK 6]() - Hesap Makinesi | [ÖDEV 6]() - Girilen Sayılardan Min ve Max Değerli Bulan Program |
| [PRATİK 7]() - Kullanıcı Girişi | [ÖDEV 7]() - Mükemmel Sayı Bulan Program |
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

:pill: Formül
Üç𝑔𝑒𝑛𝑖𝑛 ç𝑒𝑣𝑟𝑒𝑠𝑖 = 2𝑢
𝑢 = (a+b+c) / 2
Alan * Alan = 𝑢 * (𝑢 − 𝑎)* (𝑢 − 𝑏) * (𝑢 − 𝑐)

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
        alan= Math.sqrt(u* (u-a) * (u-b) * (u-c));

        //Sonucu ekrana yazdıralım.
        System.out.println("Girdiğiniz kenar değerlerine göre alan: " + alan);
    }
}

```
</details>

--------------------------------------------------------------------------------------------------------------------------------------