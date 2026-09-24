# Сообщения коммитов — памятка студенту

Необязательно. Хорошее сообщение делает историю читаемой для руководителя сейчас и для вас через три месяца. Ничто отсюда не проверяется на защите.

## Семь правил

1. Отделяйте тему от тела пустой строкой.
2. Держите тему в пределах примерно 50 символов.
3. Начинайте тему с заглавной буквы.
4. Без точки в конце темы.
5. Повелительное наклонение: тема завершает фразу «Если применить, этот коммит ...».
6. Переносите строки тела на 72 символах.
7. Тело объясняет, что и почему; дифф показывает, как.

## Типы

Необязательный префикс из Conventional Commits, совпадающий с типами веток: `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`; знак `!` после типа помечает ломающее изменение. При squash and merge заголовок PR становится коммитом в `main`, поэтому заголовок следует тем же правилам.

## Примеры

```
feat: add contrastive loss for the retrieval baseline

Replaces the triplet loss chosen in ADR-0003. The metric on the dev
split rises from 0.61 to 0.68 (MLflow run 4f2c...). Batch size stays 64.
```

Сообщения, которые ничего не говорят: `fix`, `finally works`, `changes`, `WIP`.

## Дополнительные материалы

- [How to Write a Git Commit Message](https://cbea.ms/git-commit/), Крис Бимс — семь правил с обоснованием.
- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/ru/v1.0.0/) — префиксы типов, русская редакция.
- [Version Control with Git: Tracking Changes](https://swcarpentry.github.io/git-novice/04-changes.html), Software Carpentry — индексирование логическими порциями.
