# Progetto: pagina "Comandi ct + tmux"

Pagina HTML personale di Nello Sacco con i comandi essenziali `ct` + tmux, pubblicata su GitHub Pages. Cresce nel tempo: Nello porta nuovi comandi/appunti, Claude li aggiunge alla pagina e ripubblica.

## Fatti fissi
- **File unico**: `index.html` (in questa cartella). È la copia canonica. Il vecchio file sul Desktop è morto, ignoralo.
- **Sito live**: https://nello040665.github.io/comandi-ct-tmux/
- **Repo GitHub**: https://github.com/Nello040665/comandi-ct-tmux (pubblico)
- **Account GitHub**: `Nello040665` (deve essere l'account gh attivo → `gh auth switch --user Nello040665`)
- **Autore commit**: nome "Nello Sacco", email "nello.sacco@bolognagomme.com"

## Come aggiornare la pagina (procedura standard)
1. Modifica `index.html` (aggiungi righe tabella, note, riquadri).
2. Aggiorna la data in fondo: campo `Ultimo aggiornamento:` nel footer → data/ora attuale (`date "+%Y-%m-%d %H:%M"`).
3. Commit + push:
   ```
   cd ~/comandi-ct-tmux
   gh auth switch --user Nello040665
   git add index.html
   git -c user.email="nello.sacco@bolognagomme.com" -c user.name="Nello Sacco" commit -m "descrizione modifica"
   git push origin main
   ```
4. Verifica live (Pages ci mette ~1 min): `curl -s https://nello040665.github.io/comandi-ct-tmux/ | grep "testo appena aggiunto"`.

## Convenzioni di stile della pagina
- Comandi terminale → classe CSS `.cmd`.
- Nota azzurra informativa → `<p class="note">`.
- Avviso rosso/pericolo → `<p class="warn">`.
- Gruppo di righe nella tabella → `<tr class="grp">`.

## Come riapre Nello questo progetto
`cd ~/comandi-ct-tmux && claude` — poi dice "aggiungi X alla pagina".
In alternativa modifica diretta dal browser su github.com (utile senza MacBook).
