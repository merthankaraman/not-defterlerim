# Kurulum


# İlk ayarlar
```bash
git config --global user.name "Merthan KARAMAN"
git config --global user.email merth4nkaraman@gmail.com
```
<br/><br/>
Bulunan klasörde git kurulumu kontrol etmek için
```bash
git show
```
<br/><br/>
Temel komutlar
```bash
git status
git init
git log
```
<br/><br/>
Sık kullanılan komutlar
```bash
git add <file>
git commit -m "Mesaj"
git restore <file>
git diff 
```

# Detaylı ayarlar
Dallanma ayarları
```bash
git switch main
git branch
git branch feat
```
<br/><br/>
Başka düğümleri kontrol etme
```bash
git checkout <hash>
```
<br/><br/>
Commit'leri siler logda önceki kayıtlar gözükmez ama son commit'teki değişiklikleri kalır
```bash
git reset <hash>
```
<br/><br/>
Hem commit'leri hem de o commit'lerdeki değişiklileri siler
```bash
git reset --hard <hash>
```
<br/><br/>
Seçilen kaydın verileri siliniyor logları duruyor. Yani commit'i geri alıyor
```bash
git revert <hash>
```
# Rebase
Mainden ayrılıp branch'den ilerleyip arada maindeki güncellemeleri aldıktan sonra kullanıldığında arada yapılan maindeki verileri tek seferde alıp branch ile birleştirir.

```bash
git switch feat
git rebase main
```

# Uzaktan bağlantıda ayarlar
Git'in github'a bağlanması
```bash
REPO="link"
git remote add origin ${REPO}.git
git branch -M main
git push -u origin main
git pull origin main
```
<br/><br/>
Uzaktaki branchleri görmek için
```bash
git branch -r
```
<br/><br/>
Değişiklileri alıp locale getirir ve bakarız.
```bash
git fetch origin main
```
<br/><br/>
Uzaktan branch'e bakarken
```bash
git checkout origin/main
```
<br/><br/>
Değişiklikleri fetch ettikten sonra pull yaparak local repo güncellenir
```bash
git pull origin main
```
<br/><br/>
Featin main'e gelmesini istiyorsak
```bash
git switch main
git merge feat
```

# Stash
Değişen dosyaları depolamak için
```bash
git stash
```
<br/><br/>
Son dosyayı çıkarmak ve listede çıkarmak için 
```bash
git stash pop
```
<br/><br/>
Depolanan dosya isimleri görmek için
```bash
git stash list
```
<br/><br/>
Depodan istediğimiz stash kullanılmak istendiğinde
```bash
git stash apply stash@{sira}
```
