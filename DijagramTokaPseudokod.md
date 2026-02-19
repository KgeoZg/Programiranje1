---
layout: default
title: Dijagram toka i pseudokod
nav_order: 1
has_children: true
---

# Dijagram toka i pseudokod

<p align="justify">Dijagram toka i pseudokod predstavljaju načine prikaza algoritamskog razmišljanja koji omogućuju planiranje i analizu rješenja prije njegove programske implementacije. Na taj se način pristup rješavanju zadatka radi neovisno o programskom jeziku koji će se koristiti za implementaciju algoritma u digitalnom okruženju.</p>
<p><strong>Po završetku ovih vježbi student će moći:</strong></p>

1. Razumjeti pristup analizi zahtjeva zadatka
2. Formirati analitičko razmišljanje
3. Razumjeti i znati primijeniti dijagram toka/pseudokod za rješavanje problema


<details>
    <summary><strong>Osnovni koncepti</strong></summary>

    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; align-items: start;">
        <div class="column">
            <p><strong>DIJAGRAM TOKA</strong></p>
            <p style="text-align: justify;">Dijagram toka je grafički prikaz algoritma koji pomaže programeru u boljem shvaćanju problema koji se rješava. Koriste se grafičke varijable (npr. pravokutnik) koji olakšavaju shvaćanje pristupa rješavanju problema.</p>
            <div style="text-align: center;">
                <img src="{{ '/assets/images/1_DijagramToka.png' | relative_url }}" width="100">
            </div>
        </div>

        <div class="column">
            <p><strong>PSEUDOKOD</strong></p>
            <p style="text-align: justify;">Pseudokod je drugačiji pristup boljem shvaćanju problema kojeg programer mora riješiti. Što je problem kompleksniji, to dijagram toka postaje sve masivniji.

            </p>
            <div style="text-align: center;">
                <img src="{{ '/assets/images/2_Pseudokod.png' | relative_url }}" width="100">
            </div>
        </div>
    </div>

    <p style="margin-top: 20px;">Odabir načina formalizacije algoritamskog razmišljanja ovisi o osobi koja rješava zadatak i zahtjevnosti zadatka.</p>

</details>

<details>
    <summary><strong>Primjer riješenog zadatka</strong></summary>
        <p><strong>Zadatak:</strong> Sastaviti dijagram toka i/ili pseudokod za kod koji računa površinu katastarske čestice pravokutnog oblika s proizvoljnim duljinama stranica a i b te ispisuje izračunatu površine.</p>
        <p><strong>Način razmišljanja</strong></p>
        <ul>
        <li>Katastarska čestica je pravokutnog oblika - površina se računa kao P=a*b</li>
        <li>Proizvoljna duljina stranica - vrijednosti duljina stranica su proizvoljne i popunjavaju se prilikom sastavljanja koda </li>
        <li>Kako bi se budući kod mogao primijeniti za računanje površine bilo koje katastarske čestice pravokutnog oblika (s različitim vrijednostima duljina stranica) kod mora koristiti varijable umjesto konkretnih brojeva: uvode se varijable a i b u koje će se pohraniti proizvoljna vrijednost duljina stranica pravokutnika</li>
        <li>S obzirom da površina pravokutnika ovisi o vrijednostima duljina stranica, potrebno je definirati varijablu u koju će se pohraniti izračunata vrijednost (rezultat). Bez korištenja varijable za izračunatu vrijednost, kod ne bi bio primjenjiv za računanje površine drugih pravokutnih čestica i vrijednost površine bi morala biti unaprijed poznata, a ne izračunata u zadatku</li>
        <li>Temeljem vrijednosti duljina stranica pohranjenih u varijable a i b, izračunati površinu katastarske čestice prema formuli P=a*b.</li>
        <li>Ispisati izračunatu vrijednost površine</li>
        </ul>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; align-items: start;">
            <div class="column">    
                <p><strong>Predloženi dijagram toka</strong></p>
                <div class="hotspot-wrapper">
                    <div class="hotspot-container" style="width: 100px; margin: 0 auto; display: inline-block;">
                        <!-- 1. Your Main Image -->
                            <img src="{{ '/assets/images/3_Ogledni zadatak 1.png' | relative_url}}" alt="Dijagram toka">


                        <!-- 2. Početak Hotspot Dot (Positioned at 2.5% from top, 2% from right) -->
                        <div class="hotspot" style="top: 2.5%; right: -25%;">
                            <div class="hotspot--inner" style="background: #fbb300;"></div>
                            <div class="hotspot--content">
                                <h4>Početak programa</h4>
                                <p>Početak se označava ovalom i predstavlja točku od koje kreće program (izvršavanje koda). Svaki dijagram toka mora imati početak.</p>
                            </div>
                        </div>

                        <!-- 3. Ulaz Hotspot Dot -->
                        <div class="hotspot" style="top: 24%; right: -25%;">
                            <div class="hotspot--inner" style="background: #fbb300;"></div>
                            <div class="hotspot--content">
                                <h4>Ulaz</h4>
                                <p>Ulazna radnja označava ulazne podatke koje daje korisnik, a koji su nužni za izvršavanje koda.<br>
                                Kako je cilj programa biti što više univerzalan, tj. podržavati automatizirano izvršavanje neovisno o unesenim vrijednostima, umjesto konkretnih brojeva u ulaz se upisuju nazivi varijabli u koje se te vrijednosti pohranjuju. Iznimno, konkretni brojevi se upisuju kada se radi o konstantnim vrijednostima, npr. vrijednost broja Pi. U ovom slučaju, ulaz su varijable <em>a</em> i <em>b</em> koje služe za pohranjivanje vrijednosti duljina stranica katastarske čestice.<br>
                                Ulaz se u dijagramu toka prikazuje trapezom kojem je kraća stranica dolje (zamisliti kao lijevak koji podatke ulijeva u program).</p>
                            </div>
                        </div>

                        <!-- 4. Operacija/obrada Hotspot Dot -->
                        <div class="hotspot" style="top: 46%; right: -25%;">
                            <div class="hotspot--inner" style="background: #fbb300;"></div>
                            <div class="hotspot--content">
                                <h4>Obrada podataka</h4>
                                <p>Radnje unutar algoritma u dijagramu toka označavaju se pravokutnikom. Jedan pravokutnik može sadržavati jednu ili više operacija koje odgovaraju radnjama u tom koraku algoritma.<br>
                                Kako je ishod radnje u algoritmu nova vrijednost, nju je potrebno pohraniti u varijablu iz koje se ta vrijednost po potrebi može pozivati (primjerice za ispis ili kasnije korištenje). U ovom slučaju radnja označava računanje površine pa je zapis u pravokutniku oblika P=a*b. </p>
                            </div>
                        </div>

                        <!-- 5. Izlaz Hotspot Dot -->
                        <div class="hotspot" style="top: 66%; right: -25%;">
                            <div class="hotspot--inner" style="background: #fbb300;"></div>
                            <div class="hotspot--content">
                                <h4>Izlaz</h4>
                                <p>Izlaz predstavlja ono što je rezultat programa. Primjerice, izlaz može biti ispisivanje teksta ili neke od izračunatih vrijednost.<br>U konkretnom primjeru, izlaz predstavlja izračunatu površinu katastarske čestice, a koja je pohranjena u varijabli P.<br>
                                Izlaz se u dijagramu toka označava trapezom kojem je kraća stranica gore (zamisliti kao obrnuti lijevak koji izlijeva podatke iz programa) </p>
                            </div>
                        </div>

                        <!-- 6. Kraj Hotspot Dot -->
                        <div class="hotspot" style="top: 89%; right: -25%;">
                            <div class="hotspot--inner" style="background: #fbb300;"></div>
                            <div class="hotspot--content">
                                <h4>Kraj programa</h4>
                                <p>Kraj predstavlja završetak programa. Kao i početak, sastavni je dio zapisa algoritma u dijagramu toka.<br>
                                Kraj se u dijagramu toka označava ovalom, isto kao i početak.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="column">
            <p><strong>Predloženi pseudokod</strong></p>
            <div class="hotspot-wrapper">
                <div class="hotspot-container" style="width: 100px; margin: 0 auto; display: inline-block;">
                    <!-- 1. Your Main Image -->
                        <img src="{{ 'assets\images\3_Ogledni zadatak 1 pseudokod.png' | relative_url}}" alt="Dijagram toka">


                    <!-- 2. Početak Hotspot Dot (Positioned at 2.5% from top, 2% from right) -->
                    <div class="hotspot" style="top: -3%; right: -25%;">
                        <div class="hotspot--inner" style="background: #fbb300;"></div>
                        <div class="hotspot--content">
                            <h4>Početak programa</h4>
                            <p>Umjesto grafičkih varijabli, pseudokod koristi ključne riječi za označavanje dijelova algoritma. U pseudokodu, početak se zapisuje rječju <em>početak</em>, a označava podvlačenjem.</p>
                        </div>
                    </div>

                    <!-- 3. Ulaz Hotspot Dot -->
                    <div class="hotspot" style="top: 19%; right: -25%;">
                        <div class="hotspot--inner" style="background: #fbb300;"></div>
                        <div class="hotspot--content">
                            <h4>Ulaz</h4>
                            <p>Ulaz se u pseudokodu označava podvučenom rječju <em>ulaz</em> pri čemu su u zagradu dodane oznake varijabli. Kako pseudokod služi za pisanje koda, jednostavnost čitanja, tj. struktura zapisa postiže se uvlačenjem retka. Uvučeni redak označava koje radnje se događaju unutar kojeg dijela algoritma. Primjerice, cijelo rješenje zadatka se događa između početka i kraja programa pa zapis pseudokoda mora biti uvučen u odnosu na početak i kraj pseudokoda.<br>
                            Osim uvlačenja retka, pseudokod koristi i elemente programskog jezika kojima se radi razgraničavanje linija koda tj. instrukcija koda. Drugim riječima, potrebno je naznačiti kraj radnji pojedine linije budućeg koda što se u pseudokodu označava s <strong>;</strong>.<br>
                            U konkretnom primjeru, ulazne vrijednosti za rješavanje zadatka su duljine stranica a i b, pa je zapis pseudokoda oblika "<u>ulaz</u> (a,b);" </p>
                        </div>
                    </div>

                    <!-- 4. Operacija/obrada Hotspot Dot -->
                    <div class="hotspot" style="top: 41%; right: -25%;">
                        <div class="hotspot--inner" style="background: #fbb300;"></div>
                        <div class="hotspot--content">
                            <h4>Obrada podataka</h4>
                            <p>Radnje unutar algoritma u imaju klasičan oblik govornog jezika, npr. zapisa formula. Ono što je specifično za zapis pseudokoda u odnosu na kod je što se prije znaka jednakosti u jednadžbi stavlja oznaka dvotočja, <strong>:=</strong> umjesto =. Ponovno, zapis kraja linije koda označava se s <strong>;</strong> </p>
                        </div>
                    </div>

                    <!-- 5. Izlaz Hotspot Dot -->
                    <div class="hotspot" style="top: 62%; right: -25%;">
                        <div class="hotspot--inner" style="background: #fbb300;"></div>
                        <div class="hotspot--content">
                            <h4>Izlaz</h4>
                            <p>Izlaz se u pseudokodu označava slično kao ulaz, ali s ključnom rječju <u>izlaz</u>, a koristi se u kombinaciji s izlaznom vrijednosti zapisanoj u zagradi, npr <u>izlaz</u> (p);. </p>
                        </div>
                    </div>

                    <!-- 6. Kraj Hotspot Dot -->
                    <div class="hotspot" style="top: 84%; right: -25%;">
                        <div class="hotspot--inner" style="background: #fbb300;"></div>
                        <div class="hotspot--content">
                            <h4>Kraj programa</h4>
                            <p>Kraj pseudokoda označava se ključnom rječju kraj, odnosno kao <u>kraj</u>.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</details>
