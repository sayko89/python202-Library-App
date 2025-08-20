# python202-Library-App
📚 Library API Projesi
Bu proje, Global AI Hub Python 202 Bootcamp kapsamında geliştirilmiştir. Amaç, Python'da Nesne Yönelimli Programlama (OOP), Harici API kullanımı ve FastAPI ile kendi API'mizi geliştirme adımlarını birleştirerek somut bir ürün ortaya çıkarmaktır.
Projeyi üç aşamada inşa ettim:
1.	Komut satırında basit bir kitap yönetim sistemi 
2.	Harici bir API’den (ör. Google Books API) veri çekme
3.	FastAPI ile kendi servisimiz üzerinden bu verileri sunma
________________________________________
🚀 Kurulum
Projeyi kendi bilgisayarınızda çalıştırmak için şu adımları takip edebilirsiniz:
1.	Projeyi klonlayın
2.	git clone https://github.com/kullanici/library-project.git
3.	cd library-project
4.	Sanal ortam oluşturun (opsiyonel)
5.	python -m venv venv
6.	source venv/bin/activate   # Mac/Linux
7.	venv\Scripts\activate      # Windows
8.	Bağımlılıkları yükleyin
9.	pip install -r requirements.txt
10.	API sunucusunu çalıştırın
11.	uvicorn main:app --reload
________________________________________
🛠 Kullanım
API şu anda 3 temel endpoint içeriyor:
•	GET /books → Sistemdeki tüm kitapları listeler
•	POST /books → Yeni kitap ekler. Eğer ISBN girerseniz, Google Books API’den kitap bilgilerini otomatik çeker.
•	DELETE /books/{isbn} → Belirtilen ISBN numarasına sahip kitabı siler
________________________________________
📂 Proje Yapısı
library-project/
│── main.py          # FastAPI uygulaması
│── books.py         # OOP ile kitap sınıfı ve yönetimi
│── api_service.py   # Harici API (Google Books) ile entegrasyon
│── requirements.txt # Bağımlılıklar
│── README.md        # Proje açıklamaları
________________________________________
🌟 Örnek Kullanım
Yeni kitap ekleme:
POST /books
{
  "isbn": "9780140449136"
}
Kitapları listeleme:
GET /books
Kitap silme:
DELETE /books/9780140449136
________________________________________
📌 Not
Bu proje, Python 202 Bootcamp’in son pro
