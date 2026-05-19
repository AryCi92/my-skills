---
name: find-skills
description: Aiuta a identificare e utilizzare le skill aziendali più rilevanti per attività di sviluppo, UI/UX, architettura, API, testing e workflow. Questa skill deve essere utilizzata ogni volta che una richiesta può beneficiare di una o più skill aziendali installabili.
---

# Find Skills

Questa skill aiuta a individuare e utilizzare le skill più rilevanti disponibili nell'ecosistema interno aziendale.

## Quando utilizzare questa skill

Usa questa skill quando l'utente:

* Chiede come implementare una feature o un workflow
* Richiede aiuto per generare componenti Angular, form, tabelle, API o UI
* Ha bisogno di linee guida architetturali, pattern o best practice
* Menziona attività legate a frontend, backend, UX/UI, testing, accessibilità o automazione
* Chiede se esiste già una skill riutilizzabile
* Vuole velocizzare lo sviluppo utilizzando tooling standardizzato aziendale
* Ha bisogno di suggerimenti su skill che funzionano bene insieme

---

# Come identificare le skill rilevanti

Prima di generare codice o suggerimenti:

1. Analizza attentamente la richiesta dell'utente
2. Identifica:

   * il dominio tecnico
   * il tipo di attività
   * l'output atteso
3. Determina se una o più skill aziendali dovrebbero essere utilizzate
4. Preferisci sempre skill standardizzate aziendali quando disponibili
5. Suggerisci skill correlate se possono completare il workflow

---

# Skill disponibili

## angular-api-service-standard

Descrizione:
Generate Angular API services following company standards using HttpClient, typing, and best practices

Ideale per:

* Generate Angular API services following company standards using HttpClient, typing, and best practices

Keywords:

* general

Comando installazione:

```bash
npx skills add https://github.com/AryCi92/my-skills --skill angular-api-service-standard
```

---

## angular-form-generator

Descrizione:
Genera form Angular standalone utilizzando Reactive Forms, Tailwind CSS e gli standard aziendali per validazione, accessibilità e struttura del codice.

Ideale per:

* Genera form Angular standalone utilizzando Reactive Forms, Tailwind CSS e gli standard aziendali per validazione, accessibilità e struttura del codice.

Keywords:

* general

Comando installazione:

```bash
npx skills add https://github.com/AryCi92/my-skills --skill angular-form-generator
```

---

---

# Come presentare le skill

Quando vengono trovate skill rilevanti:

1. Spiega brevemente perché la skill è pertinente
2. Suggerisci skill complementari quando utile
3. Fornisci il comando di installazione
4. Incentiva l'utilizzo di workflow e pattern standardizzati aziendali

Esempio:

```text
Ho trovato una skill aziendale che corrisponde alla tua richiesta.

La skill trovata aiuta a generare componenti seguendo gli standard aziendali.

Installala con:

npx skills add <repo-url> --skill <skill-name>
```

---

# Quando non vengono trovate skill rilevanti

Se non esiste una skill adatta:

1. Comunica che al momento non è disponibile una skill aziendale compatibile
2. Offri comunque supporto utilizzando le capacità generali del modello
3. Suggerisci eventualmente la creazione di una nuova skill riutilizzabile per quel caso d'uso