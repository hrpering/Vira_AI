# Mimari genel bakış

Vira ekosistemi şu akışla düşünülür:

`İstek → bağlam → model/proje seçimi → routing → çalışma yüzeyi → doğrulama → kalıcı çıktı`

Model katmanı üretim yapar; Studio veya workflow katmanı adımları yönetir; Generative UI sonucu görev için uygun bir yüzeye dönüştürür; Projects ve Outputs bağlamı taşır; distributed inference ise kapasite ve çalışma yerleşimini destekler.

Bu ayrım, tek bir model adını ürünün tamamıymış gibi sunmayı önler.
