## Acil Durum Müdahale Sistemi

## Proje Özeti
Bu projede, şehirde rastgele oluşan acil durumlara (yangın, cinayet vb.) en kısa sürede müdahale edebilecek bir sistem geliştirilmiştir.  
Çağrılar aciliyet derecesine göre önceliklendirilmektedir ve mahalle ile acil birimler arasındaki en kısa yol, **Dijkstra algoritması** ile hesaplanmaktadır.



## 🧠 Kullanılan Veri Yapıları ve Algoritmalar

### 🔹 MinHeap
- Acil durum çağrıları, olay tipine göre belirlenen öncelik puanlarıyla MinHeap yapısına eklenir.
- Bu sayede en acil olay **O(1)** zamanda alınabilir.
- Yeni çağrı ekleme ve yeniden düzenleme: **O(log n)**

### 🔹 Graph + Dijkstra Algoritması
- Mahalleler arası mesafeleri ve bağlantıları temsil eder. Tüm kenarlar çift yönlü ve ağırlıklıdır.
- **Amaç:** Mahalleden en yakın acil birimi bulmak.
- Karmaşıklık: **O((V + E) log V)**

### 🔹 Queue (FIFO)
- İşlenmiş çağrıların sırasını korur.
- Sistem geçmiş verilerin izlenebilirliğini sağlar.
- Karmaşıklık:
  - `Enqueue`: **O(1)**
  - `Dequeue`: **O(1)**

### 🔹 PriorityQueue (Dijkstra içinde)
- En kısa yolu bulurken minimum mesafeli düğümün seçilmesi için kullanılır.
- Karmaşıklık: **O(log n)**

---

## ⏱️ Zaman Karmaşıklığı Özeti

| İşlem                   | Zaman Karmaşıklığı       |
|------------------------|--------------------------|
| Çağrı oluşturma        | O(log n)                 |
| En yakın birimi bulma  | O((V + E) log V)         |
| Çağrı işleme           | O(log n)                 |
| Listeyi güncelleme     | O(n log n)               |

---

## ✅ Sonuç
Bu proje, **graph yapısı** ve **öncelikli kuyruk (MinHeap)** sayesinde gerçek zamanlı çağrı yönlendirme problemini çözmeyi amaçlar.  
Sistem, verimli çalışmakta ve **gerçek hayattaki acil durum yönetim senaryolarına uygun** olarak tasarlanmıştır.
