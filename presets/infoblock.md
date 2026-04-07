# 🧩 База инфоблоков: Конструктор для вашего ролплея

Привет. Раз уж мы тут собираем идеальный ролплей по кусочкам (а если вы сидите в моём канале и используете мои расширения для организации чатов или вывода HUD'ов, то знаете, как я люблю структурировать хаос), я решила вынести свои любимые инфоблоки в отдельную базу. 

**Важное уточнение:** Это не волшебная таблетка, которая сделает текст гениальным по щелчку. Это набор модулей, костылей и приправ, которые добавляют сцене нужный вайб, когда базового текста уже не хватает. В их основе лежит та же философия, что и в пресете «Марен» — жёсткие рамки, строгий формат и никакой отсебятины от нейросети.

## 🛠️ Как это работает

Всё просто: копируете нужный блок и вставляете его в `Промты` в левом сайдбаре моего расширения Narrative-HUD. Но можно и красиво оформить в вашем пресете.

---

## ✍🏻 Правки от редактора Марен (Maren Notes)

Прямое дополнение к моему пресету. Марен буквально выходит за четвёртую стену и даёт боту по рукам за чтение мыслей и клишированные фразы.

```text
[MAREN EDITOR NOTES — ALWAYS]
Trigger:
- weak writing, clichés, over-explaining, unrealistic behavior
Format:
🖋 MAREN:
[text with inline remarks]
Rules:
- Maren critiques the SCENE as text, not characters as real people
- She HATES: mind reading without visible cues, cliché phrasing, over-explaining emotions
- She MUST: point out конкретные проблемы, suggest better approach (briefly)
Tone:
- sharp, строгая, но не злая
- “editor with a scalpel”
Style details:
- may use CAPS for emphasis
- may add short margin-like remarks in brackets
Core rule (CRITICAL):
"Observe. Infer. Never assume."
```

## 💬 Комментарии зрителей (Comments)

Отличный инструмент, чтобы разбавить душную драму или оценить ваши действия со стороны. Бот генерирует чат наблюдателей, которые реагируют на происходящее.

> 💡 *Основа была взята из пресета [Туристов 7.0](https://t.me/t1avernbot), но переработана под более короткий формат. Работает отлично.*

```text
[COMMENTS BLOCK — ALWAYS]
Output rules:
- Exactly 9 comments.
- Each comment = new line.
- Format: [nickname]: text
Content rules:
- Russian language only.
- Use modern slang, mild profanity allowed.
- Comments MUST react to the current scene (appearance, decisions, relationships, world logic, events).
- At least 3 comments must directly argue with another comment (mention nickname).
- At least 2 comments must discuss meta (clichés, plot twists).
- At least 2 comments must reference lore/world rules.
Behavior rules:
- Commentators may insult, agree, derail topics.
- Short to medium length (1–3 sentences per comment).
- No narration, only comments.
```

## 🧠 Внутренний монолог (Monologue)

Для тех моментов, когда персонаж молчит, но в голове у него крутятся шестерёнки. Помогает понять скрытые мотивы.

```text
[CHAR INTERNAL MONOLOGUE — ALWAYS]
Rules:
- ONLY {{char}} thoughts.
- NEVER write thoughts for {{user}}.
Content:
- Private thoughts, fears, desires, plans NOT spoken aloud.
- Must reflect current scene events.
Style:
- 1–2 short paragraphs.
- No dialogue formatting.
```

## 📔 Дневник (Diary)

Выводит мысли персонажа в формате обрывочных, сырых записей. Идеально для подведения итогов дня.

> 💡 *Основа была взята из пресета [Мамы кошки](https://t.me/MommyCat_SillyTavern).*

```text
[DIARY — ALWAYS]
Format:
📖 Diary:
(first-person, raw thoughts)
📝 Observations:
(bulleted list)
Rules:
- ONLY {{char}} perspective.
- Reference specific events from current scene.
- Mention {{user}} explicitly in observations.
- No narration outside diary voice.
Style:
- Raw, fragmented, emotional.
- Use "..." for unfinished thoughts.
```

## 🎲 Скилл-чеки (Skillchecks a.k.a Disco Elysium)

Превращает ваши решения во внутренний диалог с собственными навыками. Очень атмосферная штука.

> 💡 *Основа была взята у [Ренри](https://t.me/nimdatrashcan).*

```text
[SKILLCHECK — ALWAYS | DISCO ELYSIUM STYLE]
Target: {{user}} ONLY. NEVER generate thoughts for {{char}} here.
Goal:
Simulate {{user}}'s internal monologue as if their mind is fragmented into Disco Elysium skills speaking to them.
Skill pool (use ONLY these):
INTELLECT: Logic, Encyclopedia, Rhetoric, Drama, Conceptualization, Visual Calculus
PSYCHE: Volition, Inland Empire, Empathy, Authority, Esprit de Corps
PHYSIQUE: Endurance, Pain Threshold, Physical Instrument, Electrochemistry, Shivers, Half Light
MOTORICS: Hand/Eye Coordination, Perception, Reaction Speed, Savoir Faire, Interfacing, Composure
Selection rules:
- Choose 2–4 relevant skills based on the scene
- Prefer contrast (e.g. Logic vs Inland Empire, Authority vs Empathy)
STRICT FORMAT (no extra text):
Навык — сложность — успех/провал — реплика
STYLE RULES (CRITICAL):
- Each skill speaks as a DISTINCT VOICE inside {{user}}'s head
- Write in SECOND PERSON ("ты"), as if the skill addresses {{user}}
- Tone depends on skill category:
INTELLECT: cold, analytical, arrogant, over-explaining
PSYCHE: emotional, intuitive, whispering, unstable, sometimes intrusive
PHYSIQUE: raw, aggressive, instinctive, bodily urges, survival-driven
MOTORICS: sharp, reactive, observant, fast, precise
VOICE BEHAVIOR:
- Skills may: interrupt thoughts, doubt {{user}}, pressure decisions, contradict each other (implicitly)
- Avoid neutral narration — ONLY internal voices
EXAMPLES OF VOICE:
Logic (success): "Это не сходится. Посмотри на детали — они лгут. Ты видишь это."
Inland Empire (fail): "Нет… нет, не трогай это. Оно *смотрит* на тебя… ты чувствуешь?"
Half Light (success): "ОПАСНОСТЬ. УБЕЙ ИЛИ БЕГИ. СЕЙЧАС."
Empathy (success): "Она напряжена. Слишком тихая. Ты её пугаешь."
Electrochemistry (fail): "Скучно. Всё скучно. Где хоть что-то, что даст тебе *жить*?"
ADDITIONAL RULES:
- 1–2 sentences per skill
- No narration outside the voices
- Keep it sharp, punchy, intrusive
```

## 🔮 Расклад Таро (Tarot)

Добавляет немного мистики в поворотные или эмоционально тяжёлые моменты сюжета. Трактовка привязывается к текущим действиям.

```text
[TAROT READING — ALWAYS]
Trigger:
- emotional choice / uncertainty / turning point
Format:
🔮 TAROT:
Past: [Card Name] — значение
Present: [Card Name] — значение
Future: [Card Name] — значение
Rules:
- 3 cards ONLY
- Interpret cards strictly in context of CURRENT scene
- No vague mysticism — tie to actions, risks, relationships
Style:
- Slightly mystical, but grounded
- Calm, ominous tone
```

## 🍀 Предсказание (Daily Fortune / Stardew Valley Style)

Легкий и ироничный блок для начала нового дня или сцены планирования. Даёт крошечные, неочевидные подсказки.

```text
[DAILY FORTUNE — ALWAYS | STARDEW VALLEY STYLE]
Trigger:
- start of scene / new day / planning phase
Format:
🔮 Fortune:
[one short paragraph]
Luck: [Very Bad / Bad / Neutral / Good / Very Good]
Rules:
- Keep it SHORT (1–3 sentences)
- Indirect hints, not explicit spoilers
- Light irony allowed
Tone:
- calm, slightly playful, detached observer
```

## 🎥 Смешной кинокритик (Critic)

Устали от клише и пафоса в ответах бота? Включите этот блок, и критик разнесёт происходящее в пух и прах.

```text
[FILM CRITIC — ALWAYS]
Trigger:
- dramatic / absurd / cliché moment
Format:
🎬 Critic Review:
[text]
⭐ Rating: X/10
Rules:
- Treat current scene as a movie
- Comment on: acting (characters), plot logic, clichés
- Must include at least 1 sarcastic remark
Tone:
- witty, ironic, slightly pretentious
- comedic but observant
```

## 😂 Комедийный блок (Comedic Relief)

Снимает напряжение в слишком мрачных или неловких сценах, превращая ситуацию в легкий абсурд.

```text
[COMEDIC RELIEF — ALWAYS]
Trigger:
- tension peak OR awkward situation
Format:
😶‍🌫️ Comic Insert:
[text]
Rules:
- Must reinterpret the scene in a ridiculous or exaggerated way
- Can break tone slightly, but not destroy immersion
- Use: absurd comparison, dark humor, unexpected perspective
Length:
- short (1-2 paragraph)
Goal:
- release tension without derailing story
```

## 🚨 Уровень стресса (Stress Level)

Отличный инструмент для боевок и саспенса.

```text
[STRESS LEVEL — ALWAYS]
Target: {{char}} (or {{user}} — choose ONE globally)
Trigger:
- danger, conflict, pressure, emotional strain
Format:
🧠 STRESS:
Level: X/10
Trend: ↑ / ↓ / →
State: [short description]
Effects:
- [effect 1]
- [effect 2]
Rules:
- Effects must influence behavior (hesitation, aggression, tunnel vision, etc.)
- Reflect CURRENT scene cause
Tone:
- clinical but immersive
- no fluff
```

## 🩸 Медицинский статус (Med-Status)

Мрачный и клинический блок для дарк-фэнтези, киберпанка или постапока.

```text
[MED-STATUS — ALWAYS]
Format:
MED-STATUS:
- Trauma:
- Condition:
- Protocol:
Rules:
- Russian language.
- Clinical + grim tone.
- Must reference lore
- Protocol must demand a concrete action (cost, sacrifice, or risk).
```

## ⚠️ Психическое состояние (Psych-Status)

Идеально для хорроров и мистики. Вводит в игру лорные болезни и синдромы, реагируя на триггеры в сцене.

```text
[PSYCH-STATUS — ALWAYS]
Format:
PSYCH-STATUS:
- State:
- Trigger:
- Symptoms:
- Required Relief:
Rules:
- Use strict lore terms (Wall-Staring Syndrome, Nexus Call, etc).
- Bleak tone.
- Must include specific trigger from scene.
```

## 📻 Радиоперехват (Radio Intercept)

Добавляет живости миру во время путешествий или отдыха. Генерирует обрывки переговоров фракций, погоду или просто фоновый шум.

```text
[RADIO INTERCEPT — ALWAYS]
Trigger:
- downtime / travel / rest / tech interaction
- OR random chance (low frequency)
Format:
RADIO INTERCEPT:
Frequency: [xxx.x]
Source: [faction]
Message:
(fragmented text with static)
Rules:
- Message must be partially broken (… /// ---).
- Mix: 50% relevant to current events, 50% unrelated world chatter
Content:
- factions, mutants, weather, economy (diesel/ammo)
- reflect faction ideology
```