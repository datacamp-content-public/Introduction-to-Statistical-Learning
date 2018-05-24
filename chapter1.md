---
title: Template Chapter 1
description: >-
  This is a template chapter.


---
## Ex 1.1

```yaml
type: NormalExercise
lang: r
xp: 100
skills: 1
key: c6055a198c
```

This is the assignment text. It should help provide students with the background information needed.
The instructions that follow should be in bullet point form with clear guidance for what is expected.

`@instructions`
- Instruction 1
- Instruction 2
- Instruction 3
- Instruction 4

`@hint`
- Here is the hint for this setup problem. It should get students 50% of the way to the correct answer.

`@pre_exercise_code`
```{r}
# Load datasets and packages here.
```
`@sample_code`
```{r}
# Your
# sample
# code
# should
# be
# ideally
# 10 lines or less,
# with a max
# of 16 lines.
```
`@solution`
```{r}
# Answer goes here
# Make sure to match the comments with your sample code
# to help students see the differences from solution
# to given.
```
`@sct`
```{r}
# Update this to something more informative.
success_msg("Some praise! Then reinforce a learning objective from the exercise.")
```





---
## Знакомство с датасетом

```yaml
type: NormalExercise

xp: 100

key: fffacd1c59
```

Перед работой с любым датасетом его необходимо обработать и ознакомиться с ним. Датасет candy уже загружен в Ваше рабочее пространство.

Данный датасет относительно небольшой, но в будущем Вы можете столкнуться с датасетами, в которых будет более тысячи наблюдений и десятки переменных, поэтому для примерного знакомства Вам будет достаточно первых несколько наблюдений. Встроенная функция head выводит в консоль первые 6 наблюдений, что позволяет ознакомиться со всеми переменными и сложить представление о датасете, однако количество выводимых наблюдений можно уточнить внутри самой функции. 

Иногда взгляда на первые наблюдения может быть недостаточно, тогда для анализа датасета можно использовать функцию describe из библиотеки psych, которая формирует краткий отчёт по каждой переменной. Вы можете подробнее ознакомиться с её выводом, выполнив задание.

`@instructions`
- Загрузите библиотеку psych с помощью функции library()
- Проанализируйте данный датасет.
- Выгрузите первые 10 наблюдений.

`@hint`
- Используйте функции describe() и head()

`@pre_exercise_code`
```{r}
candy <- read.csv(url("https://raw.githubusercontent.com/fivethirtyeight/data/master/candy-power-ranking/candy-data.csv"))
```
`@sample_code`
```{r}
# подключите библиотеку psych
___(psych)

# проанализируйте данный датасет
___(___)

# выгрузите первые 10 наблюдений
___(___, 10)
```
`@solution`
```{r}
# подключите библиотеку psych
library(psych)

# проанализируйте данный датасет
describe(candy) 

# выгрузите первые 10 наблюдений
head(candy, 10)
```
`@sct`
```{r}
#first instruction
test_student_typed("library(psych)", not_typed_msg = "Вы не подгрузили библиотеку psych. Внимательно прочтите инструкцию")

#second instruction
test_student_typed("describe(candy)", not_typed_msg = "Возникла проблема с анализом датасета. Внимательно прочтите инструкцию.")

#third instruction
test_student_typed("head(candy, 10)", not_typed_msg = "Возникла проблема с выгрузкой первых 10 наблюдений. Внимательно прочтите инструкцию.")

#General
test_error()
success_msg("Отлично!")
```



