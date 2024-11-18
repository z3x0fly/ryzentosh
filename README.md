# 🚀 AMD Ryzen Hackintosh EFI (OpenCore) 🔧

![Hackintosh Banner](https://i.hizliresim.com/8f3tu5j.jpg)

> **Teknik Uyarı:** APU ile çalıştırmak için üretilmiş bir EFI'dir. Bunu modifiye ederek harici ekran kartları ile kullanabilirsiniz. Server şeklinde kullanacak olan kullanıcılar, lütfen HDMI DUMMY cihazı ile kullanınız. 

Bu proje, AMD Ryzen işlemcilerle macOS'un gücünü bir araya getiren bir Hackintosh EFI yapılandırmasıdır. Modern OpenCore desteğiyle tasarlandı ve **stabil** bir Hackintosh deneyimi sunar.

> **Uyarı:** Hackintosh kurulumu, macOS lisans sözleşmelerine aykırı olabilir. Bu dosyayı indirerek yalnızca kişisel eğitim ve araştırma amaçlı kullandığınızı kabul etmiş olursunuz.

---

## 🖥️ **Desteklenen Donanımlar**
### **İşlemci**
- AMD Ryzen (3000, 5000 serisi ve üzeri)

### **Anakart**
- Gigabyte, ASUS, MSI (AM4 yonga setleri)

### **Grafik Kartı**
- AMD RX 500 serisi ve üzeri (NVIDIA kartlar *Pascal öncesi desteklenir*)

### **Diğer**
- RAM: Minimum 8GB
- Depolama: NVMe/SSD önerilir
- macOS sürümü: Ventura, Monterey, Big Sur

---

## 📂 **EFI İçeriği**
- **OpenCore Config:** `config.plist` optimize edilmiş ayarlarla birlikte gelir.
- **Kernel Yaması:** AMD işlemciler için gerekli yamalar.
- **Driverlar:** UEFI destekli macOS boot için gerekli tüm dosyalar.

```plaintext
EFI/
├── BOOT/
│   ├── BOOTx64.efi
├── OC/
│   ├── ACPI/
│   ├── Drivers/
│   ├── Kexts/
│   ├── Tools/
│   └── config.plist
```

## ⚙️ **Kurulum Adımları**
macOS İmajını İndirin

App Store üzerinden ya da GibMacOS ile.
USB Hazırlığı

16GB+ USB sürücüsü formatlayın (GUID + HFS+ veya APFS).
EFI Dosyasını USB'ye Kopyalayın

Bu repodaki EFI klasörünü USB'nin kök dizinine yapıştırın.
OpenCore Ayarlarını Düzenleyin

Sistem donanımınıza uygun config.plist dosyasını yapılandırın (ör. USB map).
BIOS Ayarlarını Yapın

AMD Ryzen Uyumlu BIOS Ayarları:
Above 4G Decoding: Enable
CSM: Disable
Secure Boot: Disable
XMP Profile: Enable (istenirse)
macOS Kurulumuna Başlayın

USB'den boot ederek OpenCore ekranına gelin ve macOS kurulumunu başlatın.
🛠️ Sorun Giderme
Boot Etmiyor:
config.plist içinde SMBIOS ayarlarını kontrol edin.
GPU Sorunları:
AMD Navi veya Polaris kartlar için doğru kext dosyalarını yükleyin.
Ses Çalışmıyor:
AppleALC.kext yamalarını kontrol edin.

## 🖼️ **Ekran Görüntüleri**

https://i.hizliresim.com/8f3tu5j.jpg

AMD Ryzen işlemci üzerinde macOS Ventura.

## 🌟 **Katkıda Bulunun**
EFI yapılandırmasında geliştirme yapmak veya önerilerde bulunmak için lütfen Pull Request gönderin ya da bir Issue açın.

## 🔗 Kaynaklar
Dortania OpenCore Guide
Hackintosh Forumları - OXInfo, Techolay, Technopat



## 💬 **İletişim**
Sorularınız mı var? Bana ulaşın:

Discord : 4n0nfly
Telegram : https://t.me/alorape

---

### **Nasıl Özelleştirilir?**
- Görseller: Örnek görseller yerine kendi EFI ekran görüntülerini alıp, GitHub’a yükledikten sonra URL’lerini ekleyebilirsin.
- Proje Detayları: Donanım ve macOS sürümü desteklerini kendi EFI yapılandırmana göre güncelle.
- İletişim Bilgileri: Kendi GitHub ve e-posta adresini ekle.

