# Proje: Kriptografik Olarak Güvenli Rastgele Sayı Üreteci (CSPRNG)

Bu proje, bir rastgele sayı üretecinin temel bileşenlerini ve kriptografik olarak güvenli bir versiyonunun nasıl oluşturulacağını göstermektedir.

## Projenin Amacı

Projenin iki temel amacı vardır:
1.  Sözde rastgele sayı üreteçlerinin (PRNG) çalışma mantığını anlamak.
2.  Güvenlik gerektiren uygulamalar için standart PRNG'lerin (LCG gibi) neden yetersiz olduğunu ve bunun yerine Kriptografik Olarak Güvenli Sözde Rastgele Sayı Üreteçlerinin (CSPRNG) neden kullanılması gerektiğini göstermek.

## İçerik

Bu repo aşağıdaki dosyaları içermektedir:

*   `1_Sozde_Kod_CSPRNG.md`: CSPRNG'nin kavramsal çalışma mantığını açıklayan sözde kod.
*   `2_Akis_Semasi_CSPRNG.md`: Algoritmanın mantıksal akışını gösteren metin tabanlı akış şeması ve görselleştirme kodu.
*   `3_Python_Kodu_CSPRNG.py`: Python'un `os` ve `secrets` modüllerini kullanarak CSPRNG'yi gerçekleyen program kodu.
*   `4_Ornek_Ciktilar_CSPRNG.txt`: Programın ürettiği örnek kriptografik olarak güvenli rastgele sayılar.
*   `README.md`: Bu dosya, projenin genel açıklamasını içerir.

## Algoritma: CSPRNG

Bu projede, basit matematiksel formüllere dayanan LCG (Doğrusal Eşlenik Üreteci) yerine, modern ve güvenli bir yaklaşım olan CSPRNG kullanılmıştır.

CSPRNG'ler, tahmin edilmesi neredeyse imkansız sayılar üretir. Bunun için klavye/fare hareketleri, ağ paketlerinin geliş zamanlamaları gibi işletim sisteminin topladığı öngörülemez verilerden (entropi) faydalanır.

Python'da bu, `os.urandom()` veya `secrets` modülü ile kolayca gerçekleştirilir. Bu yaklaşım, projenin güvenlik standartlarını en üst düzeye çıkarır.

## Nasıl Çalıştırılır?

1.  Sisteminizde Python 3'ün kurulu olduğundan emin olun.
2.  Terminali veya komut istemcisini açın.
3.  Aşağıdaki komutu çalıştırın:
    ```sh
    python 3_Python_Kodu_CSPRNG.py
    ```
4.  Program her çalıştığında farklı ve tahmin edilemez sayılar üretecektir.

