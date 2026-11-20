# CÉLA — prompty do Artlist (zdjęcia i wideo)

Dwa zdjęcia są już wygenerowane w Artlist (Flux 2.0 Pro) i podpięte w sklepie:

| Plik | Co przedstawia | Gdzie w sklepie |
|---|---|---|
| `assets/img/hero-campaign.jpg` | Para modeli w seledynowych FORM 01, kamienny dziedziniec | Hero (poster wideo), kampania, kadry „na modelce/modelu”, O nas |
| `assets/img/product-front.jpg` | Packshot bluzy na ghost-mannequin, beżowe tło | Karta produktu, sklep, koszyk, zbliżenia detali |

Kolory Kość i Grafit są na razie symulowane filtrem CSS na packshocie. Po wygenerowaniu prawdziwych zdjęć podmień pliki (patrz tabela na końcu).

---

## 1. Blokada stylu (dopisuj do KAŻDEGO promptu)

Żeby bluza wyglądała identycznie na wszystkich materiałach, dodawaj na końcu promptu ten blok bez zmian:

```
PRODUCT LOCK: the CÉLA FORM 01 hoodie — heavyweight oversized hoodie in pale celadon green (soft seledyn, approx #BFD6C4), boxy fit, dropped shoulders, slightly cropped length, thick double-layer hood with NO drawstrings and no eyelets, flat-sewn kangaroo pocket, wide 9 cm ribbed cuffs and hem, brushed 480gsm organic cotton loopback with matte surface. No text, no logos, no prints, no labels visible.
LOOK LOCK: Scandinavian luxury streetwear campaign, soft diffused natural light, muted palette of celadon, off-white, sand beige and graphite, medium-format look, subtle film grain, natural skin texture with pores, real professional fashion photography, not CGI, not plastic.
```

Wskazówka: w Artlist najlepiej utwórz **Style Kit „CÉLA”** i dodaj do niego oba istniejące zdjęcia jako referencje oraz paletę (#CFE5D3, #5E9E7B, #F6F4EF, #ECE5D8, #141615, #3B403D). Wtedy każda generacja automatycznie trzyma wygląd bluzy.

---

## 2. Zdjęcia produktowe

**P1 — tył** → `assets/img/product-back.jpg` (3:4)
```
Premium e-commerce studio product photograph, portrait 3:4. The FORM 01 hoodie shown from the BACK on an invisible ghost mannequin, hood lying naturally on the shoulders, centered on seamless warm off-white paper background (#F5F3EE), very soft shadow below. Large softbox from upper left, crisp fabric detail. [PRODUCT LOCK] [LOOK LOCK]
```

**P2 — Kość** → `assets/img/product-front-kosc.jpg` (3:4) — prompt jak packshot przodu, kolor: `bone off-white (#E9E5DC)` zamiast celadon.

**P3 — Grafit** → `assets/img/product-front-grafit.jpg` (3:4) — kolor: `deep graphite (#3E423F)`.

**P4 — makro dzianiny** → `assets/img/detail-fabric.jpg` (1:1)
```
Extreme macro photograph of brushed heavyweight cotton loopback fabric in pale celadon green, showing the soft brushed inner side folded over the smooth outer face, individual loops visible, raking side light, shallow depth of field. [LOOK LOCK]
```

**P5 — kaptur** → `assets/img/detail-hood.jpg` (4:5)
```
Close-up product detail photograph of the double-layer hood of the FORM 01 hoodie, showing the thick clean hood edge with no drawstrings and the neat flat seam where hood meets neckline, on off-white paper background, soft side light. [PRODUCT LOCK] [LOOK LOCK]
```

**P6 — szwy i ściągacz** → `assets/img/detail-cuff.jpg` (4:5)
```
Close-up detail of the wide ribbed cuff and flatlock seams of the FORM 01 hoodie sleeve, cuff resting on a pale limestone surface, soft natural window light. [PRODUCT LOCK] [LOOK LOCK]
```

**P7 — kampanijny still-life** → `assets/img/still-life.jpg` (4:5)
```
Luxury fashion campaign still life: the FORM 01 hoodie neatly folded on a block of pale travertine stone, a single sprig of eucalyptus beside it, warm off-white background, long soft shadow from low morning sun. [PRODUCT LOCK] [LOOK LOCK]
```

---

## 3. Sesje z modelkami i modelami (AI)

Różnorodność: różne wzrosty, sylwetki, typy urody i wiek 20–35. Zawsze naturalnie, bez przesadnego makijażu.

**M1 — studio, modelka** → `assets/img/model-studio-w.jpg` (3:4)
```
Full-length fashion campaign portrait of a young woman with natural curly hair and medium-brown skin, 172 cm, wearing the FORM 01 hoodie with off-white wide-leg trousers and white leather sneakers, standing relaxed with hands in the kangaroo pocket, in a minimalist photo studio with a seamless sand-beige backdrop and a single large soft key light. Calm, confident, candid. [PRODUCT LOCK] [LOOK LOCK]
```

**M2 — studio, model plus-size** → `assets/img/model-studio-m.jpg` (3:4)
```
Full-length fashion campaign portrait of a broad-shouldered man with a short beard, larger build, wearing the FORM 01 hoodie in size XXL with graphite relaxed trousers, sitting on a low travertine block in a minimalist studio with a seamless off-white backdrop, soft top light. Natural, warm expression. [PRODUCT LOCK] [LOOK LOCK]
```

**M3 — miasto** → `assets/img/model-city.jpg` (4:5)
```
Street style fashion campaign photograph of a young East Asian woman with a sleek bob walking across an empty modernist concrete plaza at blue hour, FORM 01 hoodie with the hood up, beige trench coat over one arm, motion in the stride, 35mm lens, shot from a slightly low angle. [PRODUCT LOCK] [LOOK LOCK]
```

**M4 — lifestyle, naturalne światło** → `assets/img/model-lifestyle.jpg` (3:2)
```
Lifestyle fashion photograph of a young man with freckles and buzz cut sitting on a wide windowsill in a bright Scandinavian apartment with white walls and pale oak floor, holding a ceramic cup, morning sunlight through linen curtains falling across the FORM 01 hoodie. Candid, quiet mood. [PRODUCT LOCK] [LOOK LOCK]
```

**M5 — duet przy morzu** → `assets/img/model-coast.jpg` (16:9)
```
Wide fashion campaign photograph of two friends in FORM 01 hoodies (one celadon, one bone) standing on Baltic sand dunes with pale grass under an overcast sky, wind moving their hair, lots of negative sky space at the top for headline text. [PRODUCT LOCK] [LOOK LOCK]
```

---

## 4. Wideo

Najlepiej generuj **image-to-video** z istniejących zdjęć (zachowuje wygląd bluzy). W Artlist wybierz model wideo z opcją image-to-video i jako klatkę startową użyj wskazanego pliku.

**V1 — film na stronę główną (hero)** → `assets/video/hero-16x9.mp4` · 16:9 · 6–10 s · pętla
Start frame: `hero-campaign.jpg`
```
Slow cinematic push-in on the two models in celadon hoodies in the limestone courtyard. A gentle breeze moves their hair and the hoodie fabric; the woman slowly turns her head toward the camera, the man shifts his weight. Very subtle, calm movement, no camera shake, soft overcast light, seamless loop feel. [PRODUCT LOCK] [LOOK LOCK]
```

**V2 — film produktowy** → `assets/video/product-4x5.mp4` (4:5) oraz `assets/video/product-film.mp4` (21:9)
Start frame: `product-front.jpg`
```
The FORM 01 hoodie on an invisible mannequin slowly rotates 180 degrees on a seamless off-white background, revealing the back and the double-layer hood, soft studio light, the heavy cotton fabric gently settling. Smooth, minimal, premium product film. [PRODUCT LOCK] [LOOK LOCK]
```

**V3 — Reels / TikTok 9:16 (3 klipy po 6–8 s)** → `assets/video/reel-01.mp4`, `reel-02.mp4`, `reel-03.mp4`
```
REEL 01 — 9:16 vertical. Handheld-feel tracking shot following a young woman in the FORM 01 hoodie walking through a minimalist concrete underpass, she pulls the hood up in one smooth move and looks into the lens. Quick but calm, natural light. [PRODUCT LOCK] [LOOK LOCK]
REEL 02 — 9:16 vertical. Macro shots sequence: fingers brushing the soft brushed inside of the fabric, the thick ribbed cuff stretching and snapping back, the hood edge folding. Raking light, tactile ASMR mood. [PRODUCT LOCK] [LOOK LOCK]
REEL 03 — 9:16 vertical. A man in the FORM 01 hoodie sits on a stone bench by the sea at sunrise, steam from a coffee cup, slow camera arc around him, wind moving the hood. [PRODUCT LOCK] [LOOK LOCK]
```
Muzyka: w Artlist wyszukaj „minimal ambient electronic, slow, warm” lub „lo-fi house soft” — spokojny puls 90–110 BPM.

---

## 5. Gdzie podmienić pliki w sklepie (`index.html`)

| Nowy plik | Zmień w `index.html` |
|---|---|
| `assets/video/hero-16x9.mp4` | **już jest** (4 s, 480p, darmowa generacja). Wersję 1080p / 8–10 s podmień pod tą samą nazwą — nic w kodzie nie trzeba zmieniać |
| `assets/video/product-4x5.mp4`, `product-film.mp4`, `reel-01.mp4` | nic — ścieżki są już wpisane w kampanii i na karcie produktu |
| `product-back.jpg` | dodaj w galerii (`#gallery`) nową `<figure class="g">` z `<img src="assets/img/product-back.jpg">` |
| `product-front-kosc.jpg`, `product-front-grafit.jpg` | w skrypcie zamień stałą `IMG` na mapę kolor → plik i usuń klasy filtrów `f-kosc`, `f-grafit` |
| `detail-*.jpg` | podmień `div.crop c-hood / c-pocket / c-cuff` w galerii na `<img>` z nowymi plikami |
| `model-*.jpg` | sekcja kampanii (`.camp-grid`) — zamień kadry `c-woman`, `c-man` na `<img>` |
