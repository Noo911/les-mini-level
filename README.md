# Mini-level

**Naam: Yunus** <!-- jouw naam -->  
**Klas: sd1c** <!-- jouw klas -->
**Datum: 24-10-2026** <!-- datum van inleveren -->  
**Les:6** GDV Les 6

---

## Wat heb ik gemaakt?
ik heb een mini level gemaakt waar je een key moet vinden om de deur te openen
<!-- Beschrijf kort je mini-level. Wat moet de speler doen? Wat is het doel? -->

...

---

## Screenshot / GIF van je level

<!-- Voeg hieronder een screenshot of een GIF toe van je werkende level.
     Sleep het bestand naar deze map en gebruik dan de syntax hieronder. -->

![aaa](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExb2toZXpsZWpodzZnOWpnZGdpYmhvb3g4eGxxbWllcnlwYTR4Z3hrNCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/anxObL50n9hfnPm1Bm/giphy.gif)

<!-- Tip: gebruik ShareX, LICEcap of de ingebouwde Xbox Game Bar (Win+G) om een GIF op te nemen. -->

---

## Bewegend object

<!-- Welk object beweegt en hoe heb je dat gedaan? -->

...

```csharp
private float rotateSpeed = 5f;

void Update()
{
    transform.Rotate(10, rotateSpeed * Time.deltaTime, 0);
}
```

---

## Collider of trigger

<!-- Welk object heeft een collider of trigger, en wat gebeurt er? -->

...

```csharp
    public GameObject door;
    public bool hasKey = false;

private void OnTriggerEnter(Collider other)
{
        if (other.CompareTag("Key"))
        {
            hasKey = true;
            Destroy(other.gameObject);
        }

        if (other.CompareTag("Door") && hasKey == true)
        {
            door.SetActive(false);
        }
}
```

---

## Logica met `if` of `switch`

dus hasKey = true; betekent wanneer de player de key opakt gaat de key weg en dan heeft hij hem en met de door.setactive betekent wanneer de key daar is wordt het pas active

...

```csharp
// Plak hier het stuk code met jouw if- of switch-logica.
if ()
{
        if (other.CompareTag("Key"))
        {
            hasKey = true;
            Destroy(other.gameObject);
        }

        if (other.CompareTag("Door") && hasKey == true)
        {
            door.SetActive(false);
        }
}
```

---

## Eigen extra idee

<!-- Wat is jouw eigen extra feature? Beschrijf wat het doet en hoe je het hebt gebouwd. -->

...

```csharp
// Optioneel: plak hier de bijbehorende code.

```
me eigen idee was het om damage blocks toe te voegen en opstakels maken
---

## Evaluatie

### Wat ging goed? en waarom?

<!-- Wat lukte je makkelijk of waar ben je trots op? -->
alles ging best goed omdat ik snapte wel alles
...

### Wat vond je lastig? en waarom?

<!-- Waar liep je tegenaan? Hoe heb je het opgelost (of niet)? -->
terwijl ik de key maketen hij ging niet conecten naar de block
...

### Wat zou je een volgende keer anders doen?

<!-- Wat heb je geleerd? -->
misschien een uitgebreide level maken
...
