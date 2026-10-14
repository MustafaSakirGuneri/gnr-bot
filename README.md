# GNR-BOT | E-Ticaret Otomasyon Sistemi

Python, Selenium ve Tkinter kullanilarak gelistirilmis, coklu urun ve ilan yonetimini otomatiklestiren masaustu otomasyon araci.

##  Ozellikler
* **Grafik ArayUz (GUI):** Tkinter ile tasarlanmis kullanici dostu ve kolay kullanim paneli.
* **Coklu Veri Kaynagi:** Excel (`.xlsx`), CSV ve TXT dosyalarindan dinamik veri okuma ve isleme.
* **Oturum Yonetimi:** Lokal Chrome profil destegi ile her defasinda tekrar giris yapma zahmetini ortadan kaldirir.
* **Dinamik XPath ve Form Yonetimi:** Urun adi, SKU, fiyat, kategori, marka ve teknik ozelliklerin otomatik doldurulmasi.
* **Gorsel Otomasyonu:** Urun klasorundeki gorselleri (JPG, PNG, WEBP) otomatik olarak sisteme toplu yukleme.
  
##  Karşılaşılan Zorluklar ve Çözümleri (Troubleshooting)
 ***Geliştirme sürecinde karşılaşılan bazı teknik zorluklar ve uygulanan çözümler:
*Dinamik XPath ve Tıklama Çakışmaları:** Sayfa yüklenmelerindeki gecikmeler nedeniyle elementlerin kaybolması veya `click()` komutunun yetersiz kalması sorunu;`WebDriverWait`, `ExpectedConditions` (EC) entegrasyonu ve güvenli JavaScript tıklama modulleri (`execute_script("arguments[0].click();", el)`) kullanılarak çözüldü.
*Arayüz Donması (GUI Freezing):** Selenium'un uzun süren döngüleri ve `time.sleep` beklemeleri Tkinter arayüzünün kilitlenmesine neden oluyordu. Bu sorun, botun mantığı ayrı bir arka plan iş parçacığına (`threading`) taşınarak tamamen ortadan kaldırıldı.
*Aynı html turlerinde `bg-secondary-container` ve `bg-first-container` gibi benzer kaydet butonları sorun çıkartıyordu bu yüzden `ancestor` XPath filtrelerini özel seçicilerle aşıldı.


##  Kullanılan Teknolojiler
* **Python**
* **Selenium** (Web Otomasyonu)
* **Tkinter** (Arayuz)
* **Pandas** (Veri Isleme)
* **Webdriver Manager**

##  Kurulum ve Çalıştırma
1. Repoyu klonlayin veya indirin:
   ```bash
   git clone [https://github.com/KULLANICI_ADIN/gnr-bot.git](https://github.com/KULLANICI_ADIN/gnr-bot.git)

## Gerekli Kutuphaneler
   '''pip install pandas selenium webdriver-manager
   '''python TKinter.PY;



   ENGLISH

   Features
Graphical User Interface (GUI): User-friendly panel designed with Tkinter.

Multi-Data Source: Dynamic data reading and processing from Excel (.xlsx), CSV, and TXT files.

Session Management: Eliminates repeated logins using local Chrome profile support.

Dynamic XPath & Form Management: Automated filling of product names, SKUs, prices, categories, brands, and specifications.

Image Automation: Bulk uploading of product images (JPG, PNG, WEBP) from the working folder.

 Tech Stack
Python

Selenium (Web Automation)

Tkinter (GUI Framework)

Pandas (Data Processing)

Webdriver Manager

 Installation & Usage
Clone or download the repository:

Bash
git clone https://github.com/KULLANICI_ADIN/gnr-bot.git
Install the required dependencies:

Bash
pip install pandas selenium webdriver-manager
