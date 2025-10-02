<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "c27e2a2e9055910545560e8472b341d8",
  "translation_date": "2025-10-02T08:07:44+00:00",
  "source_file": "13-agent-memory/README.md",
  "language_code": "ro"
}
-->
# Memorie pentru Agenți AI 
[![Memorie pentru Agenți](../../../translated_images/lesson-13-thumbnail.959e3bc52d210c64a614a3bece6b170a2c472138dc0a14c7fbde07306ef95ae7.ro.png)](https://youtu.be/QrYbHesIxpw?si=qNYW6PL3fb3lTPMk)

Când discutăm despre beneficiile unice ale creării agenților AI, două lucruri sunt în principal menționate: abilitatea de a apela instrumente pentru a finaliza sarcini și capacitatea de a se îmbunătăți în timp. Memoria stă la baza creării unui agent auto-îmbunătățit care poate oferi experiențe mai bune utilizatorilor noștri.

În această lecție, vom analiza ce înseamnă memoria pentru agenții AI și cum o putem gestiona și utiliza în beneficiul aplicațiilor noastre.

## Introducere

Această lecție va acoperi:

• **Înțelegerea memoriei agenților AI**: Ce este memoria și de ce este esențială pentru agenți.

• **Implementarea și stocarea memoriei**: Metode practice pentru adăugarea capacităților de memorie agenților AI, cu accent pe memoria pe termen scurt și lung.

• **Crearea agenților AI auto-îmbunătățiți**: Cum permite memoria agenților să învețe din interacțiunile anterioare și să se îmbunătățească în timp.

## Obiective de învățare

După finalizarea acestei lecții, veți ști cum să:

• **Distingiți între diferitele tipuri de memorie ale agenților AI**, inclusiv memoria de lucru, pe termen scurt și pe termen lung, precum și formele specializate, cum ar fi memoria de tip "persona" și memoria episodică.

• **Implementați și gestionați memoria pe termen scurt și lung pentru agenții AI** utilizând cadrul Semantic Kernel, instrumente precum Mem0 și memoria Whiteboard, și integrarea cu Azure AI Search.

• **Înțelegeți principiile din spatele agenților AI auto-îmbunătățiți** și cum contribuie sistemele robuste de gestionare a memoriei la învățarea și adaptarea continuă.

## Înțelegerea memoriei agenților AI

În esență, **memoria pentru agenții AI se referă la mecanismele care le permit să rețină și să recheme informații**. Aceste informații pot include detalii specifice despre o conversație, preferințele utilizatorului, acțiuni anterioare sau chiar tipare învățate.

Fără memorie, aplicațiile AI sunt adesea fără stare, ceea ce înseamnă că fiecare interacțiune începe de la zero. Acest lucru duce la o experiență repetitivă și frustrantă pentru utilizator, în care agentul "uită" contextul sau preferințele anterioare.

### De ce este importantă memoria?

Inteligența unui agent este profund legată de abilitatea sa de a rechema și utiliza informațiile din trecut. Memoria permite agenților să fie:

• **Reflexivi**: Să învețe din acțiunile și rezultatele anterioare.

• **Interactivi**: Să mențină contextul pe parcursul unei conversații în desfășurare.

• **Proactivi și Reactivi**: Să anticipeze nevoile sau să răspundă adecvat pe baza datelor istorice.

• **Autonomi**: Să opereze mai independent, bazându-se pe cunoștințele stocate.

Scopul implementării memoriei este de a face agenții mai **fiabili și capabili**.

### Tipuri de memorie

#### Memoria de lucru

Gândiți-vă la aceasta ca la o foaie de hârtie pe care un agent o folosește în timpul unei singure sarcini sau procese de gândire. Aceasta păstrează informațiile imediate necesare pentru a calcula pasul următor.

Pentru agenții AI, memoria de lucru captează adesea cele mai relevante informații dintr-o conversație, chiar dacă istoricul complet al chatului este lung sau trunchiat. Se concentrează pe extragerea elementelor cheie, cum ar fi cerințele, propunerile, deciziile și acțiunile.

**Exemplu de memorie de lucru**

În cazul unui agent de rezervare a călătoriilor, memoria de lucru ar putea capta cererea curentă a utilizatorului, cum ar fi "Vreau să rezerv o călătorie la Paris". Această cerință specifică este păstrată în contextul imediat al agentului pentru a ghida interacțiunea curentă.

#### Memoria pe termen scurt

Acest tip de memorie reține informațiile pe durata unei singure conversații sau sesiuni. Este contextul chatului curent, permițând agentului să facă referire la replicile anterioare din dialog.

**Exemplu de memorie pe termen scurt**

Dacă un utilizator întreabă, "Cât ar costa un zbor spre Paris?" și apoi continuă cu "Dar cazarea acolo?", memoria pe termen scurt asigură că agentul știe că "acolo" se referă la "Paris" în cadrul aceleiași conversații.

#### Memoria pe termen lung

Aceasta este informația care persistă pe parcursul mai multor conversații sau sesiuni. Permite agenților să-și amintească preferințele utilizatorului, interacțiunile anterioare sau cunoștințele generale pe perioade extinse. Este importantă pentru personalizare.

**Exemplu de memorie pe termen lung**

O memorie pe termen lung ar putea stoca faptul că "Ben se bucură de schi și activități în aer liber, îi place cafeaua cu vedere la munte și dorește să evite pârtiile avansate de schi din cauza unei accidentări anterioare". Aceste informații, învățate din interacțiuni anterioare, influențează recomandările în sesiunile viitoare de planificare a călătoriilor, făcându-le extrem de personalizate.

#### Memoria de tip "Persona"

Acest tip de memorie specializată ajută un agent să dezvolte o "personalitate" sau un "rol" consistent. Permite agentului să-și amintească detalii despre sine sau despre rolul său intenționat, făcând interacțiunile mai fluide și mai concentrate.

**Exemplu de memorie pe termen lung**

Dacă agentul de călătorii este conceput să fie un "planificator expert de schi", memoria de tip "persona" ar putea întări acest rol, influențând răspunsurile sale pentru a se alinia cu tonul și cunoștințele unui expert.

#### Memoria de flux/episodică

Această memorie stochează secvența de pași pe care un agent îi face în timpul unei sarcini complexe, inclusiv succesele și eșecurile. Este ca și cum ar "ține minte" episoade specifice sau experiențe anterioare pentru a învăța din ele.

**Exemplu de memorie episodică**

Dacă agentul a încercat să rezerve un anumit zbor, dar a eșuat din cauza indisponibilității, memoria episodică ar putea înregistra acest eșec, permițând agentului să încerce zboruri alternative sau să informeze utilizatorul despre problemă într-un mod mai informat în timpul unei încercări ulterioare.

#### Memoria de entitate

Aceasta implică extragerea și reținerea entităților specifice (cum ar fi persoane, locuri sau lucruri) și evenimente din conversații. Permite agentului să construiască o înțelegere structurată a elementelor cheie discutate.

**Exemplu de memorie de entitate**

Dintr-o conversație despre o călătorie anterioară, agentul ar putea extrage "Paris", "Turnul Eiffel" și "cină la restaurantul Le Chat Noir" ca entități. Într-o interacțiune viitoare, agentul ar putea să-și amintească "Le Chat Noir" și să ofere să facă o nouă rezervare acolo.

#### RAG Structurat (Generare Augmentată prin Regăsire)

Deși RAG este o tehnică mai largă, "RAG Structurat" este evidențiat ca o tehnologie de memorie puternică. Acesta extrage informații dense și structurate din diverse surse (conversații, e-mailuri, imagini) și le folosește pentru a îmbunătăți precizia, regăsirea și viteza răspunsurilor. Spre deosebire de RAG clasic, care se bazează exclusiv pe similaritatea semantică, RAG Structurat lucrează cu structura inerentă a informațiilor.

**Exemplu de RAG Structurat**

În loc să se bazeze doar pe potrivirea cuvintelor cheie, RAG Structurat ar putea analiza detaliile unui zbor (destinație, dată, oră, companie aeriană) dintr-un e-mail și să le stocheze într-un mod structurat. Acest lucru permite interogări precise, cum ar fi "Ce zbor am rezervat spre Paris marți?".

## Implementarea și stocarea memoriei

Implementarea memoriei pentru agenții AI implică un proces sistematic de **gestionare a memoriei**, care include generarea, stocarea, regăsirea, integrarea, actualizarea și chiar "uitarea" (sau ștergerea) informațiilor. Regăsirea este un aspect deosebit de crucial.

### Instrumente specializate pentru memorie

O modalitate de a stoca și gestiona memoria agenților este utilizarea unor instrumente specializate precum Mem0. Mem0 funcționează ca un strat de memorie persistentă, permițând agenților să recheme interacțiuni relevante, să stocheze preferințele utilizatorilor și contextul factual și să învețe din succese și eșecuri în timp. Ideea este că agenții fără stare devin agenți cu stare.

Funcționează printr-un **pipeline de memorie în două faze: extragere și actualizare**. Mai întâi, mesajele adăugate la firul unui agent sunt trimise către serviciul Mem0, care utilizează un model de limbaj mare (LLM) pentru a rezuma istoricul conversației și a extrage noi amintiri. Ulterior, o fază de actualizare condusă de LLM determină dacă să adauge, să modifice sau să șteargă aceste amintiri, stocându-le într-un depozit de date hibrid care poate include baze de date vectoriale, grafice și cheie-valoare. Acest sistem suportă, de asemenea, diverse tipuri de memorie și poate încorpora memoria grafică pentru gestionarea relațiilor dintre entități.

### Stocarea memoriei cu RAG

Dincolo de instrumentele specializate de memorie precum Mem0, puteți utiliza servicii robuste de căutare precum **Azure AI Search ca backend pentru stocarea și regăsirea amintirilor**, în special pentru RAG structurat.

Acest lucru vă permite să fundamentați răspunsurile agentului cu propriile date, asigurând răspunsuri mai relevante și mai precise. Azure AI Search poate fi utilizat pentru a stoca amintiri specifice utilizatorului despre călătorii, cataloage de produse sau orice altă cunoaștere specifică domeniului.

Azure AI Search suportă capabilități precum **RAG Structurat**, care excelează în extragerea și regăsirea informațiilor dense și structurate din seturi mari de date, cum ar fi istoricul conversațiilor, e-mailurile sau chiar imaginile. Acest lucru oferă "precizie și regăsire supraomenească" comparativ cu abordările tradiționale de împărțire a textului și încorporare.

## Crearea agenților AI auto-îmbunătățiți

Un model comun pentru agenții auto-îmbunătățiți implică introducerea unui **"agent de cunoaștere"**. Acest agent separat observă conversația principală dintre utilizator și agentul primar. Rolul său este să:

1. **Identifice informații valoroase**: Să determine dacă vreo parte a conversației merită salvată ca cunoaștere generală sau preferință specifică utilizatorului.

2. **Extragă și rezumeze**: Să distileze esența învățării sau preferinței din conversație.

3. **Stocheze într-o bază de cunoștințe**: Să persisteze informațiile extrase, adesea într-o bază de date vectorială, astfel încât să poată fi regăsite mai târziu.

4. **Augmenteze interogările viitoare**: Când utilizatorul inițiază o nouă interogare, agentul de cunoaștere regăsește informațiile relevante stocate și le adaugă la promptul utilizatorului, oferind context crucial agentului primar (similar cu RAG).

### Optimizări pentru memorie

• **Gestionarea latenței**: Pentru a evita încetinirea interacțiunilor utilizatorului, se poate utiliza inițial un model mai ieftin și mai rapid pentru a verifica rapid dacă informațiile sunt valoroase pentru stocare sau regăsire, invocând procesul mai complex de extragere/regăsire doar atunci când este necesar.

• **Întreținerea bazei de cunoștințe**: Pentru o bază de cunoștințe în creștere, informațiile utilizate mai rar pot fi mutate în "stocare rece" pentru a gestiona costurile.

## Aveți mai multe întrebări despre memoria agenților?

Alăturați-vă [Discordului Azure AI Foundry](https://aka.ms/ai-agents/discord) pentru a întâlni alți cursanți, a participa la ore de consultanță și a obține răspunsuri la întrebările despre agenții AI.

---

**Declinare de responsabilitate**:  
Acest document a fost tradus folosind serviciul de traducere AI [Co-op Translator](https://github.com/Azure/co-op-translator). Deși ne străduim să asigurăm acuratețea, vă rugăm să fiți conștienți că traducerile automate pot conține erori sau inexactități. Documentul original în limba sa maternă ar trebui considerat sursa autoritară. Pentru informații critice, se recomandă traducerea profesională realizată de un specialist. Nu ne asumăm responsabilitatea pentru eventualele neînțelegeri sau interpretări greșite care pot apărea din utilizarea acestei traduceri.