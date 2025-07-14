# Il Linguaggio di Programmazione Rust

[Il Linguaggio di Programmazione Rust]()
[Prefazione]()
[Introduzione]()
[Traduzione dei termini]()

## Primi passi

- [Primi passi]()
  - [Installazione]()
  - [Ciao, Mondo!]()
  - [Ciao, Cargo!]()

- [Indovina il numero]()

- [Concetti comuni di programmazione]()
  - [Variabili e Mutabilità]()
  - [Tipi di Dato]()
  - [Funzioni]()
  - [Commenti]()
  - [Flusso di Controllo]()

- [Capire l'Ownership]()
  - [Che cos'è l'Ownership?]()
  - [Reference e Borrowing]()
  - [Il tipo di dato Slice]()

- [Usare gli Struct per Rappresentare Dati Correlati]()
  - [Definire e Istanziare uno Struct]()
  - [Un Esempio di Programma con gli Struct]()
  - [Sintassi dei Metodi]()

- [Enum e Pattern Matching]()
  - [Definire un'enumerazione]()
  - [Il Costrutto `Match`]()
  - [Controllo del Flusso con `if let` e `let else`]()

## Conoscenze Base di Rust

- [Gestire Progetti con Pacchetti, Crate e Moduli]()
  - [Pacchetti e Crate]()
  - [Definire Moduli per controllare Scope e Privacy]()
  - [Percorsi per Riferirsi a un Elemento in un Albero di Moduli]()
  - [Portare Percorsi nello Scope con la Parola Chiave `use`]()
  - [Separare i Moduli in File Diversi]()

- [Collezioni Comuni]()
  - [Memorizzare Liste di Valori con i Vettori]()
  - [Memorizzare Testo UTF-8 con le Stringhe]()
  - [Memorizzare Chiavi e i Valori Associati con gli Hash Map]()

- [Gestione degli Errori]()
  - [Errori Irrecuperabili con `panic!`]()
  - [Errori Recuperabili con `Result`]()
  - [`panic!` o non `panic!`]()

- [Tipi Generici, Trait, Lifetime]()
  - [Tipi di Dato Generici]()
  - [Trait: Definire un Comportamento Comune]()
  - [Validare Reference con i Lifetime]()

- [Scrivere Test Automatizzati]()
  - [Come Scrivere i Test]()
  - [Controllare Come Vengono Eseguiti i Test]()
  - [Organizzazione dei Test]()

- [Un Progetto I/O: Creare un Programma da Linea di Comando]()
  - [Accettare Argomenti da Linea di Comando]()
  - [Leggere un File]()
  - [Rifattorizzare per Migliorare la Modularità e la Gestione degli Errori]()
  - [Sviluppare le Funzionalità della Libreria con lo Sviluppo Guidato dai Test]()
  - [Lavorare con le Variabili d'Ambiente]()
  - [Scrivere Errori in Standard Error Anziché Standard Output]()

## Pensare Rust

- [Caratteristiche Funzionali del Linguaggio: Iteratori e Closure]()
  - [Closure: Funzioni Anonime che Catturano l'Ambiente]()
  - [Processare una Serie di Elementi con gli Iteratori]()
  - [Migliorare il Nostro Progetto I/O]()
  - [Compariamo le Performance: Loop contro Iteratori]()

- [Di più su Cargo e Crates.io]()
  - [Personalizzare la Compilazione con i Profili di Pubblicazione]()
  - [Pubblicare una Crate su Crates.io]()
  - [Cargo Workspace]()
  - [Installare Binari da Crates.io con `cargo install`]()
  - [Espandere Cargo con Comandi Personalizzati]()

- [Puntatori Intelligenti]()
  - [Usare `Box<T>` per Puntare a Dati sulla Heap]()
  - [Trattare i Puntatori Intelligenti come Normali Reference con `Deref`]()
  - [Eseguire Codice di Pulizia con il Trait `Drop`]()
  - [`Rc<T>`, il Conteggio delle Reference]()
  - [`RefCell<T>` e il Pattern Interno di Mutabilità]()
  - [Cicli di Reference Possono Portare a Perdita di Memoria]()

- [Concorrenza Sicura]()
  - [Usare i Thread per Eseguire Codice in Contemporanea]()
  - [Usare il Passaggio di Messaggi per Trasferire Dati tra Thread]()
  - [Concorrenza Condivisa]()
  - [Espandere la Concorrenza con i Trait `Send` e `Sync`]()

- [Fondamenti della Programmazione Asincrona: Async, Await, Future e Stream]()
  - [Le Future e la Sintassi Async]()
  - [Applicare la Concorrenza con Async]()
  - [Lavorare con Qualsiasi Numero di Future]()
  - [Gli Stream: Future in Sequenza]()
  - [Un'Occhiata ai Trait per Async]()
  - [Future, Task e Thread]()

- [Programmazione Orientata agli Oggetti]()
  - [Caratteristiche dei Linguaggi Orientati agli Oggetti]()
  - [Usare i Trait Object Permettendo Valori di Tipi Diversi]()
  - [Implementare un Pattern Orientato agli Oggetti]()

## Argomenti Avanzati

- [Pattern e Matching]()
  - [Tutti i Posti dove i Pattern Possono Essere Usati]()
  - [Rifiutabilità: Quando un Pattern Potrebbe Non Matchare?]()
  - [Sintassi dei Pattern]()

- [Caratteristiche Avanzate]()
  - [Unsafe Rust]()
  - [Trait Avanzati]()
  - [Tipi Avanzati]()
  - [Funzioni e Closure Avanzate]()
  - [Le Macro]()

- [Progetto Finale: Costruire un Multithreaded Server]()
  - [Costruire un Server a Thread Singolo]()
  - [Trasformare il Nostro Server a Thread Singolo in un Multithreaded Server]()
  - [Un Grazioso Arresto e Pulizia del Programma]()

- [Appendice]()
  - [A - Parole Chiave]()
  - [B - Operatori e Simboli]()
  - [C - Trait Derivabili]()
  - [D - Strumenti di Sviluppo]()
  - [E - Edizioni]()
  - [F - Traduzioni del Libro]()
  - [G - Com'è prodotto Rust e “Nightly Rust”]()
