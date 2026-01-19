# 🗺️ MOC Quick Reference — Шпаргалка

## 🎯 Какой тип MOC выбрать?

```
┌─────────────────────────────────────────────────────────────┐
│ Нужна быстрая навигация по проектам/ресурсам?              │
│ → Area MOC (health, work, relationships)                    │
├─────────────────────────────────────────────────────────────┤
│ Изучаю концепцию/практику/принцип?                         │
│ → Concept MOC (творчество, страх vs любовь)                │
├─────────────────────────────────────────────────────────────┤
│ Погружаюсь глубоко в тему (research + protocols)?          │
│ → Topic MOC (fiber, VO2 Max, iron)                         │
└─────────────────────────────────────────────────────────────┘
```

---

## ⚡ Быстрое создание

### **Area MOC:**
```bash
cp area_moc_template.md ../../../01_library/mocs/[area_name].md
```
**Секции:** Vision → Projects → Resources → Metrics → Archives → Хронология

---

### **Concept MOC:**
```bash
cp concept_moc_template.md ../../../01_library/mocs/[concept]_moc.md
```
**8 секций:** Зачем → Ядро → Оси → Практики → Принципы → Источники → Пересечения → Вопросы

---

### **Topic MOC:**
```bash
cp topic_moc_template.md ../../../01_library/[category]/[topic]_moc.md
```
**Секции:** TL;DR → Структура (Research/Consensus/Protocols/Sources) → Навигация → Цели → Метрики → Концепции → TODO

---

## 📋 Чек-лист (перед сохранением)

**Обязательно:**
- [ ] YAML фронтматтер (type, id, updated, confidence)
- [ ] TL;DR/Ядро — **своими словами** (synthesis, не копипаста!)
- [ ] Каждая ссылка = **контекст** (что внутри? зачем переходить?)
- [ ] Структура по **смыслу**, не по типу файла
- [ ] **Обратные ссылки** (секция "Связанные файлы")
- [ ] **TODO** (для Concept/Topic) — что ещё изучить?

**Красные флаги:**
- ❌ Список ссылок без контекста
- ❌ Копипаста из источников
- ❌ Нет связей с другими MOC
- ❌ Нет личного применения/целей
- ❌ Алфавитный порядок без логики

---

## 🧬 Zettelkasten принципы (кратко)

### **1. Атомарность ссылок**
❌ `- [Fiber Protocol](protocols/fiber_protocol.md)`
✅ `- **[Fiber Protocol](protocols/fiber_protocol.md)** — 3-фазный протокол (+5 г/нед); troubleshooting GI distress`

### **2. Emergent structure**
Группировка **по смыслу и связям**, не по типу файла

### **3. Evergreen**
TODO + confidence + date_updated

### **4. Dense linking**
Каждый MOC связан с ≥3 другими MOC (КАК связано? ПОЧЕМУ важно?)

### **5. Personal synthesis**
Своими словами, не цитата

---

## 🎨 Примеры качества

### ✅ **Отличный пример (густые связи):**
```markdown
## Навигация по смежным темам
- **[Protein Consensus](protein_consensus.md)** — балансировка макронутриентов
- **[Iron Protocol](../../05_personal/health/protocols/iron_protocol.md)** — важно разносить приём (файбер ↓ абсорбция железа)
- **[80/20 Training](../../02_frameworks/health_training_80_20.md)** — файбер поддерживает восстановление
```

### ❌ **Плохой пример (изолированный MOC):**
```markdown
## Источники
- [Source 1](source1.md)
- [Source 2](source2.md)
```

---

## 🔧 Полезные команды

### **Проверить MOC (TODO — автоматизация):**
```bash
python3 tools/moc_lint.py --file "01_library/mocs/[name].md"
```

### **Найти битые ссылки:**
```bash
make links-validate
```

### **Найти обратные ссылки:**
```bash
grep -r "\[.*\](.*/[filename].md)" 01_library/
```

---

## 📚 Детальные правила

**→ См. полное руководство:**
- [MOC Zettelkasten Rules](../../../.cursor/rules/moc_zettelkasten.mdc) — все принципы и примеры
- [MOC Templates README](./README.md) — руководство по шаблонам
- [Project Principles](../../../90_meta/project_principles.md) — философия системы

---

**MOC = живая карта мышления, не список ссылок. Создавай сети, не папки.** 🗺️




