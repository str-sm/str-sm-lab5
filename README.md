# str-sm-lab5

## Exercițiul 1
Testați aplicații din repository-ul de la curs - cursul 5.


## Exercițiul 2
Procesarea paralelă a fişierelor text dintr-un director

#### Cerinţe
Implementați o aplicație Java care face următoarele lucruri:
1. Citeşte două argumente din linia de comandă:
- Calea către un director care conţine fişiere text (.txt);
- Numărul de fire de execuţie N.


2. Creează un ExecutorService ce are N fire de execuţie.


3. Pentru fiecare fişier text (.txt) din director, submite un Callable<FileStats> către executor.
Instanta Callable<FileStats> va face următoarele operații:
- Citeşte fişierul;
- Numără liniile, cuvintele şi caracterele;
- Returnează un obiect FileStats cu proprietăţile { String fullPath; int lines; int words; int chars; }


4. Colectează toate obiectele din Future<FileStats> într-o listă.


5. Toate rezultatele obținute vor fi scrise într-un singur fişier de raport (report.txt).

#### Sugestii
- Folosiți File.listFiles() pentru a obține lista de fișiere din director. Filtrați fișierele text după extensia .txt.


## Exercițiul 3
Generare și verificare paralelă a codurilor QR dintr-un fișier de URL-uri folosind CompletableFuture

#### Cerinţe
Implementați o aplicație Java care citește mai multe URL-uri dintr-un fișier.
Pentru fiecare URL citit din fişier, aplicația generează codul QR în paralel printr-un CompletableFuture creat cu supplyAsync, 
apoi inițiază decodarea şi verificarea QR-ului cu thenApplyAsync, raportând, la final, statusul („OK” sau „ERROR”) şi timpii de procesare.

#### Sugestii
- Se folosește librăria ZXing pentru generarea şi decodarea codurilor QR.
- Generarea și citirea codurilor QR este implementată în clasa edu.tucn.str.lab5.ex3.QrUtils.


## Exercițiul 4
Considerați lista cu API-uri gratuite (alt API public):
https://github.com/public-apis/public-apis?tab=readme-ov-file#index

Implementați o aplicație Java similară cu aplicațiile 3 și 4 din repository-ul de la cursul 5.

#### Cerințe:
Aplicația va realiza mai multe apeluri în paralel și va afișa rezultatele într-o simplă interfață grafică (Swing).





