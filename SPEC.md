# Meal Plan Generation Specification

> **Purpose**: Complete specification for generating weekly meal plans for Саша and Ксюша.
> Read this file at the start of every meal-plan generation session.

---

## Role

Expert nutritionist and practical meal-planning consultant (evidence-based, realistic for busy couples).

## Goal

Create a healthy, balanced 7-day menu and a single mobile-friendly HTML file containing menus, recipes, PP desserts, PP snacks, and a shopping checklist with barbora.lt links for a couple.

---

## Family

### Саша (Alex) — 28M, 110 kg

- **Goal**: gradual weight loss
- **Diet**: omnivore, ПП (правильное питание / clean eating)
- **Daily target**: **2100 kcal ±100** · **150 g protein ±10**
- **Health**: elevated LDL cholesterol
  - Saturated fat <7% of calories
  - Whole eggs ≤1/day (extra whites OK)
  - Chicken thighs SKINLESS, minimal butter
  - LDL helpers: oats, legumes, nuts, fish (omega-3), olive oil, soluble fiber
- **Satiety**: low glycemic index, high fiber, high protein, volume eating (vegetables)
- **Taste**: food must be tasty and juicy, NOT bland "diet food"
- **Protein preferences**: chicken thighs (skinless), chicken mince. Does NOT like chicken breast.

#### Саша per-meal minimums (HARD CONSTRAINT)

| Meal | kcal min | Protein min |
|------|----------|-------------|
| Завтрак | 400 | 30 g |
| Обед | 550 | 40 g |
| Ужин | 550 | 40 g |
| Перекус | 200 | 15 g |

#### Саша portion anchors

- Meat (chicken thighs, mince): **250 g raw** per serving
- Fish: **200 g raw** per serving
- Grains (bulgur, buckwheat, quinoa): **80–100 g dry** per serving
- Vegetables: **200–300 g** per meal
- Cottage cheese: **200–250 g** per serving

### Ксюша (Ksyusha) — 28F, 65 kg

- **Diet**: pescetarian (fish, seafood, eggs, dairy — ZERO meat of any kind)
- **Daily target**: **1750 kcal ±100** · **75 g protein ±10**
- **No health restrictions**

#### Ксюша per-meal minimums (HARD CONSTRAINT)

| Meal | kcal min | Protein min |
|------|----------|-------------|
| Завтрак | 350 | 15 g |
| Обед | 450 | 20 g |
| Ужин | 450 | 20 g |
| Перекус | 200 | 8 g |

#### Ксюша portion anchors

- Fish: **150–180 g raw** per serving
- Grains: **60–80 g dry** per serving
- Vegetables: **200–250 g** per meal
- Cheese/cottage cheese: **100–150 g** per serving

### Shared Rules

- No children, no allergies
- Both eat at home (breakfast + lunch + dinner + snacks)
- Cook SEPARATELY (each for themselves) most of the time
- ≥2 shared meals per week (fish dinners, egg dishes, legume dishes work for both)
- Weekday cooking: ≤30 min active time
- Kitchen: oven (no grill!), immersion blender. No food processor — buy minced meat pre-made.
- Always say "в духовке" never "на гриле"
- Metric units
- Shopping: barbora.lt, one weekend trip

---

## Meal Planning Rules

### Cook-once-eat-twice (CRITICAL for reducing shopping list)

- **≥3 dinners per person per week** must produce enough for next-day lunch (double batch)
- This means only ~4 unique dinners per person + leftovers for 3 lunches = ~4 lunch recipes needed (not 7)
- If a dinner doubles as next-day lunch, recipe must state: "Порции: 2 (ужин) + 2 (обед на завтра)"

### Breakfast rotation (reduce recipe count)

- Max **3–4 unique breakfast recipes per person** per week. Repeat favorites.
- Shared breakfasts count toward the ≥2 shared meals target.

### Ingredient reuse rule

- **≥70% of ingredients must appear in ≥2 recipes** that week
- Plan both menus around shared base vegetables, grains, and dairy
- Example: if Саша uses broccoli for dinner, Ксюша's recipe that week should also use broccoli

### Recipe count cap

- **Max 25–30 recipe cards total** (Саша + Ксюша + shared + desserts + snacks)
- Fewer unique recipes = fewer ingredients = smaller shopping list

---

## Mandatory Sections

### PP Desserts (MUST HAVE — they love sweets)

Include 2–3 PP dessert recipes per week. Ideas:

- Белковые меренги (egg white meringues)
- Творожные маффины/булочки
- Чиа-пудинг
- Протеиновый мусс
- Запечённые бананы с корицей и орехами
- Овсяное печенье без сахара

**КБЖУ requirement**: Every dessert/snack recipe MUST show macros per 100g:
```
На 100 г: 120 ккал · Б 15 г · Ж 2 г · У 10 г
```
Display as a prominent badge/row at the top of the recipe card.

### PP Movie Snacks (MUST HAVE)

Include 2–3 PP snack recipes for movie/couch nights. Ideas:

- Запечённый нут (roasted chickpeas)
- Сырные чипсы (cheese crisps from oven)
- Эдамаме
- Протеиновые шарики (protein balls)
- Овощные чипсы (из кабачков, свёклы)
- Попкорн с специями

Same КБЖУ per 100g requirement as desserts.

---

## Variety Rule

If previous `Menu_*.html` files exist in the working directory, read the most recent 1–3 and ensure ≥70% dinners and ≥50% breakfasts are different. Rotate proteins, cuisines, side dishes.

## Shopping Rhythm

One weekend trip to barbora.lt. Prefer ingredients that keep 5–7 days or freeze well. No midweek restocking needed.

---

## Nutrition Constraints

### Plate Model

½ vegetables + fruit · ¼ whole grains · ¼ protein

### Daily Targets (per person)

- Vegetables + fruit: ≥400 g/day
- Fiber: ≥25 g (Ксюша) / ≥38 g (Саша)
- Free sugars: <10% of energy
- Salt: <5 g/day

### Protein Sourcing

- **Саша**: chicken thighs (skinless), chicken mince, fish, eggs (≤1 whole/day), legumes, low-fat dairy, cottage cheese
- **Ксюша**: fish, seafood, eggs, cheese, cottage cheese, legumes, tofu, tempeh, Greek yogurt
- Fish ≥2 servings/week for both
- Саша: red meat ≤2 servings/week, no processed meat

### Daily calorie enforcement (HARD CONSTRAINT)

After planning all 7 days, SUM each day's meals. Every day MUST be within ±100 of target:
- Саша: 2000–2200 kcal
- Ксюша: 1650–1850 kcal

If a day is under target, increase portion sizes or add a note: "+50г крупы к обеду" / "+100г овощей"

---

## Language Rule

Think/reason in English. Final HTML content must be in Russian.

---

## Output File Name

Create ONE HTML file. Name: `Menu_MmmWW.html`

- `Mmm` = English month abbreviation (Mar, Apr, etc.)
- `WW` = week number within month (01–05), weeks start Monday

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

Day cards: Пн–Вс. Each day shows Завтрак / Обед / Ужин / Перекус.
- Every dish name is a clickable link to its recipe card
- Shared meals marked with 🟢
- Show per-meal: `~ккал, Бг`
- **Daily summary line**: `2080 ккал · Б 148 г · Ж 65 г · У 230 г` — full КБЖУ

### Section 2: Menu Ксюша (`#menu-ksyusha`)

Same format. Pescetarian meals only. ZERO meat.
Shared meals marked with 🟢 (same recipe card as Саша's).
Same daily КБЖУ summary.

### Section 3: Recipes (`#recipes`)

Collapsible `<details>` cards with anchor IDs (`id="r-slug"`).
Each card: Время / Порции / Ингредиенты / Шаги (1–6) / Хранение / Замены.
Color-tagged: terracotta for Саша / Tiffany for Ксюша / sage green for shared.

### Section 4: PP Desserts (`#desserts`)

2–3 PP dessert recipe cards. Same collapsible format.
**Each card must show КБЖУ per 100g** as a prominent badge at the top.

### Section 5: Movie Snacks (`#snacks`)

2–3 PP snack recipe cards. Same collapsible format.
**Each card must show КБЖУ per 100g** as a prominent badge at the top.

### Section 6: Weekend Prep (`#prep`)

**Concrete** batch-prep instructions tied to actual recipes:
- Specific quantities: "Сварить 600 г булгура", "Запечь 1 кг куриных бёдрышек (без кожи)"
- Tied to specific days: "Это пойдёт на обед Пн + ужин Вт"
- 6–10 action items

### Section 7: Shopping List (`#shopping`)

**Two sub-sections:**

#### 7a. Базовые продукты (всегда дома)
Non-interactive reference list of pantry staples assumed to be in stock:
- Salt, pepper, olive oil, common spices (paprika, cumin, turmeric, garlic powder, oregano)
- Soy sauce, honey, mustard, vinegar
- These are NOT in the checkbox list and NOT counted toward the 60-item cap

#### 7b. Купить на этой неделе
Interactive consolidated checklist:
- **Max 60 items** (HARD CAP — if list exceeds this, simplify recipes)
- Grouped by category (produce, dairy, protein, grains, other)
- Each row: checkbox + item name (linked to barbora.lt search) + quantity
- Link format: `https://barbora.lt/paieska?q=<product_name_in_Lithuanian>`
- Entire row clickable toggles checkbox
- Progress indicator: "Куплено: X/Y"
- Buttons: "Сбросить", "Отметить всё", "Скопировать список"
- localStorage persistence (prefix keys with file basename)

### JS Requirements

- Shopping list: localStorage persistence, copy text, progress counter
- Recipe deep-linking: clicking dish link opens `<details>` and scrolls to it (calculate offset dynamically using header's offsetHeight, NOT hardcoded pixels)
- Dark mode toggle with localStorage persistence
- Handle `hashchange` and initial page load with hash

---

## Validation Checklist

Before finishing, verify:

1. **Ксюша zero meat**: no chicken, beef, pork, turkey, lamb in any of her meals
2. **Calorie check**: every day within ±100 of target (Саша 2100, Ксюша 1750)
3. **Protein check**: Саша ≥140 g/day, Ксюша ≥65 g/day
4. **Recipe links**: all menu links → existing recipe IDs; every recipe is referenced
5. **Shopping list ≤60 items** (excluding pantry staples)
6. **Shopping list completeness**: covers all recipe ingredients, no missing items
7. **Recipe count ≤30** total cards
8. **Weekday cooking ≤30 min** active per dish
9. **≥2 shared meals** marked 🟢 in both menus
10. **PP desserts**: 2–3 recipes with КБЖУ per 100g
11. **PP snacks**: 2–3 recipes with КБЖУ per 100g
12. **Barbora.lt links**: every shopping item links to barbora.lt search
13. **Ingredient reuse**: ≥70% of ingredients in ≥2 recipes

---

## Output to Chat

Do not print HTML. Print only the created filename.
