<a id="top"></a>

<div align="center">

# 🔍 Rəqəmsal Kriminalistika

**Digital Forensics · İmtahana hazırlıq qeydləri**

![Language](https://img.shields.io/badge/Language-Az%C9%99rbaycanca-0B7285?style=flat-square) ![Questions](https://img.shields.io/badge/%C4%B0mtahan_suallar%C4%B1-14-1D4ED8?style=flat-square) ![Topics](https://img.shields.io/badge/M%C3%B6vzu-4-475569?style=flat-square)

*4 mühazirə əsasında hazırlanmış 14 sualın xülasəsi*

</div>

---

> [!NOTE]
> Bu material dərs mühazirələrinə əsaslanan **imtahan konspektidir**; hüquqi və texniki praktika üçün ayrıca aktual mənbələr yoxlanmalıdır.

## 📚 Mündəricat

- [**01.** Rəqəmsal kriminalistika nədir? Fərqlər və sahələri](#sual-1)
- [**02.** Məqsədləri və əsas prinsipləri](#sual-2)
- [**03.** Hüquqi çərçivə və mərhələlər](#sual-3)
- [**04.** Rəqəmsal sübut anlayışı, xüsusiyyətləri, formaları və təsnifatı](#sual-4)
- [**05.** Sübutların qəbul edilmə şərtləri, standartlar və səbəblər](#sual-5)
- [**06.** Rəqəmsal sübutların qorunma prinsipləri](#sual-6)
- [**07.** Fayl sisteminin funksiyaları və struktur elementləri](#sual-7)
- [**08.** Faylın komponentləri, tipləri, loji və fiziki aspektləri](#sual-8)
- [**09.** Windows və Linux fayl sistemləri, icazələr](#sual-9)
- [**10.** Disk image anlayışı və forensic imaging prinsipləri](#sual-10)
- [**11.** Disk image formatları](#sual-11)
- [**12.** Imaging metodları](#sual-12)
- [**13.** Forensic imaging alətləri](#sual-13)
- [**14.** Imaging çətinlikləri, standartlar, tövsiyələr](#sual-14)
- [⚡ İmtahandan əvvəl sürətli təkrar](#tekrar)

---

## 🗂️ Mühazirə bölgüsü

| Mühazirə | Suallar |
|:--|:--:|
| Rəqəmsal kriminalistika anlayışı, məqsədləri və hüquqi çərçivəsi | 1–3 |
| Rəqəmsal sübut anlayışı, qəbul edilməsi və qorunması | 4–6 |
| Fayl sistemləri və yaddaş strukturları | 7–9 |
| Disk image və forensic imaging | 10–14 |

---

<a id="sual-1"></a>

## 1. Rəqəmsal kriminalistika nədir? Fərqlər və sahələri

Rəqəmsal kriminalistika (Digital Forensics) — rəqəmsal cihazlarda, sistemlərdə və şəbəkələrdə məlumatların toplanması, qorunması, təhlili və hüquqi sübut kimi təqdim olunması ilə məşğul olan elm və tətbiqi fəaliyyət sahəsidir.

| Ənənəvi kriminalistika | Rəqəmsal kriminalistika |
|:--|:--|
| Qan, silah, barmaq izi kimi fiziki sübutlar | Loglar, e-mail və fayllar kimi elektron sübutlar |
| Sübutlar gözlə görünə bilər | Sübutlar gizli və ya silinmiş ola bilər |
| Hadisə yeri fiziki məkandır | Hadisə yeri kompüter, server, mobil cihaz ola bilər |
| Dəyişdirmək nisbətən çətindir | Saniyələr içində dəyişdirilə və silinə bilər |

- Computer Forensics — kompüter, disk və fayllar.
- Mobile Forensics — telefon, SMS, GPS və tətbiq məlumatları.
- Network Forensics — trafik, PCAP, firewall logları.
- E-mail və sosial media kriminalistikası — phishing, saxta hesablar, mesajlar.
- Cloud Forensics — AWS, Azure, Google Cloud.
- Malware Forensics — virus, trojan, ransomware.
- Əlavə istiqamətlər: IoT və kibertibbi kriminalistika.

<a id="sual-2"></a>

## 2. Məqsədləri və əsas prinsipləri

**Məqsədlər:** sübutların aşkarlanması, silinmiş və gizlədilmiş məlumatların bərpası, dəyişdirilmədən qorunması, hadisənin rekonstruksiyası, hücumun mənbəyinin müəyyənləşdirilməsi və nəticələrin məhkəməyə etibarlı təqdimatı.

- Integrity — sübutun bütövlüyü.
- Chain of Custody — sübutun kim tərəfindən, nə vaxt və necə götürüldüyünün qeydiyyatı.
- Minimal Intervention — minimum müdaxilə.
- Documentation — hər əməliyyatın sənədləşdirilməsi.
- Legal Compliance — hüquqi prosedurlara əməl edilməsi.
- Repeatability — araşdırmanın təkrarlana bilməsi.

<a id="sual-3"></a>

## 3. Hüquqi çərçivə və mərhələlər

Hüquqi çərçivə sübutların qanuni əldə edilməsi, qorunması və məhkəmədə istifadəsini tənzimləyir. Mühazirədə Azərbaycan Respublikasının Cinayət Məcəlləsi, elektron imza və elektron sənəd haqqında qanun, kibertəhlükəsizliklə bağlı aktlar, ISO/IEC 27037 və NIST tövsiyələri qeyd olunur.

1. Hadisə yerinin qorunması.
2. Sübutların toplanması.
3. Sübutların qorunması və daşınması.
4. Təhlil və araşdırma.
5. Hadisələrin rekonstruksiyası.
6. Hesabatın hazırlanması.
7. Sübutların təqdimatı və müdafiəsi.

---

<a id="sual-4"></a>

## 4. Rəqəmsal sübut anlayışı, xüsusiyyətləri, formaları və təsnifatı

Rəqəmsal sübut (Digital Evidence) — kompüter, mobil cihaz, şəbəkə və digər elektron vasitələrdə saxlanılan, hüquqi prosesdə istifadə oluna bilən rəqəmsal izdir.

**6 xüsusiyyəti:** qeyri-maddi xarakter, kövrəklik, asan kopyalanma, çoxlaynlıq (müxtəlif cihazlarda mövcudluq), müvəqqəti məlumatlar (RAM), metadata.

1. Fayl sistemi sübutları — PDF, Word, şəkil, silinmiş fayllar.
2. Sistem sübutları — Windows Event Log, Linux Syslog.
3. Şəbəkə sübutları — IP, PCAP, DNS, e-mail başlıqları.
4. Mobil sübutlar — SMS, GPS, zəng qeydləri.
5. Bulud sübutları — iCloud, Google Drive, sosial media.
6. IoT sübutları — ağıllı saat, kamera, avtomobil GPS-i.

**Təsnifat:** mənşəyinə görə — birbaşa və dolayısı; qanuni statusuna görə — ittiham və müdafiə; əldə edilməsinə görə — fiziki daşıyıcı, onlayn və texniki cihazlardan çıxarılan.

**Mənbələr:** kompüterlər, mobil telefonlar, serverlər, routerlər, sosial media, e-mail, bulud, CCTV və IoT.

<a id="sual-5"></a>

## 5. Sübutların qəbul edilmə şərtləri, standartlar və səbəblər

1. Relevance — hadisə ilə əlaqəli olması.
2. Integrity & Authenticity — dəyişdirilməməsi və həqiqiliyi; hash ilə yoxlama.
3. Reliability — etibarlı metod və prosedurlar.
4. Legality — qanuni əldə edilmə.

**Standartlar və mənbələr:** Federal Rules of Evidence (ABŞ), Avropa İnsan Hüquqları Məhkəməsi yanaşmaları, Budapeşt Konvensiyası (2001), ISO/IEC 27037:2012.

**Qəbul edilməmənin səbəbləri:** qanunsuz əldə edilmə, orijinalın dəyişdirilməsi/silinməsi, Chain of Custody pozuntusu, qeyri-peşəkar metodlar.

<a id="sual-6"></a>

## 6. Rəqəmsal sübutların qorunma prinsipləri

> [!IMPORTANT]
> **Əsas fikir: “Orijinala toxunma, yalnız nüsxə ilə işlə.”**

1. Chain of Custody — hər təhvil-təslimin qeydiyyatı.
2. Orijinal və nüsxə — təhlil surət üzərində aparılır.
3. Hashing — SHA-256 ilə bütövlük yoxlanır.
4. Təhlükəsiz saxlanma — evidence locker, şifrələnmiş disk.
5. Qanuni prosedurlara riayət.
6. Minimal müdaxilə.
7. Standart metod və forensic alətlərdən istifadə.

---

<a id="sual-7"></a>

## 7. Fayl sisteminin funksiyaları və struktur elementləri

Fayl sistemi — yaddaş qurğularında məlumatları təşkil edən, idarə edən və onlara giriş imkanı verən proqram–məlumat kompleksidir.

1. Məlumatların təşkili — qovluq iyerarxiyası.
2. İdentifikasiya — ad, path, inode, MFT.
3. Girişin idarə edilməsi — Read, Write, Execute.
4. Bütövlüyün qorunması — journaling, snapshot, checksum.
5. Disk sahəsinin idarə edilməsi — boş və dolu bloklar.

**Struktur elementləri:** File, Directory, Path (mütləq və nisbi), Metadata, Identifier (inode/MFT). Əlavə daxili strukturlar: Superblock və Data Blocks.

<a id="sual-8"></a>

## 8. Faylın komponentləri, tipləri, loji və fiziki aspektləri

**Faylın 2 əsas komponenti:** Metadata — ad, növ, ölçü, tarix, sahiblik, icazələr; Content — disk bloklarında saxlanılan real məlumat.

- Mətn: .txt, .csv, .log; ikili: .exe, .bin, .jpg.
- Sistem: kernel32.dll, /bin/bash; istifadəçi faylları: sənədlər və şəkillər.
- Müvəqqəti və daimi fayllar.
- Multimedia: .mp3, .mp4, .png; arxiv: .zip, .rar, .tar.gz.
- Verilənlər bazası: .db, .sql, .mdb.

Loji aspekt — faylın adı, yolu, ölçüsü, icazələri və metadata-sı. Fiziki aspekt — faylın yaddaş daşıyıcısındakı bloklarda yerləşməsi.

<a id="sual-9"></a>

## 9. Windows və Linux fayl sistemləri, icazələr

| Windows | Xüsusiyyəti |
|:--|:--|
| FAT | Sadə, ayrıca icazə sistemi yoxdur |
| FAT32 | Maksimum 4 GB fayl; portativ disklər |
| NTFS | Journaling, ACL, EFS, böyük fayllar |

| Linux | Xüsusiyyəti |
|:--|:--|
| EXT2 | Journaling yoxdur |
| EXT3 | Journaling əlavə edilib |
| EXT4 | Təkmilləşdirilmiş journaling, performans |
| XFS | Böyük fayllar və serverlər |
| Btrfs | Copy-on-Write, snapshot, rollback |
| ZFS | Checksumming, snapshot |

**Windows:** ACL icazələri — Read, Write, Execute, Modify, Full Control. EFS — fayl şifrələmə; BitLocker — disk şifrələmə; Audit Policies — fəaliyyətin izlənməsi.

**Linux:** Owner, Group, Others üçün r (4), w (2), x (1). 755 = rwxr-xr-x; 644 = rw-r--r--. Əlavələr: ACL, SELinux, AppArmor, LUKS.

---

<a id="sual-10"></a>

## 10. Disk image anlayışı və forensic imaging prinsipləri

Disk image — HDD, SSD, USB kimi qurğuların bit-by-bit surətidir. Tam fiziki surət mövcud faylları, əlçatan boş sektorları, silinmiş məlumat qalıqlarını, slack space və fayl sistemi strukturlarını əhatə edə bilər.

**Üstünlükləri:** orijinalın qorunması, analizin rahatlığı, təkrar yoxlama, silinmiş məlumatların bərpa imkanı.

1. Orijinala toxunmamaq.
2. Bit-by-bit surət.
3. Hash təsdiqləmə (MD5, SHA-1, SHA-256).
4. Chain of Custody.
5. Write Blocker.
6. İzolyasiya olunmuş qorunan mühit.
7. Fiziki etiketləmə.

<a id="sual-11"></a>

## 11. Disk image formatları

| Format | Üstünlüyü | Məhdudiyyəti |
|:--|:--|:--|
| RAW (.dd) | Sadə və universal | Sıxılma və əlavə metadata yoxdur |
| E01 | Metadata, hash, hissələrə bölünmə | Proprietary format |
| AFF | Açıq format, metadata və sıxılma | Nisbətən az yayılıb |

**Digər formatlar:** SMART — köhnə forensic format; DMG — macOS; ISO — CD/DVD. Yadda saxla: RAW — sadə; E01 — metadata; AFF — açıq format.

<a id="sual-12"></a>

## 12. Imaging metodları

1. Physical Imaging — bütün əlçatan sektorlar, o cümlədən boş sahələr və slack space; geniş sübut dəsti, çox resurs tələb edir.
2. Logical Imaging — fayl sistemində görünən fayl və qovluqlar; sürətlidir, boş sektorları əhatə etmir.
3. Targeted Imaging — konkret seçilmiş fayl və qovluqlar; digər sübutlar nəzərdən qaça bilər.
4. Live Imaging — sistem işləyərkən; aktiv proseslər haqqında məlumat, dəyişiklik riski var.
5. Memory Imaging — RAM surəti; proseslər, şifrələmə açarları və bağlantılar; söndürüləndə məlumat itir.

<a id="sual-13"></a>

## 13. Forensic imaging alətləri

| Alət | İstifadəsi |
|:--|:--|
| FTK Imager | GUI, RAW/E01, hash, önizləmə |
| dd | Linux CLI, bit-by-bit surət |
| dcfldd | dd bazasında hash və log |
| Guymager | GUI, RAW/E01 |
| EnCase | Kommersiya forensic mühit |
| X-Ways Forensics | Disk, bərpa, metadata analizi |
| Magnet AXIOM | Disk, mobil və bulud təhlili |

**Mühazirədəki komanda nümunəsi:**

```bash
dd if=/dev/sda of=/mnt/evidence/disk_image.dd bs=4M conv=noerror,sync
```

if — mənbə; of — çıxış; bs — blok ölçüsü; conv=noerror,sync — oxuma xətasında davam etmək və blok ölçüsünü saxlamaq. Real sübutlarda disk seçimi və yazmadan qoruma ayrıca təmin edilməlidir.

<a id="sual-14"></a>

## 14. Imaging çətinlikləri, standartlar, tövsiyələr

1. Böyük disklər — vaxt və saxlanma yükü; image-i hissələrə bölmək mümkündür.
2. Şifrələmə — BitLocker və FileVault; qanuni açar əldə edilməsi və uyğun hallarda Live Imaging.
3. SSD TRIM — silinmiş məlumat bərpasını çətinləşdirir; bərpa zəmanətli deyil.
4. Əlavə çətinlik — uzaqdan, şəbəkə vasitəsilə image çıxarma.

**Standartlar:** ISO/IEC 27037 — sübutun əldə olunması və qorunması; NIST SP 800-101 — mobil cihaz kriminalistikası. Tövsiyələr: planlama, orijinalın qorunması, hash yoxlaması, Chain of Custody və sənədləşdirmə.

---

<a id="tekrar"></a>

## ⚡ İmtahandan əvvəl sürətli təkrar

6 əsas kriminalistika sahəsi • 7 mərhələ • 6 sübut xüsusiyyəti • 6 sübut forması • 4 qəbul şərti • 7 qorunma prinsipi • 5 fayl sistemi funksiyası • 2 fayl komponenti • 3 əsas image formatı • 5 imaging metodu.

> [!TIP]
> Integrity — bütövlük; Chain of Custody — təhvil-təslim tarixçəsi; Physical — sektor surəti; Logical — fayl və qovluqlar; Live — işlək sistem; Memory — RAM surəti.

---

<div align="center">

**Məqsəd:** əsas anlayışları sürətli təkrar etmək və imtahana hazırlaşmaq.

[⬆️ Yuxarı qayıt](#top)

</div>
