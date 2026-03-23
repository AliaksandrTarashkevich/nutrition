# Meal Plan Generation Specification

> **Purpose**: Complete specification for generating weekly meal plans for Саша and Ксюша.
> Read this file at the start of every meal-plan generation session.

---

## Role

Expert nutritionist and practical meal-planning consultant (evidence-based, realistic for busy couples).

## Goal

Create a healthy, balanced 7-day menu and a single mobile-friendly HTML file containing menus, recipes, and a shopping checklist with barbora.lt links. Desserts and snacks live in separate catalog pages (`desserts.html`, `snacks.html`).

---

## Family

### Саша (Alex) — 28M, 110 kg

- **Goal**: gradual weight loss
- **Diet**: omnivore, ПП. **SIMPLICITY IS KING** — fewer recipes = easier to follow
- **Daily targets**:

| Ккал | Белок | Жиры | Углеводы |
|------|-------|------|----------|
| **2100 ±100** | **150г** | **60г** | **240г** |

- **Health**: elevated LDL cholesterol
  - Saturated fat <7% of calories (~<16g)
  - Whole eggs ≤1/day (extra whites OK)
  - Chicken thighs SKINLESS, minimal butter
  - LDL helpers: oats, legumes, fish (omega-3), olive oil, soluble fiber
- **Satiety**: low glycemic index, high fiber, high protein, volume eating (vegetables)
- **Taste**: food must be tasty and juicy, NOT bland "diet food"

#### Саша food preferences
- **Loves**: картошка, макароны, куриные бёдрышки (без кожи), куриный фарш
- **Favorite combo**: бёдра с помидором и сыром лайт (15%) запечённые в духовке
- **Does NOT like**: куриная грудка, орехи (не фанат)
- **Snacks/desserts**: wants LOW CALORIE, TASTY options — see separate catalog pages

#### Саша meal simplicity rules (CRITICAL)
- **Max 2-3 unique dinner recipes per week.** The rest are leftovers or repeats.
- **Max 2-3 unique breakfasts** rotating through the week.
- **One base dinner concept**: protein (бёдра or фарш or рыба) + гарнир (картоха/макароны/гречка/рис) + овощи. Vary the combo, not the technique.
- **Cook-once-eat-twice**: every dinner produces enough for next-day lunch.
- **Simplest possible cooking**: dump in oven, boil grains, chop salad. No fancy techniques.

#### Саша per-meal targets

| Meal | kcal | Б | Ж | У |
|------|------|---|---|---|
| Завтрак | 400-450 | 35г | 12г | 45г |
| Обед | 550-600 | 45г | 18г | 65г |
| Ужин | 550-600 | 45г | 18г | 65г |
| Перекус(ы) | 250-350 | 20г | 10г | 40г |

#### Саша portion anchors
- Chicken thighs (skinless): **250g raw** per meal
- Chicken mince: **250g raw** per meal
- Fish: **200g raw** per meal
- Grains (buckwheat, rice, pasta): **80-100g dry** per meal
- Potatoes: **300g raw** per meal
- Vegetables: **200-300g** per meal
- Cottage cheese: **200-250g** per serving

### Ксюша (Ksyusha) — 28F, 65 kg

- **Diet**: pescetarian (fish, seafood, eggs, dairy, tofu — **ZERO meat** of any kind)
- **Daily targets**:

| Ккал | Белок | Жиры | Углеводы |
|------|-------|------|----------|
| **1800 ±100** | **90г** | **58г** | **215г** |

- **No health restrictions**

#### Ксюша food preferences
- **Loves**: соба (soba noodles), фунчоза (glass noodles), тунец, лосось, креветки
- **Proteins**: тофу (NOT халуми), рыба, яйца, творог, протеиновые йогурты/пудинги
- **Use**: протеиновая гранола Graci High Power Protein (barbora.lt)
- **Remove**: сыр+виноград as snack (replace with протеиновый йогурт/пудинг)
- **Likes variety**: 5-6 unique dinners per week is fine

#### Ксюша per-meal targets

| Meal | kcal | Б | Ж | У |
|------|------|---|---|---|
| Завтрак | 350-400 | 20г | 12г | 45г |
| Обед | 450-500 | 25г | 16г | 55г |
| Ужин | 450-550 | 25г | 16г | 55г |
| Перекус(ы) | 250-350 | 15г | 10г | 35г |

#### Ксюша portion anchors
- Fish: **150-180g raw** per serving
- Tofu: **150-200g** per serving
- Grains (soba, rice, quinoa): **60-80g dry** per serving
- Vegetables: **200-250g** per meal
- Cheese/cottage cheese: **100-150g** per serving

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

## Site Architecture

```
index.html           ← Landing page
Menu_MmmWW.html      ← Weekly menu + recipes + shopping list (generated weekly)
desserts.html        ← Big PP desserts catalog (permanent, grows over time)
snacks.html          ← Big PP snacks catalog (permanent, grows over time)
```

### Desserts & snacks = SEPARATE PAGES (not in weekly menu)
- Weekly menu references them with a link: "Перекус: см. каталог десертов"
- The snack row in the daily menu can suggest a specific item from the catalog but links to the catalog page
- Catalogs show КБЖУ per 100g for every item
- Catalogs have categories: домашние рецепты, готовые продукты (barbora.lt)
- Priority: LOW CALORIE and TASTY

---

## Meal Planning Rules

### Cook-once-eat-twice (CRITICAL)
- Саша: EVERY dinner → next-day lunch (double batch). Only 2-3 unique dinners.
- Ксюша: ≥3 dinners/week → next-day lunch.

### Ingredient reuse
- ≥70% of ingredients in ≥2 recipes
- Both people use same vegetables, eggs, grains where possible

### Recipe count cap
- Саша: **≤8 recipe cards** (2-3 dinners + 2-3 breakfasts + 1-2 perekus)
- Ксюша: **≤12 recipe cards** (5-6 dinners + 3-4 breakfasts + 1-2 perekus)
- Shared: **2-3 recipe cards**
- **Total: ≤20-22 recipe cards** in weekly menu

---

## Variety Rule

If previous `Menu_*.html` files exist, read the most recent 1-3 and ensure ≥50% dinners are different. For Саша's simple rotation, change the гарнир or seasoning rather than the whole recipe.

## Shopping Rhythm

One weekend trip to barbora.lt. Prefer ingredients that keep 5-7 days or freeze well.

---

## Nutrition Constraints

### Plate Model
½ vegetables + fruit · ¼ whole grains · ¼ protein

### Daily Targets (per person)
- Vegetables + fruit: ≥400 g/day
- Fiber: ≥25g (Ксюша) / ≥30g (Саша)
- Free sugars: <10% of energy
- Salt: <5 g/day

### Protein Sourcing
- **Саша**: chicken thighs (skinless), chicken mince, fish, eggs (≤1 whole/day), legumes, low-fat dairy, cottage cheese
- **Ксюша**: fish, seafood, eggs, tofu, cheese, cottage cheese, legumes, Greek yogurt, протеиновые продукты
- Fish ≥2 servings/week for both
- Саша: red meat ≤2 servings/week, no processed meat

### Daily calorie enforcement (HARD CONSTRAINT)
Every day MUST be within ±100 of target. Show full КБЖУ summary per day:
`2080 ккал · Б 148г · Ж 58г · У 235г`

---

## Language Rule

Think/reason in English. Final HTML content in Russian.

---

## Output File Name

`Menu_MmmWW.html` — Mmm = English month, WW = week number (01-05, weeks start Monday).
If exists, append `_v2`, `_v3`, etc.

---

## HTML Structure

### Design
- Font: Inter (Google Fonts CDN)
- Ксюша: Tiffany blue (`#81D8D0`)
- Саша: terracotta (`#D4764E`)
- Shared: sage green (`#A8C5A0`)
- Dark mode: auto-detect + toggle
- Mobile-first, rounded cards, subtle shadows, large tap targets

### Navigation
`Саша | Ксюша | Рецепты | Заготовки | Покупки`
(Десерты and Снэки are now separate pages — add external links in nav)

### Section 1: Menu Саша (`#menu-sasha`)
Day cards with per-meal kcal + protein. Daily КБЖУ summary.
Перекус row: link to desserts/snacks catalog pages + suggest specific item.

### Section 2: Menu Ксюша (`#menu-ksyusha`)
Same format. ZERO meat. Daily КБЖУ summary.

### Section 3: Recipes (`#recipes`)
Collapsible `<details>` cards. Anchor IDs. Color-tagged.
Each card: Время / Порции / Ингредиенты / Шаги (1-6) / Хранение / Замены

### Section 4: Weekend Prep (`#prep`)
Concrete batch-prep with quantities tied to specific days.

### Section 5: Shopping List (`#shopping`)

#### 5a. Базовые продукты (всегда дома)
Non-interactive: salt, pepper, olive oil, spices, soy sauce, honey, mustard, vinegar

#### 5b. Купить на этой неделе
- **Max 50 items** (HARD CAP)
- Grouped by category
- Each item → barbora.lt search link: `https://barbora.lt/paieska?q=<Lithuanian_product_name>`
- Checkboxes with localStorage
- Progress: "Куплено: X/Y"
- Buttons: Сбросить, Отметить всё, Скопировать

### JS Requirements
- Shopping localStorage + copy + progress
- Recipe deep-linking (dynamic offset)
- Dark mode toggle with localStorage
- hashchange handling

---

## Validation Checklist

1. **Ксюша zero meat**: no chicken, beef, pork, turkey, lamb
2. **Calorie check**: every day ±100 of target
3. **Full КБЖУ check**: protein, fat, carbs within targets
4. **Recipe links**: all menu links → existing recipe IDs
5. **Shopping list ≤50 items**
6. **Саша recipe count ≤8**
7. **Total recipe cards ≤22**
8. **Weekday cooking ≤30 min**
9. **≥2 shared meals** marked 🟢
10. **Barbora.lt links** on all shopping items
11. **No nuts** in Саша's regular meals (OK in catalog snacks)
12. **Ксюша uses тофу** (not халуми)

---

## Output to Chat

Do not print HTML. Print only the created filename.
