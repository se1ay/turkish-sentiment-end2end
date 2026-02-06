# Türkçe Duygu Analizi – Uçtan Uca Boru Hattı ve Model Karşılaştırması

Bu depo; Türkçe film yorumlarından duygu analizi için uçtan uca bir veri toplama + ön işleme + modelleme akışını ve
üç farklı model ailesinin (RNN, LSTM, BERT tabanlı dönüştürücü) karşılaştırmasını içerir.

## Klasör yapısı
- `notebooks/` : Projedeki Jupyter notebook’lar
- `data/` : Çalışmada kullanılan CSV dosyaları
- `reports/` : Üretilen çıktılar/özetler

## Notebooklar
- `scrape_comments.ipynb` : Web kazıma ile film/yorum toplama ve CSV üretimi
- `LSTM.ipynb` : Keras ile LSTM tabanlı duygu sınıflandırma
- `RNN_RUN.ipynb` : PyTorch tabanlı RNN/LSTM mimarisi ile sınıflandırma (tokenize + eğitim + değerlendirme)
- `BERT_traintestgrafik.ipynb` : `dbmdz/bert-base-turkish-cased` ile Transformer tabanlı sınıflandırma
- `dbmdztraintestgrafikensonhali.ipynb`, `traintestdbmdz-bert-case .ipynb` : BERT denemeleri / varyantlar

## Veri
`data/cleaned_movie_data_comment.csv` ve `data/processed_movie_comments.csv` için şema:
- `data/DATA_SCHEMA.md`


## Çalıştırma notları
- `scrape_comments.ipynb` Selenium kullandığı için Chrome/Chromedriver kurulu bir ortam ister.
- Notebook’larda bazı dosya yolları  (`/thelinkof/...`) üzerinden geçiyor. Yerelde çalıştırırken bu yolları `data/...` olacak şekilde güncellemeniz gerekir.
