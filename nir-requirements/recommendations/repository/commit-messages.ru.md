# Сообщения коммитов — памятка студенту

Эти советы необязательны. Но по хорошим сообщениям историю коммитов легко прочитать: руководителю сейчас, а вам через три месяца. На защите ничего из этого не проверяют.

## Семь правил

1. Отделяйте тему от тела пустой строкой.
2. Держите тему в пределах примерно 50 символов.
3. Начинайте тему с заглавной буквы.
4. Без точки в конце темы.
5. Пишите тему в повелительном наклонении: по-английски она должна продолжать фразу «If applied, this commit will ...».
6. Строки тела делайте не длиннее 72 символов.
7. В теле объясните, что изменилось и зачем. Как именно, видно из диффа.

## Типы

Тему можно начать с префикса из Conventional Commits. Типы те же, что у веток: `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`; знак `!` после типа помечает ломающее изменение. При squash and merge заголовок PR становится сообщением коммита в `main`, поэтому пишите его по тем же правилам.

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
- [Version Control with Git: Tracking Changes](https://swcarpentry.github.io/git-novice/04-changes.html), Software Carpentry — как добавлять изменения в индекс логически связанными частями.
