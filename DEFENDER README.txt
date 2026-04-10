# ⚠️ Windows Defender — ложное срабатывание / False Positive

---

## 🇷🇺 Русский

### Почему Windows Defender может заблокировать программу?

Entropy Miner собирает аппаратную энтропию — движения мыши, скорость нажатий клавиш, данные микрофона, Wi-Fi сигналы и снимки экрана. Для сбора движений мыши и клавиатуры программа использует системный механизм Windows под названием «глобальные хуки» (SetWindowsHookEx). Этот же механизм используется клавиатурными шпионами (кейлогерами), поэтому Windows Defender иногда ошибочно принимает программу за вредоносную.

Другие антивирусы (Kaspersky, ESET, Avast, DrWeb и др.) не обнаруживают угроз, потому что анализируют поведение программы глубже и видят, что она не отправляет перехваченные данные на сторонние серверы.

### Безопасность ваших данных

- **Все данные хранятся только локально на вашем компьютере.** Программа не отправляет нажатия клавиш, движения мыши или аудиозаписи куда-либо.
- **Данные шифруются.** Коды клавиш хэшируются алгоритмом SHA-256 прямо в момент нажатия. Восстановить исходные символы из хэша невозможно.
- **В блокчейн отправляются только числовые координаты «тапов»** — случайные точки, вычисленные на основе собранной энтропии. Никакие персональные данные в блокчейн не попадают.
- **Исходный код открыт для проверки.** Вы можете убедиться в этом самостоятельно.

### Как разрешить запуск программы

**Способ 1 — Добавить папку в исключения (рекомендуется):**

1. Откройте **Параметры Windows** → **Конфиденциальность и безопасность** → **Безопасность Windows** → **Защита от вирусов и угроз**.
2. Прокрутите вниз до **Параметры защиты от вирусов и угроз** → нажмите **Управление параметрами**.
3. Прокрутите до раздела **Исключения** → нажмите **Добавление или удаление исключений**.
4. Нажмите **Добавить исключение** → **Папка** → выберите папку с программой.

**Способ 2 — Восстановить удалённый файл:**

1. Откройте **Безопасность Windows** → **Защита от вирусов и угроз** → **Журнал защиты**.
2. Найдите запись об удалённом файле.
3. Нажмите на неё → выберите **Действия** → **Разрешить**.

**Способ 3 — Временно отключить защиту в реальном времени (на время установки):**

1. **Безопасность Windows** → **Защита от вирусов и угроз** → **Управление параметрами**.
2. Отключите **Защита в реальном времени**.
3. Установите и запустите программу.
4. Добавьте папку программы в исключения (Способ 1).
5. Включите защиту обратно.

---

## 🇬🇧 English

### Why might Windows Defender block this application?

Entropy Miner collects hardware entropy — mouse movements, keystroke timing, microphone data, Wi-Fi signals, and screen snapshots. To capture mouse and keyboard activity, the application uses a Windows system mechanism called "global hooks" (SetWindowsHookEx). This same mechanism is used by keyloggers, which is why Windows Defender may mistakenly flag the application as malicious.

Other antivirus software (Kaspersky, ESET, Avast, DrWeb, etc.) does not flag the application because they analyze program behavior more deeply and can see that it does not transmit intercepted data to external servers.

### Your Data Security

- **All data is stored locally on your computer only.** The application does not send keystrokes, mouse movements, or audio recordings anywhere.
- **Data is encrypted.** Key codes are hashed using SHA-256 at the moment of each keystroke. It is impossible to recover the original characters from the hash.
- **Only numerical "tap" coordinates are sent to the blockchain** — random points calculated from the collected entropy. No personal data ever reaches the blockchain.
- **The source code is available for review.** You can verify this yourself.

### How to allow the application to run

**Method 1 — Add folder to exclusions (recommended):**

1. Open **Windows Settings** → **Privacy & Security** → **Windows Security** → **Virus & threat protection**.
2. Scroll down to **Virus & threat protection settings** → click **Manage settings**.
3. Scroll to **Exclusions** → click **Add or remove exclusions**.
4. Click **Add an exclusion** → **Folder** → select the folder.

**Method 2 — Restore a deleted file:**

1. Open **Windows Security** → **Virus & threat protection** → **Protection history**.
2. Find the entry for the deleted file.
3. Click on it → select **Actions** → **Allow**.

**Method 3 — Temporarily disable real-time protection (during installation):**

1. **Windows Security** → **Virus & threat protection** → **Manage settings**.
2. Turn off **Real-time protection**.
3. Install and launch the application.
4. Add the application folder to exclusions (Method 1).
5. Turn real-time protection back on.