# Sito personale (Jekyll + Bootstrap Italia)

Stesso design del tema per biblioteche: blu istituzionale, angoli netti, solo Bootstrap Italia (nessun React).

## Avvio in locale

    bundle install
    bundle exec jekyll serve

Apri http://localhost:4000. Il sito carica Bootstrap Italia da jsDelivr.

## Cambiare l'obiettivo del sito: `_config.yml`

- `sito`: nome, ruolo, logo, fascia grigia in alto.
- `obiettivo`: titolo, presentazione e pulsante della home, più `sezioni_home` (ordine e presenza di `progetti`, `articoli`, `competenze`).
- `menu`: voci della barra blu (con `figli` per i sottomenu).
- `social`: link nel menu Contatti e nel piè di pagina.
- `header.ricerca`: mostra o nasconde la ricerca.

Esempi di obiettivo: portfolio `[progetti, competenze]`, blog `[articoli]`, curriculum `[competenze, progetti]`.

## Amministrazione: `/admin/`

Usa Decap CMS e legge `admin/config.yml`.

1. In locale: `npx decap-server` in un secondo terminale, poi apri http://localhost:4000/admin/.
2. In produzione: imposta `repo` in `admin/config.yml` e configura l'accesso GitHub (https://decapcms.org/docs/github-backend/).

Dall'admin si modificano articoli, progetti, pagine e `_config.yml`. Salvando `_config.yml` da lì i commenti del file vengono persi: fai un commit prima del primo salvataggio e tieni la documentazione in questo README.

## Contenuti

- Articoli: `_posts/AAAA-MM-GG-titolo.md`
- Progetti: `_progetti/nome.md` (campi `anno`, `descrizione`, `tag`, `link`)
- Pagine: `chi-sono.md`, `contatti.md`
- Ricerca: `/cerca/` usa `search.json`, generato in automatico.
