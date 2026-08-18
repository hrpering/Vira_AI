# Generative UI Spec v0.1

Bir Generative UI tarifi `type`, `version`, `title`, `inputs`, `state` ve `actions` alanlarını tanımlar. Tarifteki her alan kullanıcıya gösterilebilir veya güvenli varsayılanla doldurulabilir olmalıdır.

Render eden istemci bilmediği alanları yok saymalı, tarifi çalıştırmadan önce riskli action’lar için onay istemeli ve sonucu özgün prompt ile ilişkilendirmelidir.
