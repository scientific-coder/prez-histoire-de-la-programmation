!SLIDE
# Quoi ?
* 2300 de langages de programmation
* juste les plus importants

!SLIDE
![généalogie des langages de programmation](http://www.georgehernandez.com/h/xComputers/Programming/Media/tongues-cleaner.png)

!SLIDE
# Crédits

Douglas Crockford

![Douglas Crockford](http://upload.wikimedia.org/wikipedia/commons/e/ef/Douglas_Crockford.jpg)

!SLIDE
## Hello World!
```c
#include<stdio.h>

main()
{
      printf("Hello World");

}
```
* [Repl.it](http://repl.it)
* [Ideone](http://ideone.com/)

!SLIDE
# & moi

!SLIDE
![tour d'un vieil ordinateur](http://images.wikia.com/creepypasta/images/5/5c/Old_computer.jpg)

!SLIDE
![Nexus 4](http://gigaom2.files.wordpress.com/2012/11/nexus-4-in-hand-e1352832035571.jpg)

!SLIDE
# Tour vs Nexus 4
spécs                 | tour          | « téléphone »                             | ratio
--------------------- |:-------------:| -----------------------------------------:|----------
volume                | 40 litres     | 0,1 litres                                | /400
procésseur            | 0,1 GHz       | 4 x 1,5 GHz                               | x60
mémoire vive          | 8 Mo          | 2048 Mo                                   | x256
espace disque         | 0,85 Go       | 16 Go                                     | ~x20
autres fonctionalités | ...           | * fonctionnalité téléphone                |
                      |               | * accéléromètre                           |
                      |               | * baromètre                               |
                      |               | * écran tactile                           |
                      |               | * résolution de 1280×768 px               |
                      |               | * 2 caméras                               |
                      |               | * camescope vidéo                         |
                      |               | * GPS                                     |
                      |               | * Internet par l'air ?!                   |
                      |               | * sur batterie, chargement par induction  |

!SLIDE

* histoire méconnue
* personnes qui devraient comprendre la valeur de nouvelles technos sont souvent les derniers
* utilisation de technos obsolètes
* parfois un pas un avant, parfois un pas en arrière
* mythe de l'inévitabilité

!SLIDE cover #hello-world execute
```js
container = document.getElementById('hello-world').getElementsByClassName('content')[0];
el = document.createElement('h1');
el.appendChild(document.createTextNode("L'histoire de la programmation en 1? h"));
container.appendChild(el)
```

!SLIDE
# le métier Jacquard (1801)
![métier Jacquard](http://upload.wikimedia.org/wikipedia/commons/b/b6/Jacquard_loom_p1040320.jpg)

.notes adapté depuis piano mécanique
.notes chaque carte représente un motif sur une ligne de ce qui est tissé
.notes 10x plus productif
.notes sabotage industriel
.notes Babbage, Lovelace, I/O

!SLIDE
# The Difference Engine par Charles Babbage (1822 / 1991)
![Difference Engine](https://upload.wikimedia.org/wikipedia/commons/f/ff/Babbage_Difference_Engine_(Being_utilised).jpg)

.notes Babage and Lovelace recognize potential for punchard for moving data in and out of their machines but Babbage didn't make it out

!SLIDE
# Ada Lovelace
![Ada Lovelace](http://upload.wikimedia.org/wikipedia/commons/8/87/Ada_Lovelace.jpg)

!SLIDE
# La tabulatrice d'Hollerith (1890)
![Hollerith Card Tabulating Machine](http://www.columbia.edu/cu/computinghistory/hh/f02.jpg)

.notes clerc questionnaire copy on punchard
.notes card = set of fielsets, each fieldset contained radio buttons, on/off
.notes tabulating machine, two parts, main parts, counting + sorting cabinet
.notes take a card put in machine, push down array of pins, pool of mercury completing circuit, open up drawers sorting machine

!SLIDE
![tabulatrice IBM](http://www.fcet.staffs.ac.uk/jdw1/sucfm/1924ibmtabulator.jpg)

.notes census success, Hollerith went on other vendors to apply to business
.notes 70' IBM et d'autres boîtes utilisaient encore ce type d'équipement
.notes card
.notes automatisation

!SLIDE
![carte perforée d'Hollerith](http://upload.wikimedia.org/wikipedia/commons/4/4c/Blue-punch-card-front-horiz.png)

.notes carte performée
.notes basé sur taille du billet de dollar car format déjà dispo pour ranger cartes, réduction coûts
.notes 80 colonnes sur la carte, each column containing 12
.notes 80 char limit
.notes Hollerith code
.notes Unit record management => corporattoins
.notes cartes envoyées chez les gens
.notes carte avec factures, et quand recu orateur punched
.notes "do not fold spindle or mutilate"

!SLIDE
![terminal Lear Siegler](https://lh4.googleusercontent.com/-1RmxG22Qn_Q/UP_blG1s7qI/AAAAAAAAEmU/9fYkuwB0cQ0/s502/Lear_Siegler-ADM3A_1782.jpg)

!SLIDE
![perforatrice IBM](http://raggio5.smugmug.com/History/Computer/i-Rgf2Lk3/0/L/P1010212-L.jpg)

.notes keypunch machine, IBM bien dans les 70'
.notes deck carte, un carte par ligne du program
.notes modifier sortir cartes réordonner

!SLIDE
# cartes perforées
* Memory
* Storage
* Archive
* Networking
* UI

!SLIDE
![programmation d'une perforatrice IBM](http://www.glennsmuseum.com/ibm/med/med_ibm_402_bd.jpg)

.notes accounting machines programmable dataflow
.notes program on punchboard
.notes spaghetti code
.notes pour longtemps c'est comme ça qu'on programmait

!SLIDE
![mainframe](http://cdn.softlayer.com/innerlayer/IBM7090.jpg)

.notes rise of the mainframes, digital computers
.notes crypto, dév d'armemements
.notes 40' 50', record machines until 70'

.notes store program concept, instead of plugboard of external programming source program is stored in the same memory as the data
.notes implication, prog modified itself, program will become intelligent, even conscious, donc bcp de travial pour ça mais hype
.notes intelligence artificielle
.notes fallait donc programmer d'une autre manière
.notes d'abord code machine, chiffre pour chaque opération que la machine savait faire, et quelques chiffres pour chaque cellule dans la mémoire

!SLIDE
# assembleur vs langage machine
```assembly
 A_CR  = $0D              ;carriage return
 BSOUT = $FFD2            ;kernel ROM sub, write to current output device
 ;
         LDX #$00         ;starting index in .X register
 ;
 LOOP    LDA MSG,X        ;read message text
         BEQ LOOPEND      ;end of text
 ;
         JSR BSOUT        ;output char
         INX
         BNE LOOP         ;repeat
 ;
 LOOPEND RTS              ;return from subroutine
 ;
 MSG     .BYT 'Hello, world!',A_CR,$00
```

.notes JSR # => jump to subroutine
.notes on peut pas tout anticiper, créer propres opcodes

!SLIDE
![mainframe](http://cdn.softlayer.com/innerlayer/IBM7090.jpg)

.notes en face disques, pouvaient pas contenir autant d'infos que ce que vous avez sur votre poche (de très, très loin)
.notes 8K de mémoire
.notes visualiser 8K
.notes octet = 8
.notes laissaient pas programmeurs s

!SLIDE
![Cray CDC 6600](http://www.cbi.umn.edu/graphics/cdc03b.jpg)

.notes cray control data 6600 fastest computer world
.notes 2 écrans
.notes clavier

!SLIDE
# Traitement par lots vs Temps partagé
.notes trop cher pour programmeurs à la console
.notes batch mode, "submit"
.notes cartes + tray
.notes si bug, jour d'après
.notes analyste = writes specs and draws flowchars
.notes programmeur code le programme
.notes keypuncher punches the program
.notes verifier checks the punches
.notes operator runs the program
.notes if there is a bug, call a meeting, nobody in charge of the whole thing

!SLIDE
# Bugs
> Mr. Edison…had been up the two previous nights working on fixing ‘a bug’ in his phonograph

!SLIDE
![bug](http://www.yalealumnimagazine.com/uploads/images/200002/1283957463/ND09_arts_quotations.jpg)

.notes Grace Hopper's Bug

!SLIDE
![table ASCII](http://www.asciitable.com/index/asciifull.gif)

ASCII -> Unicode -> UTF-8

.notes ASCII : 128 chars
.notes Unicode -> UTF-8

!SLIDE
![Teletype](http://www.columbia.edu/cu/computinghistory/teletype.jpg)

.notes teletype machine
.notes online / offline mode
.notes pourquoi touche suppr et backspace?
.notes mainframe ignorait
.notes 10 char/s
.notes CR + LF, carridge return, line feed, teletype
.notes interopérabilité, aggreement mutellement dévorable, CRLF
.notes HTTP

!SLIDE
# Temps partagé

.notes Batch vs Timesharing
.notes batch : discipline
.notes "timesharing is a fad"
.notes programmers were rejecting it
.notes they never tried timesharing, so they never understood it

!SLIDE
# Temps partagé
* premier réseau social
* partage de fichiers
* email
* distribution
* "cloud" computing
* chat
* blogs
* open source
* jeux, seul ou multi-joueur
* sécurité

.notes games, single and multiplayer # really important for tech dev
.notes security # huge security problem, bcp de programmes sur même espace mémoire

!SLIDE
# Unix
![Denis Richie & Ken Thompson](http://ultimatepeter.com/wp-content/uploads/2013/04/ken-thompson-l-and-dennis-ritchie-r.jpg)

Dennis Richie et Ken Thompson

!SLIDE
<iframe src="http://bellard.org/jslinux/">

!SLIDE
# Editeurs de texte
```
EDIT - TECO - EMACS
 \
  \- vi
```
.notes démo vi

!SLIDE
![terminal Lear Siegler](https://lh4.googleusercontent.com/-1RmxG22Qn_Q/UP_blG1s7qI/AAAAAAAAEmU/9fYkuwB0cQ0/s502/Lear_Siegler-ADM3A_1782.jpg)

.notes CRT terminal
.notes photo terminal space age
.notes arrow keys on letters

![touches flèches sur clavier terminal](http://i.stack.imgur.com/ILGdM.jpg)

.notes switch process to another on keystroke basis, software was not able to do it
.notes IBM 3270, page données depuis mainframe, character reverserd as field, button submit, envoyé à mainframe => www "oh yeah, I remember that"

!SLIDE
# Doug Engelbart, The Mother of All Demos (1968)

NLS : oN-Line System

<iframe width="853" height="480" src="//www.youtube.com/embed/mT_PhstIBIA" frameborder="0" allowfullscreen></iframe>

.notes tout c'est passé en 68-69
.notes hypertext
.notes on screen displays
.notes groupware
.notes video conferincing
.notes todo list
.notes outline processing
.notes doing and showing live
.notes ... et aussi la souris
.notes chorded keyboard, datamancer
.notes couple of hours to train and then do amazing things, world decided that it didn't want to work that hard
.notes son labo un des deux premiers sites de l'ARPANET
pendant ce temps, punchcards

!SLIDE
# Mini-ordinateurs

!SLIDE
# Micro-ordinateur

Intel & Datapoint (terminaux intélligents)

!SLIDE
# Ordinateur personnel
![Apple II](http://oldcomputers.net/pics/appleii-system.jpg)

.notes IBM, cpus Intel pas cher (8086), the "personal computer"

!SLIDE
# Gordon E. Moore
![graphique Loi de Moore](http://www.cmg.org/measureit/issues/mit41/m_41_2/plot.png)

.notes Gordon E Moore
.notes complexity constant at least 10 years
.notes 1965
.notes loi de Moore
.notes prediction self-fulfilling prohecy

.notes end of CPU innovation
.notes Intel (computers)
.notes PowerPC (games
.notes ARM (mobile)

!SLIDE
# Unix ('70)
![Unix](http://oldcomputers.net/pics/att-unix-pc-boot.jpg)

!SLIDE
# Windows ('95)
![Windows 95](http://www.guidebookgallery.org/pics/gui/desktop/full/win95.png)

!SLIDE
# L'innovation dans les langages de programmation

.notes innovation in programming languages
.notes automatic programming
.notes programming trop dur
.notes high level programming

!SLIDE
# Fortran
```fortran
C AREA OF A TRIANGLE - HERON'S FORMULA
C INPUT - CARD READER UNIT 5, INTEGER INPUT
C OUTPUT - LINE PRINTER UNIT 6, REAL OUTPUT
C INPUT ERROR DISPAY ERROR OUTPUT CODE 1 IN JOB CONTROL LISTING
      INTEGER A,B,C
      READ(5,501) A,B,C
  501 FORMAT(3I5)
      IF(A.EQ.0 .OR. B.EQ.0 .OR. C.EQ.0) STOP 1
      S = (A + B + C) / 2.0
      AREA = SQRT( S * (S - A) * (S - B) * (S - C))
      WRITE(6,601) A,B,C,AREA
  601 FORMAT(4H A= ,I5,5H  B= ,I5,5H  C= ,I5,8H  AREA= ,F10.2,12HSQUARE UNITS)
      STOP
      END
```

[Hello World](http://ideone.com/z1icOw)

.notes desc de programme en détail suffisant pour faire ce qu'il doit faire, toujours un programme
.notes raising level of abstraction
.notes Language pour faire des calculs scientifiques : on peut enfin écrire directement les formules mathématiques en notation usuelle.
.notes * for multiplications

!SLIDE
# COBOL
```cobol
      IDENTIFICATION DIVISION.
      PROGRAM-ID. HELLO-WORLD.
      PROCEDURE DIVISION.
          DISPLAY 'Hello, world'.
          STOP RUN.
```
.notes look more like English

!SLIDE
# BASIC
```basic
10 INPUT "What is your name: ", U$
20 PRINT "Hello "; U$
30 INPUT "How many stars do you want: ", N
40 S$ = ""
50 FOR I = 1 TO N
60 S$ = S$ + "*"
70 NEXT I
80 PRINT S$
90 INPUT "Do you want more stars? ", A$
100 IF LEN(A$) = 0 THEN GOTO 90
110 A$ = LEFT$(A$, 1)
120 IF A$ = "Y" OR A$ = "y" THEN GOTO 30
130 PRINT "Goodbye "; U$
140 END
```

.notes pour timesharing
.notes Fortran stripped down, quick to learn
.notes line number
.notes what's your name
.notes string processing
.notes input/output relationship, modal

!SLIDE
```
Basic - Business BASIC
  \
   - Microsoft Basic, Visual Basic
```

!SLIDE
# Visual Basic, VBA
```vb
Private Sub Form_Load()
    ' Execute a simple message box that says "Hello, World!"
    MsgBox "Hello, World!"
End Sub
```
.notes photo visual basic
.notes VBA Excel

!SLIDE
# Lisp
```
(DEFUN HELLO ()
  "HELLO WORLD"
)
```

.notes hello world Lisp

!SLIDE
# ALGOL 60
```algol
FLOATING POINT ALGOL TEST'
BEGIN REAL A,B,C,D'

READ D'

FOR A:= 0.0 STEP D UNTIL 6.3 DO
BEGIN
  PRINT PUNCH(3),££L??'
  B := SIN(A)'
  C := COS(A)'
  PRINT PUNCH(3),SAMELINE,ALIGNED(1,6),A,B,C'
END'
END'
```
.notes structured programming, blocks

!SLIDE
![GOTO](http://img.docstoccdn.com/thumb/orig/22207076.png)

!SLIDE
![BD xkcd sur GOTO](http://www.terminally-incoherent.com/blog/wp-content/uploads/2007/07/goto_1.Png)

.notes GOTO considered harmful
.notes programmers were against it

!SLIDE
* FORTRAN : scientifique
* COBOL : entreprise
* ALGOL -> ALGOL 68

!SLIDE
# Simplification

* CPL (Combined programming Language) ->
* ALGOL -> Pascal
* Pascal

.notes simplifier
.notes Pascal as teaching language
.notes pas assez modulaire

!SLIDE
```
FORTRAN BCPL  Pascal
    \     |     |
     \    |     |
      - B -     /
         \     /
          - C -
```

.notes Assembly Language VS High Level Language

!SLIDE
# Atari 2600
![Atari 2600](http://upload.wikimedia.org/wikipedia/commons/d/de/Atari-2600-Console.jpg)

!SLIDE
![Pitfall](http://www.wired.com/images_blogs/gamelife/images/2009/03/11/s_pitfall_1.png)

* aucun logiciel à bord
* 4 ou 8 ko
* 128 octets de mémoire vive

.notes Atari 2600, first computer most people had in house (j'avais un clone)
.notes 4K or 8K sur carte, pas de soft sur ordi
.notes console à 128 byes de rams
.notes - ca doit contenir tout l'état du jeux
.notes variations sur carte
.notes programme dans milions de foyers

!SLIDE
# Orientation objet

* ALGOL -> Simula -> Smalltalk
* Alan Kay, Xerox Park

![Alan Kay](http://upload.wikimedia.org/wikipedia/commons/2/2c/Alan_Kay_and_the_prototype_of_Dynabook,_pt._5_(3010032738).jpg)

!SLIDE
![Dynabook](http://facweb.cs.depaul.edu/sgrais/images/iP_Project/dynabook-01.gif)

!SLIDE
![ordinateur Xerox Park](http://media.rhizome.org/blog/8587/desktop-7.jpeg)

.notes dynabook ordin portable portable
.notes adaptation travail d'Engelbart
.notes display bitmap
.notes modern UI

!SLIDE
```smalltalk
result := a > b
  ifTrue:[ 'greater' ]
  ifFalse:[ 'less or equal' ]
```
```
Object subclass: #MessagePublisher
    instanceVariableNames: ''
    classVariableNames: ''
    poolDictionaries: ''
    category: 'Smalltalk Examples'
```

.notes a message b, retour objet true
.notes Smalltalk rejeté mais inspiré quasiment tout

!SLIDE
# C
```c
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```

!SLIDE
# Orientation Objet

* 1967 Simula
* 1972 Alan Kay commence à travailler sur Smalltalk
* 1980 sortie de Smalltalk
* 1985 sortie de C++
* 1995 sortie de Java

!SLIDE
# Bonds
* Plugboards
* Symbolic Assembly Language
* High Level Languages
* Structured Programming
* Object Oriented Programming

!SLIDE
# Simplication

Smalltalk -> Self

.notes prototypage vs classes

!SLIDE
# modèle "acteur"

* envoyer un message
* services web

.notes "send a message", processus indépendants
.notes message comme email
.notes service web est un acteur

!SLIDE
![Steve Jobs jeune](http://www.bumnew.com/wp-content/uploads/2011/10/young-steve-jobs.jpg)

.notes Steve Jobs demo Xerox Park, puis produit Machintosh

!SLIDE
# HyperCard
![HyperCard](http://www.creativeapplications.net/wp-content/uploads/2009/09/Hypercard.png)

!SLIDE
* stack" : pile de prototypes et cartes
* background": (prototypes) images, bouttons et champs
* card : un prototype, bouttons et champs
* button : texte ou image
* field: texte

.notes "l'avenir du logiciel"
.notes appli base de données
.notes didn't anticipate color
.notes didn't anticipate text links
.notes didn't anticipate networking

!SLIDE
```
on mouseUp
  puts "100, 100" into pos
  repeat with x = 1 to the nubmer of card buttons
    set the location of card button x to pos
    add 15 to item 1 of pos
  end repeat
end mouseUp
```

!SLIDE
# WWW

NLS de Engelbart's NLS -> Xanadu (Ted Nelson) -> HyperCard

Xanadu -> WWW

.notes HyperCard - HyperText
.notes Tim-Berners Lee ne savait rien sur Engelbart et peu sur Xanadu, mais en conséquence très simple et a pu l'implémenter

!SLIDE
# Langages de script

!SLIDE
# La guerre des navigateurs Web
```
WWW -> Mosaic -> Netscape
              -> Spyglass (acheté par Microsoft, devenu IE)
```

.notes Mosaic car beaucoup de protocoles

!SLIDE execute
# Javascript
```
window.addEventListerner('click', function(){
  prenom = prompt('Quel est votre prénom ?');
  alert(prenom);
});
```

.notes Java Scheme Self -> Javascript
.notes Netscape voulait OS distribué, bataille avec Microsoft
.notes destiné a programmeurs non-professionnels, comme Visual Basic
.notes Nom de code Mocha, puis Livescript
.notes 10 jours

!SLIDE
# Perl
![Larry Wall](http://www.linuxjournal.com/files/linuxjournal.com/linuxjournal/articles/033/3394/3394f1.jpg)

!SLIDE
```
while (<>) {
    if ($_ !~ /^$/) {
        $_ .= "\n"
    }
} continue {
    print or die "-p failed: $!\n";
}
```

!SLIDE
# Python
![Guido Van Rossum](http://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Guido_van_Rossum_OSCON_2006.jpg/200px-Guido_van_Rossum_OSCON_2006.jpg)

!SLIDE
# Ruby
![Matz](http://farm8.staticflickr.com/7132/7838834976_3076c3a7f5_z.jpg)

!SLIDE
```ruby
exit unless "restaurant".include? "aura"
```

```ruby
5.times { print "Hello Ruby !" }
```

```ruby
['toast', 'cheese', 'wine'].each { |food| print( food.capitalize ) }
```

```ruby
require 'net/http'
Net::HTTP.start( 'www.ruby-lang.org', 80 ) do |http|
  print( http.get( '/en/LICENSE.txt' ).body )
end
```

!SLIDE
[Why's (Poignant) Guide to Ruby](http://mislav.uniqpath.com/poignant-guide/)
![Why's (Poignant) Guide to Ruby](http://mislav.uniqpath.com/poignant-guide/images/2007-cover-shut.jpg)


.notes Depuis les débuts (COBOL) on a essayé de pouvoir se passer de programmeurs : fail
.notes Mais on a réussi à rendre la programmation accessible à des non spécialistes (FORTRAN était utilisé par des scientifiques qui n'étaient pas informaticiens de formation), cf. aussi formules dans les tableurs.
.notes Mettre en lien avec le "Worse is Better" : pas besoin de faire des programmes parfaits (L'auteur de Linux aurait eu une mauvaise note de Tanenbaum et j'aurais mis une mauvaise note technique à Facebook :) )
.notes -> Just Do It !
