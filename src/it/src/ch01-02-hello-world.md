## Ciao, Mondo!

Ora che hai installato Rust, è tempo di scrivere il tuo primo programma Rust.
È tradizione quando si impara un nuovo linguaggio scrivere un semplice
programma che stampa `Hello, world!` (che noi abbiamo tradotto come `Ciao,
mondo!`) sullo schermo, quindi faremo lo stesso qui!

> Nota: Questo libro assume tu abbia conoscenze di base con la linea di
> comando. Rust non fa specifiche richieste su quali strumenti usi o dove
> scrivi il tuo codice, quindi se preferisci usare un ambiente di sviluppo
> integrato (IDE) invece della linea di comando, sentiti libero di usare il tuo
> IDE preferito. Tanti IDE hanno supporto per Rust; controlla la documentazione
> dell'IDE per maggiori dettagli. Il team di Rust si è concentrato
> nell'abilitare un grande supporto per gli IDE attraverso il `rust-analyzer`.
> Guarda l'[Appendice D][devtools]<!-- ignore --> per maggiori dettagli.

### Creare la Cartella del Progetto

Inizia creando una cartella dove inserire il codice Rust. Non importa dove si
trova il tuo codice per Rust, ma per gli esercizi e per i progetti in questo
libro, consigliamo di fare una cartella _progetti_ nella tua home directory e
tenere tutti i tuoi progetti lì.

Apri un terminale e digita i seguenti comandi per fare una cartella _progetti_
e una cartella per il progetto “Hello, world!” al suo interno.

Per Linux, macOS e PowerShell su Windows, esegui:

```console
$ mkdir ~/projects
$ cd ~/projects
$ mkdir hello_world
$ cd hello_world
```

Per Windows CMD, esegui:

```cmd
> mkdir "%USERPROFILE%\projects"
> cd /d "%USERPROFILE%\projects"
> mkdir hello_world
> cd hello_world
```

### Scrivere ed Eseguire un Programma in Rust

Successivamente, crea un nuovo file sorgente e chiamalo _main.rs_. I file Rust
terminano sempre con l'estensione _.rs_. Se stai usando più di una parola come
nome del file, convenzionalmente si usa un trattino basso per separare le
parole. Ad esempio, usa _hello_world.rs_ anziché _helloworld.rs_.

Ora apri il file _main.rs_ appena creato e digita il codice del Listato 1-1.

<Listing number="1-1" file-name="main.rs" caption="Un programma che stampa `Ciao, mondo!`">

```rust
fn main() {
    println!("Ciao, mondo!");
}
```

</Listing>

Salva il file e torna sulla tua finestra del terminale nella cartella
_~/projects/hello_world_. Su Linux o macOS, esegui il seguente comando per
compilare ede eseguire il file:

```console
$ rustc main.rs
$ ./main
Ciao, mondo!
```

Su Windows, esegui `.\main` invece di `./main`:

```powershell
> rustc main.rs
> .\main
Ciao, mondo!
```

Indipendentemente dal tuo sistema operativo, la stringa `Ciao, mondo!` dovrebbe
essere stampata sul terminale. Se non vedi questo output, ritorna alla parte
[“Diagnostica”][diagnostica]<!-- ignore --> della sezione Installazione
per avere aiuto.

Se `Ciao, mondo!` è stato stampato, congratulazioni! Hai ufficialmente scritto
un programma Rust. Questo ti rende un programmatore Rust — benvenuto!

### Anatomia di un Programma Rust

Rivediamo questo programma “Ciao, mondo” nel dettaglio. Ecco il primo pezzo del
puzzle:

```rust
fn main() {

}
```

Queste righe definiscono una funzione chiamata `main`. La funzione `main`
è speciale: è sempre la prima parte del codice a essere eseguita in tutti 
i programmi Rust eseguibili. Qui, la prima riga dichiara una funzione chiamata
`main` che non ha parametri e non ritorna nulla. Se ci fossero parametri,
andrebbero all'interno delle parentesi `()`.

Il corpo della funzione è circondato dalle `{}`. Rust richiede parentesi graffe
attorno tutti i corpi delle funzioni. È buona pratica posizionare la prima
parentesi sulla stessa riga della definizione della funzione, aggiungendo uno
spazio in mezzo.

> Nota: Se vuoi legarti a uno stile standard nei tuoi progetti Rust, puoi
> usare un formattatore automatico chiamato `rustfmt` per formattare il tuo
> codice in un particolare stile (di più su `rustfmt` nell'[Appendice
> D][devtools]<!-- ignore -->).  Il team di Rust ha incluso questo strumento
> con la distribuzione standard di Rust, come anche `rustc`, quindi dovrebbe
> già essere installato sul tuo computer!

TODO
