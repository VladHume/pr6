
# Test Case #0 — "Hello world!"

Це базовий тест на перевірку, що програма виводить `Hello world!` без жодних помилок компіляції чи попереджень від Valgrind.

## [Код](https://github.com/VladHume/pr6/blob/main/task.c)

## Компіляція

```bash
gcc -Wall -Wextra -pedantic -g -o task task.c
```

- `-Wall -Wextra -pedantic` — вмикають усі основні попередження компілятора.
- `-g` — додає відлагоджувальну інформацію для Valgrind.

## Запуск

```bash
./task
```

**Очікуваний результат:**

```
Hello world!
```

## Перевірка через Valgrind

```bash
valgrind --leak-check=full ./task
```

**Valgrind:**

![image](https://github.com/user-attachments/assets/0bae64b3-8a2b-4b6f-b39b-9ad3a6ade3d5)

Це означає, що немає помилок, витоків пам'яті або попереджень.
