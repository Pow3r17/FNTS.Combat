# FNTS.Combat
L'utilizzo è molto semplice: basta aggiungere  FNTS.Stats  all'attore.

Potenziale malinteso: nella documentazione, "Inc" è un'abbreviazione di "Increase"

var health = 100

function IncHealth(value){
  health = health + value
}

IncHealth(-10) // health = 90
IncHealth(50) // health = 140

Attributo
Gli attributi possono essere usati per gestire proprietà di base come attacco, difesa e salute massima. Per differenziare le fonti, gli attributi sono divisi in Base, Buff, e Equip.

![Image](https://github.com/user-attachments/assets/8b8619be-7084-4114-979f-244019305238)


Get Attribute restituirà la somma di Base, Buff, e Equip. Ad esempio, se la base di un carattere health è 100, Buff aggiunge 100 e Equip aggiunge 100, il massimo health del carattere sarà 300.

![Image](https://github.com/user-attachments/assets/91591b09-6d88-4d02-ab84-08e77b51ddef)


Regole degli attributi
In Rules, puoi configurare un attributo per influenzare il valore di un altro attributo. Ad esempio, 1 Strength = +10 Maximum Health & +1 Health Regen & +1 Attack Power

![Image](https://github.com/user-attachments/assets/942fe473-e439-4cfc-86e5-da2194317ccd)


carica gli attributi da DataTable

![Image](https://github.com/user-attachments/assets/9a95a681-f54c-471e-a473-c4a8fe2a3f5c)


Regole
Le regole variabili sono le regole che si applicano quando cambiano gli attributi.

![333](https://github.com/user-attachments/assets/5f1e53a9-75bf-4382-8511-547182aa82a5)

Tipo	Descrizione
None	Non fare nulla
AddToAttribute	Questa variabile diventerà parte dell'attributo, ovvero GetAttribute = Base + Buff + Equipaggiamento + Variabile
Auto-Adjust	Quando l'Attributo cambia, anche la Variabile cambierà di conseguenza. Ad esempio, se l'Attributo aumenta del 10%, anche la Variabile aumenterà del 10%.

Eventi
immagine

Evento	Descrizione
Event_OnBeginPlay	Il componente inizia l'inizializzazione
Event_OnInitialized	Il componente completa l'inizializzazione
Event_OnAttributeChanged	Quando cambia un attributo
Event_OnVariableChanged	Quando una variabile cambia
Event_OnFloatValueChanged	Quando cambia un FloatValue
Event_OnNameValueChanged	Quando cambia un NameValue
Event_OnTagValueChanged	Quando cambia un TagValue
Event_OnVectorValueChanged	Quando cambia un VectorValue
Event_OnRotatorValueChanged	Quando cambia un RotatorValue
Event_OnTransformValueChanged	Quando cambia un TransformValue
Event_OnSaveGame	Quando ci si prepara a salvare il gioco
Event_OnSavedGame	Quando il gioco è salvato
Event_OnLoadGame	Quando ci si prepara a caricare il gioco
Event_OnLoadedGame	Quando il gioco è caricato
