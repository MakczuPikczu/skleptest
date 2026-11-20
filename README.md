# CÉLA Studio — sklep z bluzami FORM 01

Statyczny sklep internetowy (HTML + CSS + JS, bez frameworków i bez budowania).
Strona główna z filmem kampanii, karta produktu, koszyk, zamówienie, O nas, Kontakt, FAQ, Dostawa i zwroty, Regulamin, Polityka prywatności.

## Struktura

```
index.html              cały sklep (style i skrypty w środku)
assets/img/             zdjęcia z Artlist (kampania, packshot)
assets/video/           film kampanii z dźwiękiem (4 s)
ARTLIST-PROMPTS.md      prompty do kolejnych zdjęć i filmów + gdzie je wstawić
```

## Publikacja na GitHub Pages

1. Utwórz nowe repozytorium na GitHubie (np. `cela-sklep`).
2. Wrzuć do niego całą zawartość tego folderu (przycisk **Add file → Upload files** albo `git push`).
3. W repozytorium wejdź w **Settings → Pages**.
4. W **Source** wybierz **Deploy from a branch**, gałąź `main`, folder `/ (root)`, zapisz.
5. Po 1–2 minutach sklep będzie dostępny pod adresem `https://<twoja-nazwa>.github.io/cela-sklep/`.

Lokalnie wystarczy otworzyć `index.html` w przeglądarce.

## Przed startem sprzedaży

- Koszyk i zamówienie działają w przeglądarce (koszyk zapisuje się w `localStorage`), ale **płatność jest demonstracyjna** — podłącz bramkę (Przelewy24, Stripe) albo przenieś sklep na Shopify / WooCommerce.
- Formularze kontaktu i newslettera nie wysyłają danych — podłącz np. Formspree lub swój system mailingowy.
- Regulamin i polityka prywatności to wzory — uzupełnij dane firmy i skonsultuj z prawnikiem.
- Kolory Kość i Grafit są symulowane filtrem CSS — podmień na prawdziwe zdjęcia (patrz `ARTLIST-PROMPTS.md`).
- Dźwięk filmu: przeglądarki często blokują dźwięk przed pierwszym kliknięciem — wtedy film gra bez dźwięku, a dźwięk włącza się po kliknięciu.
