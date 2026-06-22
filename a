* Riot Games Yetkilendirme (Authorize) Adresi:
- URL: https://auth.riotgames.com/authoriz...":null,"email_verified":null,"country":null}}
- Metot: GET
- Aciklama: Giris akisini baslatir ve access_token / id_token alir.

* Entitlements Token API:
- URL: https://entitlements.auth.riotgames.com/api/token/v1
- Metot: POST
- Aciklama: Diger Valorant envanter API'lerine erismek icin gereken yetkilendirme anahtarini (entitlements_token) uretir.

* User Info (Kullanici Bilgileri) API:
- URL: https://auth.riotgames.com/userinfo
- Metot: GET
- Aciklama: Kullanicinin PUUID, Riot ID, etiket (tag), e-posta ve telefon dogrulama durumlarini doner.

* Bolge / Affinity Tespit API:
- URL: https://riot-geo.pas.si.riotgames.com/pas/v1/service/valorant
- Metot: GET
- Aciklama: Hesabin hangi cografi bolgede (EU, NA, AP vb.) bulundugunu ogrenmek icin kullanilir.

* Account XP (Level) API:
- URL: https://pd.{shard}.a.pvp.net/account-xp/v1/players/{puuid}
- Metot: GET
- Aciklama: Hesabin Valorant oyuncu seviyesini (level) ceker. ({shard} = eu, na, ap vb.)

* Cuzdan (Wallet - VP &amp; RP) API:
- URL: https://pd.{shard}.a.pvp.net/store/v1/wallet/{puuid}
- Metot: GET
- Aciklama: Hesaptaki Valorant Puani (VP) ve Radyanit Puani (RP) bakiyelerini sorgular.

* Envanter (Skin Sayisi) API:
- URL: https://pd.{shard}.a.pvp.net/store/v1/entitlements/{puuid}/e7c63390-eda7-46e0-bb7a-a6abdacd2433
- Metot: GET
- Aciklama: e7c63390-eda7-46e0-bb7a-a6abdacd2433 (silah kaplamasi envanteri) kimligini sorgulayarak hesapta kac adet skin bulundugunu listeler.

* MMR / Rank API:
- URL: https://pd.{shard}.a.pvp.net/mmr/v1/players/{puuid}
- Metot: GET
- Aciklama: Hesabin guncel rankini, peak (en yuksek) rankini ve rank puanini (RR) getirir.

* Kisitlamalar / Kalici Ban Kontrol API:
- URL: https://riot-geo.pas.si.riotgames.com/restrictions/v3/player
- Metot: GET
- Aciklama: Hesap uzerindeki aktif kalici ban engellemelerini kontrol eder.

------------------------------------------------------------
2. CAPTCHA COZUCU API'LERI (HCAPTCHA BYPASS)
------------------------------------------------------------
Riot Games giris ekraninda cikan hCaptcha engelini gecmek icin
entegre edilmis bulut ve yerel cozucu servisleridir.

A. Bulut Servisi (YesCaptcha)
* YesCaptcha Gorev Olusturma:
- URL: https://api.yescaptcha.com/createTask
- Metot: POST
- Aciklama: hCaptcha gorsellerini ve soruyu YesCaptcha servisine gondererek cozdurur.

B. Yerel Yapay Zeka / GPU Solver (CLIP + OpenCV)
Lokalde (localhost:8000) calisan FastAPI tabanli yapay zeka modelidir.
* Canvas Sekil Eslesmesi Cozucu:
- URL: http://127.0.0.1:8000/api/solve-canvas-shapes
- Metot: POST
- Aciklama: Surukle-birak veya eslesme bulma tarzi hCaptcha bulmacalarini OpenCV ile cozer.

* Grid Ekran Goruntusu Cozucu:
- URL: http://127.0.0.1:8000/api/solve-grid-screenshot
- Metot: POST
- Aciklama: 3x3 veya 4x3 tek parca resimleri bolerek dogru tiklanacak kareleri tespit eder.

* Standart Resim Siniflandirici:
- URL: http://127.0.0.1:8000/api/solve
- Metot: POST
- Aciklama: Ayri ayri ayiklanmis resimleri, verilen sorunun ingilizce karsiligi ile CLIP modeline gonderip cozer.

------------------------------------------------------------
3. TARAYICI / CDP (Chrome DevTools Protocol) PORT API'SI
------------------------------------------------------------
* Chrome DevTools WebSocket Tespit API:
- URL: http://localhost:{port}/json/version
- Metot: GET
- Aciklama: Tarayici oturumunun CDP WebSocket debugger adresini cekerek, yuklenen hCaptcha resimlerinin URL'lerini yakalar.
============================================================
