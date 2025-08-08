### 🛠️ Βήμα 1: Εγκατάσταση Tailwind CLI

Αρχικά, εγκατέστησε το Tailwind CSS και το CLI του μέσω npm:

bash

```tsx
npm install tailwindcss @tailwindcss/cli
```

> Αν δεν έχεις εγκατεστημένο το Node.js, μπορείς να χρησιμοποιήσεις το CLI ως standalone executable χωρίς Node.
> 

### 📦 Βήμα 2: Δημιουργία αρχείου CSS εισόδου

Δημιούργησε ένα αρχείο CSS, π.χ. `src/input.css`, και πρόσθεσε την εντολή εισαγωγής του Tailwind:

css

```tsx
@import "tailwindcss";
```

### ⚙️ Βήμα 3: Εκκίνηση της διαδικασίας build

Τρέξε την CLI εντολή για να δημιουργήσεις το τελικό CSS αρχείο:

bash

```tsx
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

- `i`: δηλώνει το αρχείο εισόδου
- `o`: δηλώνει το αρχείο εξόδου
- `-watch`: παρακολουθεί για αλλαγές και κάνει αυτόματα rebuild

### 🌐 Βήμα 4: Χρήση του Tailwind στο HTML σου

Σύνδεσε το παραγόμενο CSS αρχείο στο HTML σου:

html

```tsx
<!doctype html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="./output.css" rel="stylesheet">
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
  </body>
</html>
```