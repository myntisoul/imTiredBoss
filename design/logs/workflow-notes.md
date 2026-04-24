# настройки
- **model**: flux.1 dev fp8
- **seed**: 400409799148377
- **steps**: 20
- **cfg**: 4.0
- **sampler**: euler
- **latent size**: 512x512
по большей части я не менял seed, sampler, latent size, cfg. между вариантами менял сам промт и иногда steps. с его увеличением картинка становится менее расплывчатой (при 16 по совету от chatgpt совсем мыло). также иногда использовал lora ps1_style_flux_v1 со значениями 0.4-0.6, но результат нравился больше без неё. 

# результаты
### кабинет оракула
`01-w04-location-oracle's-office
отлично передаёт загадочную атмосферу локации, неплохо передаёт визуальный стиль.
удачно: композиция, атмосфера. визуальный стиль, освещение, образ оракула. 
требует доработки: сделать более угловатым, более "лоу-поли".

### протагонист в квартире
`01-w04-character-protagonist
подходящая депрессивная атмосфера и настроение игры. 
удачно: атмосфера, настроение. протагонист - сломленный человек.
требует доработки: сделать более угловатый визуал, главный герой слишком худой, правая рука забагованная.

### сцена с офицером и протагонистом
`01-w04-mood-officer-and-protagonist-scene
нормально передаёт визуал игры и композицию сцены.
удачно: атмосфера, напряжённое настроение. 
требует доработки: неуместное яркое освещение позади протагониста и девочки (будто они из рая вышли), странные позы полицейских, сделать более угловатый визуал.

### спящий мессия
`01-w04-character-messiah
отличная передача атмосферы и персонажа.
удачно: атмосфера, персонаж. мессия не выглядит как святой мученик, а просто как обычный ребёнок, но при этом чувствуется тревожность, что что-то не так.
требует доработки: сделать более угловатые модельки.

## шаг 1. кабинет оракула
**Контекст:**
- нужен концепт-арт важной локации взаимодействия протагониста с ключевым персонажем.
- визуальная часть проекта

**Что пробовали:**
- Вариант 1
	ps1 game screenshot, low poly, dirty office from 1970s soviet era, dark wood desk with green glass lamp, dusty bookshelves, gramophone with brass horn, middle-aged man in gray jacket sitting at desk writing with fountain pen, tired face with glasses, warm dim light from lamp, deep shadows, muddy textures, visible low polygon count, flat lighting, grainy, claustrophobic atmosphere, view from doorway, ps1 style, 1990s 3d game graphics
	использовал lora ps1_style_flux_v1 с параметром 1.00.
- Вариант 2
	low-poly dirty surreal indie game concept art, grim narrative atmosphere, PS1-era aesthetic, harsh geometry, noisy textures, slight dithering, analog horror tone
	a small office room existing inside a dream void, viewed from a doorway leading into absolute pitch-black darkness, the camera slightly off-angle, observational perspective, as if intruding
	the room is lit only by a single green glass desk lamp casting dim warm yellow light, corners consumed by dense shadows that subtly shift and feel alive, dusty heavy air, frozen time atmosphere, untouched for decades yet clearly inhabited and maintained
	a large worn dark wooden desk with ink stains, neatly arranged stacks of yellowed papers, fountain pen and inkwell, a man sits behind it in half-profile, writing slowly and carefully without looking up
	the man (the Oracle’s human shell): plain, nondescript male, 50-55 years old, slightly balding, tired eyes behind thin metal-frame glasses, worn gray jacket, white shirt without tie, calm, neutral expression, bureaucratic presence, NOT sinister
	floor-to-ceiling bookshelves filled with old leather-bound books with faded spines, interspersed with small objects: a turned-away photo frame, a dried flower, stopped mechanical clocks
	a gramophone with a large brass horn stands against the wall, nearby dusty vinyl records, silent but heavy with implied sound
	old parquet wooden floor, worn and creaky, near the walls dark damp-like stains that feel wrong, as if something avoids being perceived directly
	subtle details: a city map on the wall marked with strange unreadable symbols, a grandfather clock behaving incorrectly (either ticking without movement or moving without sound), optional window showing only black void, faint silhouette barely visible when not looked at directly
	composition emphasizes contrast between mundane human interior and incomprehensible surrounding void
	style references: low-poly, retro rendering, crunchy lighting, vertex shading, texture warping, analog noise, slight motion blur feel, PS1/PS2 era survival horror aesthetics
	mood keywords: uncanny, oppressive calm, quiet dread, controlled space, unnatural stillness, reality slightly broken
	без lora.
**Вывод:**
- принимаем второй вариант, т.к. первый выглядит слишком устаревшим. мне нужен стиль, похожий на ps1, но он должен выглядеть современно. 
- дальше будем либо генерировать без lora ps1, либо с низкими значениями (0.2-0.6).  более подробные промты дают лучший результат.
## шаг 2. спящий мессия
**Контекст:**
- нужен концепт-арт важного для истории персонажа.
- визуальная часть проекта

**Что пробовали:**
- Вариант 1
	low-poly dirty indie game concept art, PS1 aesthetic, soft noise, minimal lighting
	small quiet room, simple and modest, grounded environment
	a child (around 9 years old) lies in bed, asleep, motionless
	camera is close but not intimate, slightly distant, observational
	the room is dimly lit by a weak, warm light source (lamp or small light)
	the child looks peaceful but unnaturally still, as if sleeping too deeply
	subtle unsettling details: no visible breathing movement, hands too still, blanket undisturbed
	around the room: minimal personal items (small toys, simple objects), nothing excessive
	important: everything is grounded, no glow, no divine effects
	optional subtle hint: shadows slightly too deep, silence feels unnatural
	tone: fragile, quiet, deeply unsettling, unnatural stillness, restrained sadness
	без lora.
- Вариант 2
	low-poly dirty indie game concept art, PS1 aesthetic, soft noise, minimal lighting
	small quiet room, simple and modest, grounded environment, old appartment of soviet era 90s
	a child (around 9 years old) lies in bed, asleep, motionless
	camera is close but not intimate, slightly distant, observational
	the room is dimly lit by a weak, warm light source (lamp or small light)
	the child looks peaceful but unnaturally still, as if sleeping too deeply
	subtle unsettling details: no visible breathing movement, hands too still, blanket undisturbed
	around the room: minimal personal items (small toys, simple objects), nothing excessive
	important: everything is grounded, no glow, no divine effects
	optional subtle hint: shadows slightly too deep, silence feels unnatural
	tone: fragile, quiet, deeply unsettling, unnatural stillness, restrained sadness
	использовал lora ps1 со значением 0.30.
**Вывод:**
- принимаем второй вариант, т.к. первый выглядит слишком гладким. 
- дальше будем либо генерировать без lora ps1, либо с низкими значениями (0.2-0.6).

## Шаг 2. Style A/B test

**Контекст:**
- Что сравнивали: бойня протагониста с "демонами"
	- Для какой части проекта: очень примерная визуализация геймплея

**Фиксировали:**
- Модель: flux.1 dev fp8
- Workflow template
- Anchor asset
- Общий prompt skeleton

**Что меняли:**
- Direction A: протагонист с битой 
- Direction B: протагонист с огнестрелом
- добавил lora "low-poly joy" со значением 1.00
- lora "ps1-style" значение 0.60-0.80 

**Вывод:**
- Что принимаем как baseline: вариант B
- Почему: у нейронки плохо получается нарисовать биту в руках протагониста - слишком маленькая и выглядит, как игрушечная.
- Что делаем дальше: продолжаем использовать lora "low-poly joy", комбинируя с ps1-style.

# таблица тестов
- модель: flux.1 dev fp8
- workflow: `w06_multiprompt`
- seed: 694101601609615
- promt-блоки: 
	 - `constants`
	  - `style/world`
	  - `modifier`


|Вариант|Seed (фикс)|Weight / Strength|Что меняли|Что изменилось|Keep / Drop|
|---|---|---|---|---|---|
|1|694101601609615|constants=1.0, style=0.9, modifier=0.3|modifier: снижен вес до 0.3|Трип-эффекты (кислотные цвета, аберрация) стали слабее, почти незаметны. Больше похоже на обычную перестрелку.|Drop (теряется ключевая механика трипа)|
|2|тот же|constants=1.0, style=0.9, modifier=0.7|modifier: повышен вес до 0.7|Трип слишком сильный: цвета вырвиглазные, геометрия сильно искажена, враги едва узнаваемы. Перегружено.|Drop (нарушает читаемость)|
|3|тот же|constants=1.0, style=0.7, modifier=0.5|style/world снижен до 0.7|Текстуры стали более гладкими, пропал пиксельный шум. Стиль мира «уехал» в сторону фотореализма.|Drop (нарушает style bible)|
|4|тот же|constants=1.0, style=0.9, modifier=0.5|modifier: `emotion: protagonist feels pain, not euphoria` (замена в modifier)|Протагонист выглядит испуганным, гримаса боли. Потеряно ощущение «ложной праведности».|Drop (меняет характер персонажа)|
|5|тот же|constants=1.0, style=0.9, modifier=0.5|modifier: `camera angle: third-person, over-the-shoulder`|Камера отошла назад, видно тело протагониста со спины. Потеря иммерсии, ощущение от первого лица исчезло.|Drop (нарушает камеру из констант)|
|6|тот же|constants=1.0, style=0.9, modifier=0.5|modifier: без изменений, но добавлен `lighting: realistic, no psychedelic`|Трип убран, свет стал плоским серым. Сцена выглядит как обычное насилие без оправдания.|Keep (как вариант для «трезвого» режима, если нужно показать реальность без химии)|

## Шаг 3. Inpaint test

### Контекст
- **кадр**
	`01-w06-scene-oracle-and-victor`
- **Что в нём уже работало**
	атмосфера тайны, сверхъестественного через рутинность, напряжение в диалоге.
- **Что нужно было исправить**
	виктор сидит в пиджаке, это полностью не подходит его образу.

### Что фиксировали
- **Модель**: `flux.1 dev fp8 fill`
- **Workflow**: `w07_img2img_inpaint_outpaint.json`
- **Seed**: `919828922167906`
- **Основные параметры**:
	- cfg: 1.0
	- steps: 20
	- lora: ps1-style & low-poly-joy

### Что меняли
- **Denoise**: при значении меньше 1.00 ничего не меняется.

**Вывод:**
- **Что принимаем**: новый вариант
- **Почему**: 
	серая футболка всё ещё не совсем соответствует указанному описанию виктора, но всё же лучше, чем пиджак.
- **Что делаем дальше**: продолжаем в том же духе.

## Шаг 4. img2img test

### Контекст
- **кадр**
	`01-w04-mood-officer-and-protagonist-scene`
- **Что в нём уже работало**
	напряжение сцены, атмосфера
- **Что нужно было исправить**
	неуместное свечение позади виктора и освобождённой девочки, будто они вышли из портала в рай.
### Что фиксировали
- **Модель**: `flux.1 dev fp8 fill`
- **Workflow**: `w07_img2img_inpaint_outpaint.json`
- **Seed**: `919828922167906`
- **Основные параметры**:
	- cfg: 1.0
	- steps: 20
	- lora: ps1-style & low-poly-joy
### Что меняли
- **Denoise**: 0.5 и меньше ничего не меняется; при больших значениях свечение не убирается, зато ломается сцена.
**Вывод:**
- **Что принимаем**: старый вариант
- **Почему**: 
	нейросеть ничего не изменяет, сколько бы я ни пытался. я произвёл 25 генераций, и ни одна из них ничего не меняла. я устал.
- **Что делаем дальше**: хз
