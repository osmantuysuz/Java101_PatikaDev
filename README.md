# Java 101 - PatikaDev

[Patika.dev](https://app.patika.dev/egitimler) adresindeki "Java ile Backend Web Development Patikası" eğitiminde kullandığım kaynak kodları içeren bir repo.

Bu README dosyasında bu eğitimdeki pratik ve ödevlerin cevaplarını bulacaksınız.

--------------------------------------------------------------------------------------------------------------------------------------

| PRATİK | ÖDEV |
|-----|-----|
|[PRATİK 1]() - Not Ortalaması|[ÖDEV 1]() - Vücut Kitle Endeksi Hesaplama|

|[PRATİK 2]()|[ÖDEV 2]()|

|[PRATİK 3]()|[ÖDEV 3]()|

|[PRATİK 4]()|[ÖDEV 4]()|

|[PRATİK 5]()|[ÖDEV 5]()|

|[PRATİK 6]()|[ÖDEV 6]()|

|[PRATİK 7]()|[ÖDEV 7]()|

|[PRATİK 8]()|[ÖDEV 8]()|

|[PRATİK 9]()|[ÖDEV 9]()|

|[PRATİK 10]()|[ÖDEV 10]()|

|[PRATİK 11]()|[ÖDEV 11]()|

|[PRATİK 12]()|[ÖDEV 12]()|

|[PRATİK 13]()|[ÖDEV 13]()|

|[PRATİK 14]()|

|[PRATİK 15]()|

|[PRATİK 16]()|

|[PRATİK 17]()|

|[PRATİK 18]()|

|[PRATİK 19]()|

|[PRATİK 20]()|

|[PRATİK 21]()|

|[PRATİK 22]()|

|[PRATİK 23]()|

|[PRATİK 24]()|

|[PRATİK 25]()|

|[PRATİK 26]()|

|[PRATİK 27]()|

--------------------------------------------------------------------------------------------------------------------------------------

## :brain: PRATİK 1 - Not Ortalaması

### :question: SORU 
Java dili ile 'Not Ortalaması Hesaplama' adında program yazalım. İçerisinde Matematik, Fizik, Kimya, Biyoloji, Türkçe ve Tarih dersleri olan öğrencinin aldığı notları girmesi sağlayarak derslerin not ortalamasını ona söyleyelim. 

:warning: İf-Else kullanmadan sadece koşullu ifadeler ileortalaması 60'tan büyük ise ona 'Başarılı' değil ise 'Başarısız' cevabı verelim.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>

```java
import org.w3c.dom.ls.LSOutput;

import java.util.Scanner;

public class test {
    public static void main(String[] args) {
        //Değişkenleri oluştur.
        int matematik, fizik, kimya, biyoloji, turkce, tarih;
        int toplam;
        double sonuc;

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
        boolean kosul = sonuc>=60;
        System.out.println("Durum: " + (kosul==true ? "Başarılı" : "Başarısız"));
    }
}
```
</details>

--------------------------------------------------------------------------------------------------------------------------------------
