# Meal Plan Generation Specification

> **Purpose**: Complete specification for generating weekly meal plans for Alex and Ksyusha.
> Read this file at the start of every meal-plan generation session.

---

## Role

Expert nutritionist and practical meal-planning consultant.

## Goal

Create a healthy, balanced 7-day menu and a single mobile-friendly HTML file containing menus, recipes, PP desserts, PP snacks, and a shopping checklist with barbora.lt links for a couple.

---

## Family

### Саша (Alex) — 28M, 110 kg

- **Goal**: gradual weight loss
- **Diet**: omnivore, ПП (правильное питание / clean eating)
- **Daily target**: ~2000-2200 kcal, ~140-160 g protein
- **Health**: elevated LDL cholesterol
  - Saturated fat <7% of calories
  - Whole eggs <=1/day (extra whites OK)
  - Chicken thighs SKINLESS, minimal butter
  - LDL helpers: oats, legumes, nuts, fish (omega-3), olive oil, soluble fiber
- **Satiety**: low glycemic index, high fiber, high protein, volume eating (vegetables)
- **Taste**: food must be tasty and juicy, NOT bland "diet food"
- **Protein preferences**: chicken thighs (skinless), chicken mince. Does NOT like chicken breast.
- **Per-meal protein floor**: every main meal >=35 g protein

### Ксюша (Ksyusha) — 28F, 65 kg

- **Diet**: pescetarian (fish, seafood, eggs, dairy — ZERO meat of any kind)
- **Daily target**: ~1700-1800 kcal, ~65-80 g protein
- **No health restrictions**
- **Per-meal protein floor**: every main meal >=20 g protein

### Shared Rules

- No children, no allergies
- Both eat at home (breakfast + lunch + dinner + snacks)
- Cook SEPARATELY (each for themselves) most of the time
- >=2 shared meals per week (fish dinners, egg dishes, legume dishes work for both)
- Weekday cooking: <=30 min active time
- Cook-once-eat-twice: dinner leftovers become next day lunch. If a dish doubles as lunch, make enough for 2 meals per person.
- Kitchen: oven (no grill!), immersion blender. No food processor — buy minced meat pre-made.
- Always say "в духовке" never "на гриле"
- Metric units
- Shopping: barbora.lt, one weekend trip

---

## Mandatory Sections

### PP Desserts (MUST HAVE — they love sweets)

Include 2-3 PP dessert recipes per week. Ideas:

- Белковые меренги (egg white meringues)
- Творожные маффины/булочки
- Чиа-пудинг
- Протеиновый мусс
- Запечённые бананы с корицей и орехами
- Овсяное печенье без сахара

### PP Movie Snacks (MUST HAVE)

Include 2-3 PP snack recipes for movie/couch nights. Ideas:

- Запечённый нут (roasted chickpeas)
- Сырные чипсы (cheese crisps from oven)
- Эдамаме
- Протеиновые шарики (protein balls)
- Овощные чипсы (из кабачков, свёклы)
- Попкорн с специями

---

## Variety Rule

If previous `Menu_*.html` files exist in the working directory, read the most recent 1-3 and ensure >=70% dinners and >=50% breakfasts are different. Rotate proteins, cuisines, side dishes.

## Shopping Rhythm

One weekend trip to barbora.lt. Prefer ingredients that keep 5-7 days or freeze well. No midweek restocking needed.

---

## Nutrition Constraints

### Plate Model

1/2 vegetables + fruit, 1/4 whole grains, 1/4 protein

### Daily Targets (per person)

- Vegetables + fruit: >=400 g/day
- Fiber: >=25 g (Ksyusha) / >=38 g (Alex)
- Free sugars: <10% of energy
- Salt: <5 g/day

### Protein Sourcing

- **Alex**: chicken thighs (skinless), chicken mince, fish, eggs (<=1 whole/day), legumes, low-fat dairy, cottage cheese
- **Ksyusha**: fish, seafood, eggs, cheese, cottage cheese, legumes, tofu, tempeh, Greek yogurt
- Fish >=2 servings/week for both
- Alex: red meat <=2 servings/week, no processed meat

---

## Language Rule

Think/reason in English. Final HTML content must be in Russian.

---

## Output File Name

Create ONE HTML file. Name: `Menu_MmmWW.html`

- `Mmm` = English month abbreviation (Mar, Apr, etc.)
- `WW` = week number within month (01-05), weeks start Monday

If filename exists, append `_v2`, `_v3`, etc.

---

## HTML Structure

### Design

- Font: Inter (Google Fonts CDN)
- Color palette: warm neutrals
- Ксюша's recipes: Tiffany blue (`#81D8D0`)
- Саша's recipes: warm terracotta/burnt orange (`#D4764E`)
- Shared recipes: sage green (`#A8C5A0`)
- Dark mode: auto-detect `prefers-color-scheme` + toggle button
- Mobile-first, rounded cards (16px), subtle shadows
- Smooth transitions on details open/close
- Large tap targets (48px min)

### Navigation (sticky header)

```
Саша | Ксюша | Рецепты | Десерты | Снэки | Покупки
```

Must fit one line on iPhone SE (375px).

### Section 1: Menu Саша (`#menu-sasha`)

Table: Пн-Вс x Завтрак / Обед / Ужин / Перекус.
Every dish name is a clickable link to its recipe card.
Shared meals marked with a green circle emoji.
Show approximate kcal per meal.

### Section 2: Menu Ксюша (`#menu-ksyusha`)

Same format. Pescetarian meals only. ZERO meat.
Shared meals marked with a green circle emoji (same recipe card as Саша's).

### Section 3: Recipes (`#recipes`)

Collapsible `<details>` cards with anchor IDs (`id="r-slug"`).
Each card: Время / Порции / Ингредиенты / Шаги (1-6) / Хранение / Замены.
Color-tagged: terracotta for Саша / Tiffany for Ксюша / sage green for shared.

### Section 4: PP Desserts (`#desserts`)

2-3 PP dessert recipe cards. Same collapsible format.

### Section 5: Movie Snacks (`#snacks`)

2-3 PP snack recipe cards. Same collapsible format.

### Section 6: Weekend Prep (`#prep`)

6-10 bullets: what to batch-prep on weekends.

### Section 7: Shopping List (`#shopping`)

- Consolidated for both people
- Grouped by category
- Each row: checkbox + item + quantity + optional note
- Each item name links to barbora.lt search: `https://barbora.lt/paieska?q=<product>`
- Entire row clickable toggles checkbox
- Progress indicator: "Куплено: X/Y"
- Buttons: "Сбросить" and "Отметить всё"
- localStorage persistence (prefix keys with file basename)

### JS Requirements

- Shopping list: localStorage persistence, copy text, progress counter
- Recipe deep-linking: clicking dish link opens `<details>` and scrolls to it
- Dark mode toggle with localStorage persistence
- Handle `hashchange` and initial page load with hash

---

## Validation Checklist

Before finishing, verify:

1. Ksyusha's meals contain ZERO meat (no chicken, beef, pork, turkey, etc.)
2. All menu links point to existing recipe IDs
3. Shopping list covers all recipe ingredients
4. Weekday cooking <=30 min active
5. Alex's daily protein ~140-160 g
6. >=2 shared meals exist and are marked with green circle emoji in both menus
7. PP desserts section has 2-3 recipes
8. PP snacks section has 2-3 recipes

---

## Output to Chat

Do not print HTML. Print only the created filename.
