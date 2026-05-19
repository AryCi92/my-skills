```markdown
---
name: angular-form-generator
description: Genera form Angular standalone utilizzando Reactive Forms, Tailwind CSS e gli standard aziendali per validazione, accessibilità e struttura del codice.
---

# Angular Form Generator

Questa skill genera form Angular seguendo gli standard aziendali di architettura, UX/UI e accessibilità.

## Quando utilizzare questa skill

Usa questa skill quando l’utente:

- Chiede di creare un form Angular
- Richiede login form, registration form o CRUD form
- Ha bisogno di validazioni standardizzate
- Vuole utilizzare Reactive Forms
- Richiede form responsive con Tailwind CSS
- Necessita di componenti standalone Angular
- Vuole una struttura coerente con gli standard aziendali

---

# Standard obbligatori

Quando generi codice Angular:

- Usa sempre standalone components
- Usa sempre Reactive Forms
- Usa `FormBuilder`
- Non usare `ngModel`
- Evita logica complessa nel template
- Usa tipizzazione forte
- Usa Tailwind CSS per il layout
- Mantieni naming chiaro e consistente
- Centralizza le validazioni quando possibile
- Mantieni il codice leggibile e modulare

---

# Regole UX/UI

Tutti i form devono:

- Avere label accessibili
- Mostrare errori sotto il campo associato
- Evidenziare chiaramente i campi invalidi
- Avere spacing coerente
- Essere responsive
- Usare CTA ben visibili
- Supportare keyboard navigation
- Evitare layout troppo complessi

---

# Regole di validazione

Quando appropriato:

- Usa `Validators.required`
- Usa `Validators.email`
- Usa `Validators.minLength`
- Usa validazioni custom riutilizzabili
- Mostra messaggi di errore chiari e brevi
- Mostra errori solo dopo `touched` o `dirty`

---

# Struttura attesa

Quando generi un form:

1. Crea component standalone
2. Definisci il Reactive Form nel TypeScript
3. Usa `FormBuilder`
4. Implementa validazioni
5. Genera template HTML pulito
6. Usa classi Tailwind coerenti
7. Implementa submit handler tipizzato
8. Mantieni separazione chiara tra logica e UI

---

# Convenzioni Angular

Preferisci:

- `inject()` invece di constructor injection quando appropriato
- Signals quando utili
- `ChangeDetectionStrategy.OnPush`
- Struttura feature-based
- Computed e helper methods piccoli e riutilizzabili

Evita:

- subscribe annidati
- `any`
- logica nel template
- componenti troppo grandi
- duplicazione delle validazioni

---

# Esempio richieste valide

Questa skill è ideale per richieste come:

- "Crea un login form Angular"
- "Genera un form CRUD utenti"
- "Crea un form checkout responsive"
- "Genera un form con validazioni custom"
- "Crea un registration form con conferma password"

---

# Output atteso

L’output deve includere quando necessario:

- componente TypeScript
- template HTML
- validazioni
- tipi forti
- classi Tailwind
- gestione submit
- gestione errori
- struttura leggibile e pronta per produzione

---

# Skill correlate

Questa skill può essere utilizzata insieme a:

- angular-api-service-standard
- angular-table-generator
- angular-auth-flow
- angular-validation-utils

---

# Come comportarsi

Prima di generare il form:

1. Analizza il tipo di form richiesto
2. Identifica campi e validazioni necessarie
3. Determina eventuali dipendenze API
4. Genera una struttura coerente con gli standard aziendali
5. Mantieni il codice riutilizzabile e facilmente estendibile

---

# Quando non utilizzare questa skill

Non usare questa skill quando:

- Il form non è Angular
- L’utente richiede template-driven forms
- La richiesta riguarda solo styling statico
- Non è necessaria interazione tramite form

In questi casi utilizza skill più appropriate.
```