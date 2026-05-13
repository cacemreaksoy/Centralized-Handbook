# **P4V Commit Convention Kuralları**

Proje büyüdükçe "abi bu kodu kim bozdu", "şu dosyayı kim ne zaman değiştirdi" dramalarını yaşamamak ve Perforce geçmişimizi temiz tutmak için bugünden itibaren yepyeni bir commit kural seti (Convention) uyguluyoruz. 🛑

Bundan sonra Perforce üzerinden atacağınız tüm commitler bu kurallara uygun olacak. Kurala uymayan, ne idüğü belirsiz commitler gerekirse revert edilecektir. Bu disiplinin oturmaması durumunda ise Pull Request sistemine geçilecek ve atılan her commit
manuel olarak tarafımdan ayıklanarak excel'e geçirilip uygunluk durumuna göre onay verilecektir. 

# **Nasıl Commit Atıyoruz?**
Commit formatımız tek satırlık ve aşırı basit. Yapı kesinlikle şöyle olacak:
[Kategori] Kısa ve net İngilizce açıklama

#  **Zorunlu Kategori Etiketleri (Tagler)**
İşin türüne göre mesajın başına mutlaka şu taglerden birini koyuyorsunuz:

 [Art] - 3D model, animasyon ve texture eklentileri/güncellemeleri.

 [TechArt] - Shader, materyal, VFX, rig ve optimizasyon işleri.

 [Code] - C++, ana Blueprint sistemleri ve core mekanikler.

 [LD] - (Level Design) Harita, çevre düzeni ve ışıklandırma mevzuları. Level Art da bu Tag ile atabilir. 

 [UI] - Arayüz, menüler ve HUD değişiklikleri.

 [Audio] - SFX, müzik ve ses ayarları.

 [GD] Game Design ile alakalı değişiklikler; ekonomik düzeltmeler, parametre ayarları, balancing, CCC değişiklikleri.

 [DOC] Dökümantasyonla alakalı bir commit atılırsa bu tag kullanılacaktır.

 [Bugfix] - Departman fark etmeksizin acil bir patlağı/hatayı çözdüğünüz durumlar.

# 🚨** Kesinlikle Dikkat Edilecek Altın Kurallar**
1️⃣ Sadece İngilizce: Motor standartlarına uyuyoruz. Türkçe commit kesinlikle yasak.

2️⃣ Emir Kipi Kullanın: Geçmiş zamanla işimiz yok. Added, Fixed, Updated YERİNE --> Add, Fix, Update kullanıyoruz. Yaptığınız işi emir veriyormuş gibi yazın.

3️⃣ Alt Çizgi (_) Kullanmayın: Alt çizgileri sadece dosya (asset) isimlendirirken kullanın. Commit mesajı dediğin normal insan cümlesi gibi okunabilmeli. Kelimeler arasına boşluk bırakın geçin. 

4️⃣ Çöp Commit Atmayın: "test", "wip", "ufak düzeltmeler", "asdf" gibi ne olduğu belli olmayan commitler görmek istemiyoruz. Ne yaptıysan onu net bir şekilde yazacaksın. 

# **Doğru ve Yanlış Örnekler (Buraya Dikkat)**
❌ Hatalı: [Art] added_church_textures_and_meshes (Geçmiş zaman ve alt çizgi var - PATLADI 💥)
✅ Doğru: [Art] Add church exterior meshes and textures

❌ Hatalı: [TechArt] Fixed smoke material (Geçmiş zaman kullanılmış - PATLADI 💥)
✅ Doğru: [TechArt] Fix smoke material 

❌ Hatalı: ufak tefek buglar çözüldü (Tag yok, Türkçe, belirsiz - DİREKT RET ❌)
✅ Doğru: [Bugfix] Fix memory leak in enemy spawner 

❌ Hatalı: test (Bu artık kessinlikle yok zaten)
✅ Doğru: [LD] Update village lighting and post-process

Herkese kolay gelsin. 
