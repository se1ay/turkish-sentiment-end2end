# Veri Şeması

Bu klasörde iki CSV bulunur:

## cleaned_movie_data_comment.csv
Kolonlar:
- `movie_name` : Film adı (metin)
- `year` : Yayın yılı (sayısal)
- `rating` : Filmin sitedeki puanı (sayısal)
- `genre` : Tür (metin)
- `comment_text` : Yorum metni (metin)
- `comment_rating` : Yoruma verilen 1–10 arası puan (sayısal)

## processed_movie_comments.csv
Yukarıdakilere ek olarak:
- `cleaned_comment` : Temizlenmiş yorum metni (küçük harf, noktalama/emoji temizliği vb.)
- `tokens` : Token listesi (string/temsil)

### 3 sınıflı etiketleme
Notebook’larda kullanılan etiketleme kuralı:
- 0: `comment_rating < 4`
- 1: `4 <= comment_rating < 7`
- 2: `comment_rating >= 7`
