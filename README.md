# 🧠 SQL CLI vs Prisma/Drizzle - Guía Novia + Devs

**SQL directo = 80% más rápido que ORMs.** 2hrs basics, production ready.

## 🎯 SQL en 2 Horas (Novia)

### 1. Bases (15min)
```
-- supabase.com/dashboard → SQL Editor
SELECT * FROM stocks WHERE symbol = 'AAPL';
```

### 2. Leer (20min)
```
SELECT symbol, price FROM stocks WHERE price > 50 ORDER BY price DESC LIMIT 5;
```

### 3. Escribir (25min)
```
INSERT INTO stocks (symbol, price) VALUES ('TSLA', 250.5);
UPDATE stocks SET price = 260 WHERE symbol = 'TSLA';
```

### 4. JOINs (20min)
```
SELECT u.name, s.symbol FROM users u JOIN stocks s ON u.fav_stock = s.symbol;
```

## 👨‍💻 CLI > ORMs (Devs)
| Metric | SQL CLI | Prisma | Drizzle |
|--------|---------|--------|---------|
| Bundle | **0kb** | 500kb+ | 7kb |
| Cold Start | ⚡10ms | 🐌2s | ✅50ms |
| RLS | Native | Config | Config |

## 🚀 Práctica Live
1. **Copia** `sql/novia-practice.sql` abajo
2. **Pega** en Supabase SQL Editor
3. **¡Ver realtime!** en Table Editor

<details>
<summary>📋 sql/novia-practice.sql (Copia aquí)</summary>

```
-- 🌟 PRÁCTICA NOVIA - Copia en Supabase
INSERT INTO stocks (symbol, price, ai_prediction) VALUES 
('AAPL', 220.5, 'Sube mañana'),
('TSLA', 250.0, 'Volátil bullish'),
('GOOG', 180.2, 'Estable');

-- Stocks caros
SELECT * FROM stocks WHERE price > 200 ORDER BY price DESC;

-- Predicciones positivas
SELECT symbol, ai_prediction FROM stocks WHERE ai_prediction LIKE '%sube%';
```
</details>

**👩‍💻 Hecho por @ioniacob con el equipo de bigbangsmm para [novia] - Dec 2025**


