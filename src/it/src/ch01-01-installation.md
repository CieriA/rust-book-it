## Installazione

Il primo passaggio è installare Rust. Scaricheremo Rust attraverso `rustup`,
uno strumento da linea di comando per gestire le versioni di Rust e gli
strumenti a esso collegati. Hai bisogno di una connessione a internet per il
download.

> Nota: Se preferisci non usare `rustup` per un qualsiasi motivo, guarda
> [Altri Metodi di Installazione di Rust][altre-installazioni] per maggiori
> opzioni.

Il passaggio seguente installa la versione stabile più recente del compilatore
di Rust. La garanzia della stabilità di Rust assicura che tutti gli esempi del
libro che compilano, continueranno a compilare con versioni successive di Rust.
L'output potrebbe variare leggermente tra versioni perché Rust spesso migliora
i messaggi di errore e di avviso. In altre parole, qualsiasi versione più
recente di Rust tu installi con questi passaggi dovrebbe funzionare come
voluto.

> ### Notazione della Linea di Comando
> 
> In questo capitolo e per tutto il libro, mostreremo comandi da eseguire nel
> terminale. Le righe che dovresti digitare nel terminale iniziano con `$`.
> Non serve tu scriva il simbolo `$`: serve a indicare l'inizio di un nuovo
> comando. Righe che non iniziano con `$` mostrano generalmente l'output del
> comando precedente. Inoltre, i comandi specifici di PowerShell inizieranno
> con `>` anziché `$`.

### Installare `rustup` su Linux o macOS

Se stai usando Linux o macOS, apri un terminale ed esegui:

```console
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

Il comando scarica uno script e inizia l'installazione dello strumento
`rustup`, che installa l'ultima versione stabile di Rust. Potrebbe chiedere la
tua password. Se l'installazione avviene correttamente, dovresti vedere:

```text
Rust is installed now. Great!
```

Avrai anche bisogno di un _linker_, un programma che Rust usa per unire i suoi
output compilati in un unico file. È molto probabile tu lo abbia già.
Se ottieni degli errori del linker, dovresti installare un compilatore C,
che dovrebbe contenere un linker. Un compilatore C è inoltre molto utile poiché
alcuni dei pacchetti più comuni di Rust dipendono da codice C e avranno bisogno
di un compilatore C.

Su macOS, puoi installare un compilatore C eseguendo:

```console
$ xcode-select --install
```

GLi utenti Linux dovrebbero generalmente installare GCC o CLang, secondo la
documentazione della loro distribuzione. Per esempio, se usi Ubuntu, puoi
installare il pacchetto `build-essential`.

### Installare `rustup` su Windows

Su Windows, vai su [https://www.rust-lang.org/tools/install][installazione] e
segui le istruzioni per installare Rust. A un certo punto, ti verrà chiesto di
installare Visual Studio, che contiene un linker e le librerie native
necessarie per compilare dei programmi. Se hai bisogno di maggiore aiuto, vai
su [https://rust-lang.github.io/rustup/installation/windows-msvc.html][msvc]

### Diagnostica

Per controllare se hai installato Rust correttamente, apri una shell ed esegui:

```console
$ rustc --version
```

Dovresti ottenere il numero di versione, l'hash del commit, e la data del
commit per l'ultima versione stabile rilasciata, nel formato:

```text
rustc x.y.z (abcabcabc yyyy-mm-dd)
```

Se vedi questo, hai installato Rust correttamente! In caso contrario, controlla
che Rust sia nella tua variabile di sistema `%PATH%` come segue.

Su Windows CMD, esegui:

```console
> echo %PATH%
```

Su PowerShell, esegui:

```powershell
> echo $env:Path
```

Su Linux e macOS, esegui:

```console
$ echo $PATH
```

Se anche questo è corretto e Rust continua a non funzionare, ci sono numerosi
posti dove chiedere aiuto. Trova il modo di entrare in contatto con altri
Rustaceans (uno sciocco nome che ci siamo dati) sulla [pagina della
community][community].

### Aggiornare e Disinstallare

Una volta che Rust è installato con `rustup`, aggiornarlo a una nuova versione
è semplice. Dalla shell, esegui:

```console
$ rustup update
```

Per disinstallare Rust e `rustup`, esegui:

```console
$ rustup self uninstall
```

### Documentazione Locale

L'installazione di Rust include inoltre una copia locale della documentazione
per leggerla offline. Esegui `rustup doc` per aprire la documentazione locale
nel tuo browser.

Ogni volta che un tipo o una funzione deriva dalla standard library e non sei
sicuro di cosa faccia o di come usarlo, usa la documentazione dell'interfaccia
di programmazione dell'applicazione (API) per scoprirlo!

### Editor di Testo e Ambienti di Sviluppo Integrato

Questo libro non fa alcuna assunzione su quali strumenti tu stia usando e su
dove è scritto il tuo codice Rust. Qualsiasi editor di testo andrà bene!
Tuttavia, molti editor di testo e ambienti di sviluppo integrato (IDE) hanno
supporto nativo per Rust. Puoi trovare una lista di molti editor e IDE sulla
[pagina degli strumenti][strumenti] sul sito ufficiale di Rust.

### Lavorare Offline con Questo Libro

In molti esempi, useremo pacchetti di Rust esterni alla standard library. Per
usare questi esempi, dovrai avere una connessione a internet o aver installato
le dipendenze in precedenza. Per scaricare le dipendenze in anticipo, esegui il
comando seguente. (Spiegheremo cos'è `cargo` e cosa fanno questi comandi più
avanti.)

```console
$ cargo new get-dependencies
$ cd get-dependencies
$ cargo add rand@0.8.5 trpl@0.2.0
```

Questo salverà i download per questi pacchetti per fare in modo che tu non
debba installarli più avanti. Una volta eseguito questo comando, non hai
bisogno di conservare la cartella `get-dependencies`. Se hai eseguito questo
comando, puoi usare la flag `--offline` con tutti i comandi `cargo` per usare
queste versioni invece di provare a connettersi a internet.

[altre-installazioni]: https://forge.rust-lang.org/infra/other-installation-methods.html
[installazione]: https://www.rust-lang.org/tools/install
[msvc]: https://rust-lang.github.io/rustup/installation/windows-msvc.html
[community]: https://www.rust-lang.org/community
[strumenti]: https://www.rust-lang.org/tools
