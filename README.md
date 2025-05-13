Proje Adı: Acil Durum Müdahale Sistemi
1. Proje Özeti
 
Bu projede, şehirde rastgele oluşan acil durumlara (yangın, cinayet vb.) en kısa sürede müdahale edebilecek bir sistem geliştirildi. Çağrılar aciliyet derecesine göre önceliklendirildi ve mahalle ile acil birimler arası en kısa yol, Dijkstra algoritması ile hesaplandı.
3. Kullanılan Veri Yapıları ve Algoritmalar
MinHeap : Olaylara ait çağrılar, olay tipine göre belirlenen öncelik puanlarıyla MinHeap veri yapısına eklenir. Bu yapı sayesinde en acil olay O(1) zamanda alınabilirken yeni bir çağrı eklemek veya çıkarılanı yeniden düzenlemek O(log n) zamanda gerçekleşir. Bu, zaman açısından verimli bir önceliklendirme yapar.
Graph + Dijkstra : Mahalleler arası mesafeleri ve bağlantıları temsil etmek için kullanılır. Her kenar çift yönlüdür ve mesafe ağırlıkları içerir. Bu graph, mahalleler arasında dinamik yönlendirme yapılabilmesini sağlar.Dijkstra algoritması ile en yakın acil birim bulundu. Karmaşıklık: O((V + E) log V)
Queue (FIFO) : Bu yapı, işlenmiş acil çağrıların sırasını korumak için kullanılır. FIFO (First In First Out) mantığıyla çalışır.Bu durum, geçmiş çağrıları takip etmek veya raporlama yapmak isteyen bir sistem için önemlidir. Karmaşıklık: Enqueue , Dequeue: O(1)
PriorityQueue (Dijkstra içinde): Minimum mesafeli düğüm seçimi için kullanıldı. Karmaşıklık: O(log n)

4. Zaman Karmaşıklığı Özeti
İşlem	Zaman Karmaşıklığı
Çağrı oluşturma	O(log n)
En yakın birimi bulma	O((V + E) log V)
Çağrı işleme	O(log n)
Listeyi güncelleme	O(n log n)
5. Sonuç
Proje, graph yapısı ve öncelikli kuyruk sayesinde gerçek zamanlı çağrı yönlendirme sorununa çözüm sunar. Tüm işlemler başarılı şekilde gerçekleştirilmiş olup sistem, gerçek hayata uygundur.

Enes Emre Turan	032390083
Hakan Dargalı		032390087
Sezer Okan Gölge	032390089
Selsabil Aya Belkabla	032390092
Ravan Novruzov	032390095
