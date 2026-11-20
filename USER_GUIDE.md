# Flowchart Master – User guide / Guida utente

*English first, Italiano più sotto.*

---

## English

### 1. Starting
Double-click **FlowchartMaster.exe** (or install it with **FlowchartMaster-Setup-…exe**). No installation, no internet connection and no account are needed. The first start shows a sample corporate org chart and a sample flowchart so you can try things straight away. Switch the language with **EN / IT** at the top right (or *View › Language*).

**Dark interface:** *View › Interface* offers **Light**, **Dark** and **Follow Windows** (the default: the program uses whatever Windows is set to). **Ctrl+Shift+D** flips between light and dark at any time; the choice is remembered. The interface look changes only menus, panels and windows – your diagrams keep their own colours, so prints and exports look the same. To give a diagram a dark page too, apply the **Dark** theme (see *Themes and styles*). The start-up sample follows the interface by itself until you change it.

### 2. The screen
- **Menu bar**: File, Edit, View, Insert, Layout, Format, Tools, Help.
- **Toolbar**: new/open/save, undo/redo, Select / Connect / Pan tools, **Fit to window** and **Actual size (1:1)**, add position, add subordinate, layout algorithm + *Layout* button, Print; on the right the light/dark switch (moon/sun) and EN / IT. Picture reconstruction and PDF export are in the File menu (Ctrl+I, Ctrl+E).
- **Library (left)**: organisational elements, basic shapes, flowchart symbols, containers and swimlanes, *My saved shapes* and *Templates*. **Drag** a tile onto the canvas or **click** it to add it in the middle of the view.
- **Canvas (centre)**: one tab per diagram (a project can hold many); the **×** on a tab closes that diagram (Ctrl+Z brings it back). **Mouse wheel zooms around the pointer**; Shift+wheel scrolls sideways, Alt+wheel up/down; middle drag or Space+drag pans. Zoom controls bottom-left, see-through minimap (project map) bottom-right.
- **Properties (right)**: everything about the selection – text, font, colours, border, corners, shadow, transparency, icon, photo, position and size, organisational data, connector settings. With nothing selected it shows the diagram settings, layout options and themes.
- **Status bar**: hints, counts, selection, unsaved marker, zoom.

### 3. Editing
- **Select**: click; add/remove with **Ctrl** or **Shift** + click; drag on empty space for a selection rectangle.
- **Move**: drag. Blocks snap to the grid and to **pink alignment guides**; hold **Alt** to move freely. Arrow keys nudge (Shift = one grid step).
- **Resize**: drag the white handles (Shift keeps proportions). With several blocks selected (Ctrl+click) every one shows handles: dragging any of them **stretches all the selected blocks together** by the same amount.
- **Text**: double-click a block or press **F2**. For org positions the three lines are *role / name / department*. Click outside or press Ctrl+Enter to confirm, Esc to cancel.
- **Connect**: hover a block and drag one of the **blue dots** to another block. Dropping on empty space creates a new connected block. You can also use the Connect tool (C) or *Insert › Connect selected*.
- **Connector options**: select a line to change **Route** (orthogonal, straight, curved), **Line style** (9: solid, dashed, dotted, long dash, dash-dot, dash-dot-dot, short dash, sparse dots, double), width, colour, **Start** and **End** arrowheads (8: none, filled, open, diamond, open diamond, dot, open circle, bar), entry/exit sides, label, and the relationship type (hierarchical, functional dotted-line, flow). Every choice is shown as a small drawing. Drag the yellow dot to move the middle segment. The same line styles apply to block borders.
- **Overlapping connectors** read as one line: connectors running along the same path (or within 2.5 units of each other) are drawn once, so shared trunks never look doubled or darker.
- **Copy, cut, paste (Ctrl+C / Ctrl+X / Ctrl+V)** work for every block, shape, container (with what is inside), group and the connectors between them; selecting a connector copies it with its two blocks. Shapes also travel between two open windows, and text copied from another program is pasted as a text block. Also duplicate, delete, group, lock.
- **Layers**: **Page Up** brings the selection one step forward, **Page Down** one step back; with Shift all the way to the front / back.
- **Freeform shape**: Insert › Freeform shape, click points, double-click or Enter to finish.
- **Pictures**: Properties › Photo / picture (employee photos are shown in a circle) and Icon (24 built-in icons or your own PNG/JPG).
- **Undo/redo**: Ctrl+Z / Ctrl+Y, up to 200 steps.

### 4. Org charts
- Select a position and press **Tab** for a subordinate, **Enter** for a colleague; or use the buttons in Properties (also *Add assistant*, *Add manager above*).
- Fill in the **Organisational data**: name, role, department, functional area, direct manager (choose from the list to move the position), description, responsibilities, contact, employment status, position status (occupied, vacant, temporary). Vacant positions are drawn dashed with "VACANT POSITION".
- **Drag a position onto another** to make it report there.
- **Deleting** a position moves its subordinates up to its manager.
- **Dotted-line reporting**: connect two positions that already have a manager, or set the connector type to *Functional*.
- **Automatic layout**: Layout menu or toolbar. Choose *Hierarchy – balanced*, *Hierarchy – compact* (stacks small teams), *Layered flow*, *Grid* or *Circular*, and the direction (top-down, bottom-up, left-right, right-left). With *Re-layout automatically on changes* only the affected tree moves.
- **Tools › Check org chart** finds reporting cycles and positions with two solid managers. **Tools › Statistics** counts positions, vacancies and departments.
- **Employee lists**: *File › Import employee list (CSV)* builds a chart from a spreadsheet (columns such as id, name, title, department, manager_id; Italian headers work too). *File › Export › Employee list (CSV)* writes it back.

### 5. Reconstructing a diagram from a picture
*File › Reconstruct from image* (Ctrl+I), the toolbar button *From image*, or open a JPG/PNG/PDF directly.
1. **Import** – choose a JPG, PNG or PDF (pick the page for multi-page PDFs).
2. **Image processing** – automatic cropping, rotation correction (deskew), extra rotation, contrast enhancement, noise reduction, sharpening, background cleanup, resolution optimisation. For photos taken at an angle tick *Perspective correction* and drag the 4 orange corners onto the page corners. Press *Process image*.
3. **Recognition** – choose the OCR engine and language, press *Start recognition*.
4–5. **Preview & correction** – the result is drawn over the picture: **blue** blocks, **green** text, **orange** connectors, **red** = uncertain, please check. Use *Next uncertain ›* to walk through them.
   - Click a block to edit its text, shape, colours or its parent; *Re-read text (OCR)* reads it again.
   - *Add block* (drag a rectangle), *Connect* (click two blocks), *Delete*, *Merge selected blocks*, *Split block in two*, *Reverse connector*, *Mark verified*.
   - Ctrl + wheel zooms, right or middle drag pans.
6–7. **Generate & optimise** – choose the diagram type, keep original colours/positions, keep the picture as a see-through **reference layer**, and optionally align to the grid, equalise sizes, apply an automatic layout or a theme. Press **Generate editable diagram**: a new tab with real, editable blocks and connectors appears. Elements that were uncertain stay outlined in red until you confirm them (Properties › *Mark as verified*). The reference layer can be hidden or removed in the diagram properties and is never exported.

**Text recognition** runs locally: Flowchart Master uses the OCR built into Windows 10/11 (Italian and/or English, depending on the Windows language packs installed) and, if present, a local Tesseract installation (put it in a `tesseract` folder next to the program or install it normally). *Tools › Text recognition (OCR)* shows what is available. Without OCR, shapes and lines are still recognised and you type the text.

### 6. Themes and styles
Properties (nothing selected) › Theme, or *Format › Apply theme*: **Original** (brings back the look the diagram was acquired with – the colours read from the imported picture, or its own styling before the first theme; it is kept automatically the first time you apply a theme), Corporate, Minimal, Modern, Industrial, Technical, Monochrome, Colour-coded departments, Dark (dark page, light text – pairs with the dark interface; exports keep the dark page). *Format › Colour by department* gives each department its own colour. Every colour picker has a palette; *Format › Palette › Add selection colour* builds your own palette. *Save selection style as template* and *Format › Style templates* reuse styles; *Copy/Paste format* copies a look between blocks. *Save selection as custom shape* puts any group of blocks into *My saved shapes* for future projects.

### 7. Saving, versions, recovery
- **Save** (Ctrl+S) writes a `.orgm` project (all diagrams, pictures and metadata in one file). *Save a copy* duplicates the project.
- **Auto-save**: every 60 s the project file is saved (if it has a name) and a recovery copy is kept. After a crash or power cut Flowchart Master offers to **recover** the work at the next start.
- **File › Version history**: save named versions inside the project and restore any of them.
- **File › Project properties**: name, category, author, tags, description, dates.

### 8. Export and print
*File › Export* or *File › Print* (Ctrl+P):
- **PNG / JPG** at 96–600 DPI (PNG can be transparent; can export the selection only).
- **Editable SVG** (vector; re-opening it in Flowchart Master restores the full diagram).
- **PDF** – vector, print quality; A4, A3, A2, A1, A0, Letter or custom size; portrait/landscape; margins; **Fit to page** or **Multi-page** tiling at a chosen scale (pages are labelled row/column for assembling posters); one or all diagrams. Flowchart Master PDFs can be re-opened as editable diagrams.
- **PowerPoint (PPTX)** – native shapes and connectors, one slide per diagram.
- **Print** creates the print-ready PDF and sends it to Windows printing (or opens it in your PDF viewer).

Importing: `.orgm` projects, SVG (Flowchart Master SVGs exactly; other SVGs best-effort, or via the picture wizard), PDF (Flowchart Master PDFs exactly; any other PDF – vector or scanned – is rendered and reconstructed with OCR), JPG/PNG, CSV employee lists.

### 9. Portable use
The `Flowchart Master` folder can be copied to a USB stick. If a folder named `portable_data` sits next to `FlowchartMaster.exe`, settings, saved shapes and recovery files are kept there instead of in your Windows profile.

### 10. Installing and updating
- **Install**: double-click `FlowchartMaster-Setup-<version>-r<release>.exe`. No administrator rights are needed; it installs into your user profile, adds Start-menu / desktop shortcuts, opens `.orgm` files with a double-click and appears in *Settings › Apps* (uninstall from there). The release number is shown in the setup window, in *Help › About* and in the file's properties.
- **Update**: put a newer Setup file in the update folder – by default the folder you installed from, or any local/network folder chosen in *Tools › Settings › Updates*. At start-up (or *Help › Check for updates*) Flowchart Master finds it and offers **Install now**, **Later** or **Skip this release**. Installing saves your work, closes the program, upgrades it and starts it again; projects and settings stay. No internet connection is used.
- Settings from the old ORGANIGRAM name are carried over automatically.

### 11. Fonts and interface colours
- The font list shows the **three fonts used most in the current file** at the top, then every font installed in Windows (with a search box). A font is read from disk the first time a diagram uses it. PNG/JPG/SVG exports use the same fonts; the vector PDF maps them to its standard Sans/Serif/Mono fonts.
- *Tools › Settings › Interface*: Light, Dark or Follow Windows, and your own colours for the accent, panels, windows and menus, the area around the drawing and the text (each look keeps its own colours; ↺ restores one, *Restore the built-in colours* all).

---

## Italiano

### 1. Avvio
Fai doppio clic su **FlowchartMaster.exe** (oppure installalo con **FlowchartMaster-Setup-…exe**). Non serve installazione, connessione internet né account. Al primo avvio trovi un organigramma aziendale e un diagramma di flusso di esempio. Cambia lingua con **EN / IT** in alto a destra (o *Visualizza › Lingua*).

**Interfaccia scura:** *Visualizza › Interfaccia* offre **Chiara**, **Scura** e **Come Windows** (predefinita: il programma segue l'impostazione di Windows). **Ctrl+Maiusc+D** alterna chiara e scura in qualsiasi momento; la scelta viene ricordata. L'aspetto dell'interfaccia cambia solo menu, pannelli e finestre: i diagrammi mantengono i propri colori, quindi stampe ed esportazioni restano uguali. Per dare anche al diagramma una pagina scura applica il tema **Scuro** (vedi *Temi e stili*). L'esempio iniziale segue da solo l'interfaccia finché non lo modifichi.

### 2. Lo schermo
- **Barra dei menu**: File, Modifica, Visualizza, Inserisci, Layout, Formato, Strumenti, Aiuto.
- **Barra strumenti**: nuovo/apri/salva, annulla/ripeti, strumenti Seleziona / Collega / Sposta vista, **Adatta alla finestra** e **Dimensioni reali (1:1)**, aggiungi posizione, aggiungi subordinato, algoritmo di layout + pulsante *Layout*, Stampa; a destra il selettore chiaro/scuro (luna/sole) ed EN / IT. Ricostruzione da immagine ed esportazione PDF sono nel menu File (Ctrl+I, Ctrl+E).
- **Libreria (sinistra)**: elementi organizzativi, forme di base, simboli di flusso, contenitori e corsie, *Le mie forme salvate*, *Modelli*. **Trascina** un elemento sulla tela o **cliccalo** per aggiungerlo al centro della vista.
- **Tela (centro)**: una scheda per diagramma (un progetto può contenerne molti); la **×** sulla scheda chiude quel diagramma (Ctrl+Z lo recupera). **La rotella del mouse fa lo zoom centrato sul puntatore**; Maiusc+rotella scorre in orizzontale, Alt+rotella in verticale; trascinamento col tasto centrale o Spazio+trascinamento sposta la vista. Zoom in basso a sinistra, mappa del progetto (minimappa) semitrasparente in basso a destra.
- **Proprietà (destra)**: testo, carattere, colori, bordo, angoli, ombra, trasparenza, icona, foto, posizione e dimensioni, dati organizzativi, connettori. Senza selezione: impostazioni del diagramma, layout e temi.
- **Barra di stato**: suggerimenti, conteggi, selezione, modifiche non salvate, zoom.

### 3. Modifica
- **Selezione**: clic; aggiungi/togli con **Ctrl** o **Maiusc** + clic; trascina nel vuoto per un rettangolo di selezione.
- **Spostamento**: trascina. I blocchi si agganciano alla griglia e alle **guide rosa**; tieni **Alt** per spostare liberamente. Frecce = spostamento fine (Maiusc = un passo di griglia).
- **Dimensioni**: trascina le maniglie bianche (Maiusc mantiene le proporzioni). Con più forme selezionate (Ctrl+clic) ognuna mostra le maniglie: trascinandone una **si stirano tutte insieme** della stessa misura.
- **Testo**: doppio clic sul blocco o **F2**. Per le posizioni le tre righe sono *ruolo / nome / reparto*. Clic fuori o Ctrl+Invio per confermare, Esc per annullare.
- **Collegare**: passa sopra un blocco e trascina uno dei **pallini blu** su un altro blocco; rilasciando nel vuoto si crea un nuovo blocco collegato. Oppure strumento Collega (C) o *Inserisci › Collega selezionati*.
- **Connettori**: **Percorso** (ortogonale, diretto, curvo), **Stile linea** (9: continua, tratteggiata, punteggiata, tratto lungo, tratto-punto, tratto-punto-punto, tratto corto, punti radi, doppia), spessore, colore, frecce di **Inizio** e **Fine** (8: nessuna, piena, aperta, rombo, rombo vuoto, pallino, cerchio vuoto, barretta), lati di uscita/entrata, etichetta e tipo di relazione (gerarchica, funzionale tratteggiata, flusso). Ogni scelta è mostrata con un piccolo disegno. Il pallino giallo sposta il tratto centrale. Gli stessi stili valgono per i bordi dei blocchi.
- **Connettori sovrapposti** appaiono come una linea sola: i tratti che seguono lo stesso percorso (o distano meno di 2,5 unità) vengono disegnati una volta, così i tronchi comuni non sembrano doppi o più scuri.
- **Copia, taglia, incolla (Ctrl+C / Ctrl+X / Ctrl+V)** funzionano per tutti i blocchi, forme, contenitori (con il contenuto), gruppi e i connettori tra loro; selezionando un connettore lo copi con i suoi due blocchi. Le forme passano anche tra due finestre aperte e il testo copiato da altri programmi diventa un blocco di testo. Inoltre duplica, elimina, raggruppa, blocca.
- **Livelli**: **Pag ↑** porta la selezione un livello avanti, **Pag ↓** un livello indietro; con Maiusc in primo piano / in fondo.
- **Forma libera**: Inserisci › Forma libera, clic per i punti, doppio clic o Invio per finire.
- **Immagini**: Proprietà › Foto (mostrata in un cerchio) e Icona (24 icone incluse o un tuo PNG/JPG).
- **Annulla/ripeti**: Ctrl+Z / Ctrl+Y, fino a 200 passi.

### 4. Organigrammi
- Seleziona una posizione e premi **Tab** per un subordinato, **Invio** per un collega; oppure i pulsanti nelle Proprietà (anche *Aggiungi assistente*, *Aggiungi responsabile sopra*).
- Compila i **Dati organizzativi**: nome, ruolo, reparto, area funzionale, responsabile diretto (sceglilo dall'elenco per spostare la posizione), descrizione, responsabilità, contatto, stato contrattuale, stato della posizione (occupata, vacante, temporanea). Le posizioni vacanti sono tratteggiate con "POSIZIONE VACANTE".
- **Trascina una posizione su un'altra** per farla riportare a quella.
- **Eliminando** una posizione, i suoi subordinati passano al suo responsabile.
- **Riporto funzionale (tratteggiato)**: collega due posizioni che hanno già un responsabile, oppure imposta il connettore su *Funzionale*.
- **Layout automatico**: menu Layout o barra strumenti – *Gerarchia bilanciata*, *Gerarchia compatta* (impila i piccoli team), *Flusso a livelli*, *Griglia*, *Circolare*; direzione dall'alto, dal basso, da sinistra, da destra. Con *Riorganizza automaticamente* si sposta solo l'albero interessato.
- **Strumenti › Verifica organigramma** trova cicli e doppi responsabili; **Strumenti › Statistiche** conta posizioni, vacanze e reparti.
- **Elenchi dipendenti**: *File › Importa elenco dipendenti (CSV)* crea l'organigramma da un foglio di calcolo (colonne come id, nome, ruolo, reparto, responsabile; vanno bene anche intestazioni italiane). *File › Esporta › Elenco dipendenti (CSV)* lo riesporta.

### 5. Ricostruire un diagramma da un'immagine
*File › Ricostruisci da immagine* (Ctrl+I), pulsante *Da immagine*, o apri direttamente un JPG/PNG/PDF.
1. **Importa** – scegli JPG, PNG o PDF (per PDF di più pagine scegli la pagina).
2. **Elaborazione immagine** – ritaglio automatico, raddrizzamento, rotazione aggiuntiva, contrasto, riduzione rumore, nitidezza, pulizia sfondo, ottimizzazione risoluzione. Per foto scattate di sbieco attiva *Correzione prospettiva* e trascina i 4 angoli arancioni sugli angoli del foglio. Premi *Elabora immagine*.
3. **Riconoscimento** – scegli motore OCR e lingua, premi *Avvia riconoscimento*.
4–5. **Anteprima e correzione** – sopra l'immagine: **blu** blocchi, **verde** testo, **arancione** connettori, **rosso** = incerto, da verificare. *Prossimo incerto ›* li scorre uno a uno.
   - Clic su un blocco per correggere testo, forma, colori o superiore; *Rileggi testo (OCR)* lo rilegge.
   - *Aggiungi blocco* (trascina un rettangolo), *Collega* (clic su due blocchi), *Elimina*, *Unisci*, *Dividi*, *Inverti connettore*, *Segna verificato*.
   - Ctrl + rotella per lo zoom, tasto destro o centrale per spostare.
6–7. **Genera e ottimizza** – tipo di diagramma, mantieni colori/posizioni originali, mantieni l'immagine come **livello di riferimento** trasparente, e se vuoi allinea alla griglia, uniforma le dimensioni, applica un layout automatico o un tema. **Genera diagramma modificabile** crea una nuova scheda con blocchi e connettori veri e modificabili. Gli elementi incerti restano bordati di rosso finché non li confermi (Proprietà › *Segna come verificato*). Il livello di riferimento si nasconde o si rimuove nelle proprietà del diagramma e non viene mai esportato.

Il **riconoscimento del testo** è locale: Flowchart Master usa l'OCR integrato in Windows 10/11 (italiano e/o inglese secondo i pacchetti lingua installati) e, se presente, Tesseract installato sul PC (anche in una cartella `tesseract` accanto al programma). *Strumenti › Riconoscimento testo (OCR)* mostra cosa è disponibile. Senza OCR forme e linee vengono comunque riconosciute e il testo si scrive a mano.

### 6. Temi e stili
Proprietà (nessuna selezione) › Tema, o *Formato › Applica tema*: **Originale** (riporta lo schema acquisito in origine – i colori letti dall'immagine importata o lo stile proprio prima del primo tema; viene conservato automaticamente la prima volta che applichi un tema), Aziendale, Minimale, Moderno, Industriale, Tecnico, Monocromatico, Reparti a colori, Scuro (pagina scura e testo chiaro – si abbina all'interfaccia scura; le esportazioni mantengono la pagina scura). *Formato › Colora per reparto* assegna un colore a ogni reparto. Ogni selettore colore ha una tavolozza; *Formato › Tavolozza › Aggiungi colore della selezione* crea la tua. *Salva stile come modello* e *Formato › Modelli di stile* riutilizzano gli stili; *Copia/Incolla formato* copia l'aspetto. *Salva selezione come forma personalizzata* aggiunge gruppi di blocchi a *Le mie forme salvate*.

### 7. Salvataggio, versioni, recupero
- **Salva** (Ctrl+S) scrive un progetto `.orgm` (tutti i diagrammi, le immagini e i metadati in un file). *Salva una copia* duplica il progetto.
- **Salvataggio automatico** ogni 60 s (se il progetto ha un nome) più una copia di recupero. Dopo un arresto imprevisto, al riavvio Flowchart Master propone di **recuperare** il lavoro.
- **File › Cronologia versioni**: salva versioni con nome dentro il progetto e ripristinale.
- **File › Proprietà progetto**: nome, categoria, autore, etichette, descrizione, date.

### 8. Esportazione e stampa
*File › Esporta* o *File › Stampa* (Ctrl+P):
- **PNG / JPG** da 96 a 600 DPI (PNG anche trasparente; anche solo la selezione).
- **SVG modificabile** (vettoriale; riaprendolo in Flowchart Master torna il diagramma completo).
- **PDF** vettoriale per la stampa: A4, A3, A2, A1, A0, Letter o formato personalizzato; verticale/orizzontale; margini; **Adatta alla pagina** o **Multi-pagina** in scala (pagine numerate per riga/colonna per comporre poster); uno o tutti i diagrammi. I PDF di Flowchart Master si riaprono come diagrammi modificabili.
- **PowerPoint (PPTX)** con forme e connettori nativi, una diapositiva per diagramma.
- **Stampa** crea il PDF e lo invia alla stampa di Windows (o lo apre nel lettore PDF).

Importazione: progetti `.orgm`, SVG, PDF (vettoriali o scansionati, tramite OCR), JPG/PNG, elenchi CSV.

### 9. Uso portatile
La cartella `Flowchart Master` si può copiare su una chiavetta USB. Se accanto a `FlowchartMaster.exe` c'è la cartella `portable_data`, impostazioni, forme salvate e file di recupero vengono tenuti lì invece che nel profilo Windows.

### 10. Installazione e aggiornamenti
- **Installare**: doppio clic su `FlowchartMaster-Setup-<versione>-r<release>.exe`. Non servono diritti di amministratore: si installa nel tuo profilo utente, crea i collegamenti nel menu Start / sul desktop, apre i file `.orgm` con doppio clic e compare in *Impostazioni › App* (da lì si disinstalla). Il numero di release è indicato nella finestra di installazione, in *Aiuto › Informazioni* e nelle proprietà del file.
- **Aggiornare**: metti il nuovo file Setup nella cartella aggiornamenti – per default quella da cui hai installato, oppure una cartella locale o di rete scelta in *Strumenti › Impostazioni › Aggiornamenti*. All'avvio (o con *Aiuto › Cerca aggiornamenti*) Flowchart Master lo trova e propone **Installa ora**, **Più tardi** o **Salta questa release**. L'installazione salva il lavoro, chiude il programma, lo aggiorna e lo riavvia; progetti e impostazioni restano. Non usa internet.
- Le impostazioni del vecchio nome ORGANIGRAM vengono riprese automaticamente.

### 11. Caratteri e colori dell'interfaccia
- L'elenco dei caratteri mostra in alto **i tre più usati nel file corrente**, poi tutti i caratteri installati in Windows (con casella di ricerca). Un carattere viene letto dal disco la prima volta che un diagramma lo usa. Le esportazioni PNG/JPG/SVG usano gli stessi caratteri; il PDF vettoriale li sostituisce con i suoi caratteri standard Sans/Serif/Mono.
- *Strumenti › Impostazioni › Interfaccia*: Chiara, Scura o Come Windows, e colori personalizzati per accento, pannelli, finestre e menu, area attorno al disegno e testo (ogni aspetto ha i suoi colori; ↺ ne ripristina uno, *Ripristina i colori predefiniti* tutti).
