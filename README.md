# markdown
Методы сбора и обработки данных

---

### 📌 Методы сбора и обработки данных

```markdown
# 📥 Методы сбора и обработки данных — мои конспекты

## Источники данных

- **API** — программный доступ
- **Веб-скрапинг** — парсинг сайтов
- **Базы данных** — SQL, NoSQL
- **Файлы** — CSV, JSON, Excel
- **Логи** — серверные журналы

---

## Инструменты

| Инструмент | Назначение |
| :--- | :--- |
| **pandas** | Обработка таблиц |
| **requests** | HTTP-запросы |
| **BeautifulSoup** | Парсинг HTML |
| **Scrapy** | Фреймворк для скрапинга |
| **Airbyte** | Сбор данных из 300+ источников |

---

## Пример: парсинг сайта

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")
titles = soup.find_all("h2")
for t in titles:
    print(t.text)
