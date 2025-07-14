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

Il corpo della funzione `main` contiene il seguente codice:

```rust
println!("Ciao, mondo!");
```

Questa riga svolge tutto il lavoro in questo piccolo programma: stampa il testo
sullo schermo. Ci sono 3 dettagli importanti da notare qui.

Primo, `println!` chiama una macro di Rust. Se avesse chiamata una funzione,
sarebbe scritto come `println` (senza il `!`). Le macro in Rust sono un modo di
scrivere codice che genera codice per estendere la sintassi di Rust e ne
parleremo più nel dettaglio nel [Capitolo 20][ch20-macros]<!-- ignore -->. Per
adesso, hai solo bisogno di sapere che usare un `!` indica l'uso di una macro
anziché una normale funzione e che le macro non sempre seguono le stesse regole
delle funzioni.

Secondo, puoi vedere la stringa `"Ciao, mondo!"`. Passiamo questa stringa come
argomento per `println!` e la stringa è stampata a schermo.

Terzo, finiamo la riga con un punto e virgola (`;`), che indica la fine di
quest'espressione e che la prossima è pronta a cominciare. La maggior parte
delle righe del codice Rust finisce con un punto e virgola.

### Compilare ed Eseguire sono Passaggi Separati

Hai appena eseguito un programma appena creato, quindi esaminiamo ogni
passaggio di questo processo.

Prima di eseguire un programma Rust, devi compilarlo usando il compilatore
di Rust digitando il comando `rustc` con il nome del file come argomento,
così:

```console
$ rustc main.rs
```

Se conosci C o C++, noterai che questo è simile a `gcc` o `clang`. Dopo aver
compilato correttamente, Rust produce un file binario eseguibile.

Su Linux, macOS e PowerShell su Windows, puoi vedere l'eseguibile digitando il
comando `ls` sulla tua shell:

```console
$ ls
main  main.rs
```

Su Linux e macOS, vedrai due file. Con PowerShell su Windows, vedrai gli stessi
tre file che vedresti usando CMD. Con CMD su Windows, dovresti digitare il
seguente:

```cmd
> dir /B %= the /B option says to only show the file names =%
main.exe
main.pdb
main.rs
```

Questo mostra il file del codice sorgente con l'estensione _.rs_, il file
eseguibile (_main.exe_ su Windows, _main_ sulle altre piattaforme), e, usando
Windows, un file contenente informazioni sul debugging con l'estensione _.pdb_.
Da qui, esegui il file _main_ o _main.exe_ così:

```console
$ ./main # or .\main on Windows
```

Se il tuo _main.rs_ è il tuo programma “Ciao, mondo!”, questa riga stampa
`Ciao, mondo!` sul tuo terminale.

Se sei familiare con un linguaggio dinamico, come Ruby, Python o Javascript,
potresti non essere abituato a compilare ed eseguire un programma in passaggi
separati. Rust è un linguaggio _compilato in anticipo_, il che significa che
puoi compilare un programma e dare l'eseguibile a qualcun altro e lui può
eseguirlo senza avere Rust installato. Se dai a qualcuno un file _.rb_, _.py_ o
_.js_, lui avrà bisogno di avere Ruby, Python o Javascript installati
(rispettivamente), però in quei linguaggi hai bisogno di un solo comando per
compilare ed eseguire il tuo programma. Ogni cosa è un compromesso nello stile
di un linguaggio.

Compilare con `rustc` è abbastanza per programmi semplici, ma man mano che il
tuo progetto cresce, ???. Nella prossima pagina, ti introdurremo allo strumento
Cargo, che ti aiuta a scrivere programmi Rust del mondo reale.

[diagnostica]: ch01-01-installation.md#diagnostica
[devtools]: appendix-04-useful-development-tools.md
[ch20-macros]: ch20-05-macros.md
