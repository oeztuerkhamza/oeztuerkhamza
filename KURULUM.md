# GitHub Profil Kurulum Talimatları

## Adım 1 – Profil Deposu Oluştur

GitHub'da **yeni bir depo** oluşturun:
- Depo adı (zorunlu): `oeztuerkhamza`  ← kullanıcı adınızla aynı olmalı!
- Public olarak işaretle
- README dosyasıyla birlikte başlat seçeneğini KAPATIN (biz kendi dosyamızı ekleyeceğiz)

## Adım 2 – Dosyaları Yükle

Bu klasördeki tüm dosyaları oluşturduğunuz depoya atın:

```powershell
# GitHub-Profile klasörüne gidin
cd "C:\Users\hamza\Desktop\Lebenslauf\GitHub-Profile"

# Git başlat
git init
git branch -M main

# Remote ekle (oeztuerkhamza yerine kendi kullanıcı adınız)
git remote add origin https://github.com/oeztuerkhamza/oeztuerkhamza.git

# Dosyaları ekle ve commit et
git add .
git commit -m "feat: profil README ve snake animasyonu eklendi"

# Push et
git push -u origin main
```

## Adım 3 – GitHub Actions İzni Ver

Depo ayarlarından Actions'ın yazma iznine sahip olduğundan emin olun:

1. Depo → **Settings** → **Actions** → **General**
2. "Workflow permissions" bölümünde **"Read and write permissions"** seçin
3. **Save** butonuna tıklayın

## Adım 4 – Snake Animasyonunu Manuel Tetikle

İlk kez animasyonu oluşturmak için:

1. Depo → **Actions** sekmesi
2. Sol taraftan **"Generate Snake Animation"** workflow'unu seçin
3. **"Run workflow"** butonuna tıklayın
4. Birkaç dakika bekleyin – `output` branch'ında SVG dosyaları oluşacak

## Adım 5 – Profili Görüntüle

[github.com/oeztuerkhamza](https://github.com/oeztuerkhamza) adresine gidin ve profilinizi görün! 🎉

---

## Dosya Yapısı

```
oeztuerkhamza/          ← depo ismi
├── README.md           ← profil sayfasında gösterilen içerik
└── .github/
    └── workflows/
        └── snake.yml   ← her gece otomatik snake animasyonu üretir
```

## Sorun Giderme

| Sorun | Çözüm |
|-------|-------|
| Snake SVG görünmüyor | Actions çalıştı mı kontrol et; `output` branch'ının oluştuğundan emin ol |
| Stats yüklenmiyor | github-readme-stats bazen yavaş olabilir; birkaç dakika bekle |
| Workflow başarısız | Settings > Actions > General > "Read and write permissions" seçilmiş mi? |
