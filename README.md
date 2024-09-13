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


