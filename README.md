# 🏥 Hastane Yönetim Sistemi (Hospital Management System)

Bu proje, **Java** dilinde geliştirilmiş nesne tabanlı bir **Hastane Yönetim Sistemi** uygulamasıdır.  
Sistem; **hasta**, **doktor** ve **randevu** işlemlerini konsol üzerinden yönetmeyi sağlar.

---

## 🚀 Proje Özeti

Bu uygulama bir hastanede gerçekleşen temel işlemleri yönetmek için tasarlanmıştır.  
Kullanıcı, menü üzerinden şu işlemleri yapabilir:

- Yeni hasta kaydı oluşturma  
- Doktor kaydı ekleme  
- Hasta / doktor arama  
- Randevu oluşturma, iptal etme veya listeleme  
- Tüm kayıtları detaylı şekilde görüntüleme  

Proje nesne yönelimli programlama (OOP) ilkelerine göre tasarlanmıştır.  
Sınıflar arasında **kalıtım (inheritance)** ve **kapsülleme (encapsulation)** kavramları etkin biçimde kullanılmıştır.

---

## 🧩 Sınıf Yapısı

### 🔹 `Kisi`
- Hasta ve Doktor sınıflarının üst sınıfıdır.  
- Ortak özellikleri içerir: `ad`, `soyad`, `tcNo`, `telefon`.

### 🔹 `Hasta`
- `Kisi` sınıfından türetilmiştir.  
- Her hasta için otomatik artan bir `hastaNo` değeri atanır.  
- Metotlar:
  - `getHastaNo()`
  - `toString()` — Hasta bilgilerini biçimli olarak döndürür.

### 🔹 `Doktor`
- `Kisi` sınıfından türetilmiştir.  
- Her doktorun kendine özgü bir `doktorId` ve `brans` (branş) bilgisi vardır.  
- Metotlar:
  - `getDoktorId()`, `getBrans()`
  - `toString()` — Doktor bilgilerini biçimli olarak döndürür.

### 🔹 `Randevu`
- Bir `Hasta` ve bir `Doktor` arasında oluşturulan randevuyu temsil eder.  
- Özellikler:
  - `randevuNo`, `tarih`, `saat`, `durum`  
- Metotlar:
  - `iptalEt()` — Randevunun durumunu "İptal" yapar.  
  - `toString()` — Randevu bilgilerini formatlı olarak döndürür.

### 🔹 `HastaneYonetimSistemi`
- Sistemin merkezidir.  
- Hasta, doktor ve randevu listelerini yönetir.  
- Ana menü üzerinden tüm işlemler bu sınıf aracılığıyla yapılır.

**Ana menü seçenekleri:**
1. Hasta İşlemleri
2. Doktor İşlemleri
3. Randevu İşlemleri
4. Listeleme
0. Çıkış

### 🔹 `Main`
- Programın giriş noktasıdır.  
- `HastaneYonetimSistemi` sınıfını başlatır:

```java
public static void main(String[] args) {
    HastaneYonetimSistemi sistem = new HastaneYonetimSistemi();
    sistem.anaMenu();
}
```

---

## 🧠 Kullanılan Kavramlar

| Kavram | Açıklama |
|--------|----------|
| **Encapsulation (Kapsülleme)** | Tüm özellikler private olarak tanımlanmış ve getter/setter metodlarıyla erişim sağlanmıştır. |
| **Inheritance (Kalıtım)** | Hasta ve Doktor, Kisi sınıfından türetilmiştir. |
| **Static Değişkenler** | hastaNo, doktorId ve randevuNo değerleri otomatik artan sayaçlarla yönetilir. |
| **ArrayList Kullanımı** | Kayıtlar dinamik listelerde tutulur (ArrayList<Hasta>, ArrayList<Doktor>, ArrayList<Randevu>). |
| **Polimorfizm** | toString() metodu sınıflara göre özelleştirilmiştir. |

---

## 💻 Proje Çalıştırma

### 🔧 Gereksinimler
- Java JDK 8 veya üzeri
- IntelliJ IDEA, Eclipse veya VS Code (Java eklentisiyle)

### ▶️ Çalıştırma Adımları
1. Tüm `.java` dosyalarını `src` klasörüne yerleştirin.
2. IDE'de yeni bir Java Project oluşturun.
3. `Main.java` dosyasını çalıştırın.
4. Konsolda menü aracılığıyla işlemleri gerçekleştirin.

---

## 📂 Proje Dosya Yapısı

```
📦 HastaneYonetimSistemi
 ┣ 📜 Kisi.java
 ┣ 📜 Hasta.java
 ┣ 📜 Doktor.java
 ┣ 📜 Randevu.java
 ┣ 📜 HastaneYonetimSistemi.java
 ┣ 📜 Main.java
 ┗ 📄 README.md
```

---

## 🧪 Örnek Konsol Çıktısı

```
============================================================
     HASTANE RANDEVU VE KAYIT YÖNETİM SİSTEMİ
============================================================
1. Hasta İşlemleri
2. Doktor İşlemleri
3. Randevu İşlemleri
4. Listele
0. Çıkış
============================================================
Seçiminiz: 1

--- YENİ HASTA KAYDI ---
Ad: Sude
Soyad: Sönmez
TC Kimlik No: 12345678910
Telefon: 0533-123-4567
✓ Hasta başarıyla kaydedildi!
Hasta No: 1001 | Ad Soyad: Sude Sönmez | TC: 12345678910 | Tel: 0533-123-4567
```

## 📜 Lisans
