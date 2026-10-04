# Vlad — Kinetoterapie & masaj (landing)

Site static, un singur fișier: `site/index.html`. Fără build, fără dependențe.

## Deploy (Netlify)
Live: https://vlad-kinetoterapie.netlify.app (site id `12493377-4f12-40f3-97f5-e14640971046`).
v1 a fost publicată ca fișier unic (imagini inline) prin import de pe un artifact claude.ai public,
pentru că sesiunea cloud nu avea acces de rețea la Netlify. `vlad-kinetoterapie-old` e un site gol, poate fi șters.

Pentru deploy automat din Git (necesar pentru faza 2), leagă site-ul de acest repo:
Netlify → Site configuration → Build & deploy → Continuous deployment → **Link repository** → `Nikita1129/taproom-buiucani-reels`, branch `master`.
`netlify.toml` setează deja publish dir = `site`. După asta, fiecare push pe `master` publică automat.

## Ce trebuie schimbat înainte de lansare
Toate contactele sunt placeholder. Caută și înlocuiește în `site/index.html`:
- `+37360000000` (tel: și wa.me) și `+373 60 000 000` (textul afișat)
- `vlad_kineto` (Telegram + Instagram)
- programul `Lun–Sâm, 09:00–20:00` și adresa din butonul „Locație” (`maps.apple.com/?q=...`)

## Structură
- `site/index.html` — pagina (CSS + JS inline)
- `site/assets/` — poză (WebP + JPG, 1x/2x), OG image, iconițe iOS/PWA
- `site/manifest.webmanifest` — „Add to Home Screen” pe iOS
- `netlify.toml` — publish dir, cache headers, security headers

## Urmează (faza 2)
- Programare online (calendar + sloturi) → Netlify Functions + Supabase
- Panou pentru Vlad (programările lui, confirmare/anulare) → pagină protejată cu login
