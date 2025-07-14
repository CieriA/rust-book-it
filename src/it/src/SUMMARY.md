# Il Linguaggio di Programmazione Rust

[Il Linguaggio di Programmazione Rust](title-page.md)
[Prefazione](foreword.md) <!-- todo -->
[Introduzione](ch00-00-introduction.md) <!-- todo -->
[Traduzione dei termini](ch00-01-translated-terms.md) <!-- todo -->

## Primi passi

- [Primi passi](ch01-00-getting-started.md)
  - [Installazione](ch01-01-installation.md)
  - [Ciao, Mondo!]() <!-- todo -->
  - [Ciao, Cargo!]() <!-- todo -->

- [Indovina il numero]() <!-- todo -->

- [Concetti comuni di programmazione]() <!-- todo -->
  - [Variabili e Mutabilità]() <!-- todo -->
  - [Tipi di Dato]() <!-- todo -->
  - [Funzioni]() <!-- todo -->
  - [Commenti]() <!-- todo -->
  - [Flusso di Controllo]() <!-- todo -->

- [Capire l'Ownership]() <!-- todo -->
  - [Che cos'è l'Ownership?]() <!-- todo -->
  - [Reference e Borrowing]() <!-- todo -->
  - [Il tipo di dato Slice]() <!-- todo -->

- [Usare gli Struct per Rappresentare Dati Correlati]() <!-- todo -->
  - [Definire e Istanziare uno Struct]() <!-- todo -->
  - [Un Esempio di Programma con gli Struct]() <!-- todo -->
  - [Sintassi dei Metodi]() <!-- todo -->

- [Enum e Pattern Matching]() <!-- todo -->
  - [Definire un'enumerazione]() <!-- todo -->
  - [Il Costrutto `Match`]() <!-- todo -->
  - [Controllo del Flusso con `if let` e `let else`]() <!-- todo -->

## Conoscenze Base di Rust

- [Gestire Progetti con Pacchetti, Crate e Moduli]() <!-- todo -->
  - [Pacchetti e Crate]() <!-- todo -->
  - [Definire Moduli per controllare Scope e Privacy]() <!-- todo -->
  - [Percorsi per Riferirsi a un Elemento in un Albero di Moduli]() <!-- todo -->
  - [Portare Percorsi nello Scope con la Parola Chiave `use`]() <!-- todo -->
  - [Separare i Moduli in File Diversi]() <!-- todo -->

- [Collezioni Comuni]() <!-- todo -->
  - [Memorizzare Liste di Valori con i Vettori]() <!-- todo -->
  - [Memorizzare Testo UTF-8 con le Stringhe]() <!-- todo -->
  - [Memorizzare Chiavi e i Valori Associati con gli Hash Map]() <!-- todo -->

- [Gestione degli Errori]() <!-- todo -->
  - [Errori Irrecuperabili con `panic!`]() <!-- todo -->
  - [Errori Recuperabili con `Result`]() <!-- todo -->
  - [`panic!` o non `panic!`]() <!-- todo -->

- [Tipi Generici, Trait, Lifetime]() <!-- todo -->
  - [Tipi di Dato Generici]() <!-- todo -->
  - [Trait: Definire un Comportamento Comune]() <!-- todo -->
  - [Validare Reference con i Lifetime]() <!-- todo -->

- [Scrivere Test Automatizzati]() <!-- todo -->
  - [Come Scrivere i Test]() <!-- todo -->
  - [Controllare Come Vengono Eseguiti i Test]() <!-- todo -->
  - [Organizzazione dei Test]() <!-- todo -->

- [Un Progetto I/O: Creare un Programma da Linea di Comando]() <!-- todo -->
  - [Accettare Argomenti da Linea di Comando]() <!-- todo -->
  - [Leggere un File]() <!-- todo -->
  - [Rifattorizzare per Migliorare la Modularità e la Gestione degli Errori]() <!-- todo -->
  - [Sviluppare le Funzionalità della Libreria con lo Sviluppo Guidato dai Test]() <!-- todo -->
  - [Lavorare con le Variabili d'Ambiente]() <!-- todo -->
  - [Scrivere Errori in Standard Error Anziché Standard Output]() <!-- todo -->

## Pensare Rust

- [Caratteristiche Funzionali del Linguaggio: Iteratori e Closure]() <!-- todo -->
  - [Closure: Funzioni Anonime che Catturano l'Ambiente]() <!-- todo -->
  - [Processare una Serie di Elementi con gli Iteratori]() <!-- todo -->
  - [Migliorare il Nostro Progetto I/O]() <!-- todo -->
  - [Compariamo le Performance: Loop contro Iteratori]() <!-- todo -->

- [Di più su Cargo e Crates.io]() <!-- todo -->
  - [Personalizzare la Compilazione con i Profili di Pubblicazione]() <!-- todo -->
  - [Pubblicare una Crate su Crates.io]() <!-- todo -->
  - [Cargo Workspace]()v
  - [Installare Binari da Crates.io con `cargo install`]() <!-- todo -->
  - [Espandere Cargo con Comandi Personalizzati]() <!-- todo -->

- [Puntatori Intelligenti]() <!-- todo -->
  - [Usare `Box<T>` per Puntare a Dati sulla Heap]() <!-- todo -->
  - [Trattare i Puntatori Intelligenti come Normali Reference con `Deref`]() <!-- todo -->
  - [Eseguire Codice di Pulizia con il Trait `Drop`]() <!-- todo -->
  - [`Rc<T>`, il Conteggio delle Reference]() <!-- todo -->
  - [`RefCell<T>` e il Pattern Interno di Mutabilità]() <!-- todo -->
  - [Cicli di Reference Possono Portare a Perdita di Memoria]() <!-- todo -->

- [Concorrenza Sicura]() <!-- todo -->
  - [Usare i Thread per Eseguire Codice in Contemporanea]() <!-- todo -->
  - [Usare il Passaggio di Messaggi per Trasferire Dati tra Thread]() <!-- todo -->
  - [Concorrenza Condivisa]() <!-- todo -->
  - [Espandere la Concorrenza con i Trait `Send` e `Sync`]() <!-- todo -->

- [Fondamenti della Programmazione Asincrona: Async, Await, Future e Stream]() <!-- todo -->
  - [Le Future e la Sintassi Async]() <!-- todo -->
  - [Applicare la Concorrenza con Async]() <!-- todo -->
  - [Lavorare con Qualsiasi Numero di Future]() <!-- todo -->
  - [Gli Stream: Future in Sequenza]() <!-- todo -->
  - [Un'Occhiata ai Trait per Async]() <!-- todo -->
  - [Future, Task e Thread]() <!-- todo -->

- [Programmazione Orientata agli Oggetti]() <!-- todo -->
  - [Caratteristiche dei Linguaggi Orientati agli Oggetti]() <!-- todo -->
  - [Usare i Trait Object Permettendo Valori di Tipi Diversi]() <!-- todo -->
  - [Implementare un Pattern Orientato agli Oggetti]() <!-- todo -->

## Argomenti Avanzati

- [Pattern e Matching]() <!-- todo -->
  - [Tutti i Posti dove i Pattern Possono Essere Usati]() <!-- todo -->
  - [Rifiutabilità: Quando un Pattern Potrebbe Non Matchare?]() <!-- todo -->
  - [Sintassi dei Pattern]() <!-- todo -->

- [Caratteristiche Avanzate]() <!-- todo -->
  - [Unsafe Rust]() <!-- todo -->
  - [Trait Avanzati]() <!-- todo -->
  - [Tipi Avanzati]() <!-- todo -->
  - [Funzioni e Closure Avanzate]() <!-- todo -->
  - [Le Macro]() <!-- todo -->

- [Progetto Finale: Costruire un Multithreaded Server]() <!-- todo -->
  - [Costruire un Server a Thread Singolo]() <!-- todo -->
  - [Trasformare il Nostro Server a Thread Singolo in un Multithreaded Server]() <!-- todo -->
  - [Un Grazioso Arresto e Pulizia del Programma]() <!-- todo -->

- [Appendice]() <!-- todo -->
  - [A - Parole Chiave]() <!-- todo -->
  - [B - Operatori e Simboli]() <!-- todo -->
  - [C - Trait Derivabili]() <!-- todo -->
  - [D - Strumenti di Sviluppo]() <!-- todo -->
  - [E - Edizioni]() <!-- todo -->
  - [F - Traduzioni del Libro]() <!-- todo -->
  - [G - Com'è prodotto Rust e “Nightly Rust”]() <!-- todo -->
