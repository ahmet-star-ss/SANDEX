# SANDEX — APK Kurulum Adımları

## 1) GitHub'a yükle
Bu klasörün tamamını yeni bir GitHub reposuna push et:

```
git init
git add .
git commit -m "SANDEX ilk sürüm"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADIN/sandex.git
git push -u origin main
```

## 2) Otomatik derleme
Push işlemi sonrası GitHub reponda **Actions** sekmesine git.
"Build SANDEX APK" workflow'u otomatik çalışacak (birkaç dakika sürer).

## 3) APK'yı indir
Workflow bitince, o çalışmanın sayfasında en altta **Artifacts** kısmında
`sandex-debug-apk` dosyasını göreceksin. İndirip zip'i aç, içinden
`app-debug.apk` çıkacak.

## 4) Telefona kur
- APK'yı telefonuna aktar (Telegram'a kendine gönderebilirsin, Drive, USB vs.)
- "Bilinmeyen kaynaklardan yükleme" iznini aç (Ayarlar > Güvenlik)
- APK'ya dokun, kur.

## 5) İlk açılış
Uygulama açılınca demo modda çalışır (sağ üstteki ⚙ ayarlar ikonuna
dokunup backend URL + API token girene kadar örnek cevaplar verir).
Backend'in hazır olunca oradan bağlarsın.

## Notlar
- Bu bir **debug APK**'dır — kendi telefonuna kurman için yeterli,
  Play Store'a yüklemek için ayrı bir imzalama (release build) süreci gerekir.
- `android/` klasörü ilk workflow çalışmasında otomatik oluşturuluyor,
  onu elle oluşturman gerekmiyor.
