Cilt Hastalıklarının Yapay Zeka ile Sınıflandırılması
Bu proje, yapay zeka ve derin öğrenme yöntemlerini kullanarak cilt hastalıklarının görseller üzerinden sınıflandırılması üzerine odaklanmıştır. Proje kapsamında psoriasis (sedef), chickenpox (su çiçeği), acne (akne), vitiligo ve nevus (hastalıklı ben) gibi beş farklı cilt hastalığı ele alınmıştır. Transformer tabanlı modern modellerin gücünden yararlanılarak, bu hastalıkların doğru şekilde sınıflandırılması amaçlanmıştır.

Proje Hedefleri
Beş farklı cilt hastalığına ait veri seti oluşturmak ve işlemek.
Farklı derin öğrenme modellerini uygulayarak performanslarını karşılaştırmak.
Klinik uygulamalar ve akademik araştırmalara katkı sağlayacak bir yapay zeka çözümü geliştirmek.
Veri Hazırlama
Görseller, çeşitli kaynaklardan toplanarak veri seti oluşturulmuştur.
Görsellerin tekrarlı olmaması için hash değerleri kullanılmış ve veri seti temizlenmiştir.
Veri seti, modellerin daha iyi öğrenmesini sağlamak için veri artırma (data augmentation) yöntemleri ile zenginleştirilmiştir.
Veri seti, %80 eğitim ve %20 doğrulama oranında ikiye bölünmüştür.
Kullanılan Modeller
Projede aşağıdaki transformer tabanlı modeller kullanılmıştır:

DeiT-Small-Patch16-224
Swin-Tiny-Patch4-Window7-224
BEiT-Base-Patch16-224
CaiT-S24
MobileViT-S
Her model, PyTorch, TIMM ve Hugging Face kütüphaneleri kullanılarak eğitilmiştir. Model performansları, doğruluk (accuracy), duyarlılık (recall), kesinlik (precision), F1 skoru ve AUC (Area Under Curve) gibi metriklerle detaylı bir şekilde değerlendirilmiştir.

Eğitim ve Test Süreci
Eğitim, Google Colab platformunda gerçekleştirilmiş ve GPU kaynakları optimize edilmiştir.
Eğitim sırasında en iyi model ağırlıkları düzenli olarak kaydedilerek bağlantı kesintisi gibi sorunlara karşı önlem alınmıştır.
Test sonuçları, özellikle NEVUS ve CHCPOX sınıflarında modelin yüksek doğruluk ve dengeli performans gösterdiğini ortaya koymuştur.
Öne Çıkan Sonuçlar
NEVUS ve VITILIGO sınıflarında en yüksek doğruluk oranları elde edilmiştir.
Eğitim ve doğrulama kayıpları, modelin istikrarlı ve dengeli bir şekilde optimize edildiğini göstermektedir.
ROC eğrileri ve AUC skorları, tüm modellerin güçlü bir sınıflandırma performansı sunduğunu kanıtlamıştır.
Sorunlar ve Çözümler
Eğitim Süresinin Uzunluğu: Eğitim sırasında en iyi model ağırlıkları kaydedilerek süre optimize edilmiştir.
Bağlantı Kesintileri: Google Drive'a düzenli kayıt yapılarak eğitim kaldığı yerden devam ettirilmiştir.
GPU Kaynaklarının Kısıtlılığı: Google Colab Pro veya alternatif bulut platformları değerlendirilmiştir.
Kullanılan Teknolojiler
Programlama Dili: Python
Kütüphaneler: PyTorch, TIMM, NumPy, Matplotlib, Seaborn, Pillow
Platform: Google Colab
Gelecek Çalışmalar
Daha geniş bir veri seti ile modellerin performansını artırmak.
Farklı model mimarilerini entegrasyonuna yönelik çalışmalar yapmak.
Gerçek zamanlı uygulamalar için modellerin daha fazla optimize edilmesi.
Bu proje, yapay zeka ve sağlık alanındaki kesişim noktalarını vurgulayarak, cilt hastalıklarının teşhisinde yenilikçi bir yaklaşım sunmaktadır. Proje sonuçlarının, sağlık teknolojilerinde gelecekteki çalışmalara katkı sağlaması hedeflenmektedir.
