# CryLevelConvert, CryDumper и Mission_Extract | Как извлечь содержимое уровня Warface

Благодаря связке из CryLevelConvert (далее - «CLC»), CryDumper (далее - «дампер») и Mission_Extract вы сможете получить следующие данные уровня:
1. Динамические сущности (в том числе и архетипы сущностей);
2. Flow Graph;
3. Trackview (треки уровня);
4. Данные о времени суток (TimeOfDay);
5. Слои текстуры террейна;
6. Статическую геометрию;
7. Навигацию AI (якоря для ИИ, AIPoint);
8. Карта высот ландшафта (Terrain);
9. Координаты растительности (Vegetation);
10. Данные о растительности (Vegetation);
11. Данные для инструмента освещения местности (Terrain Lighting Tool)

При этом важно понимать, зачем нужен каждый инструмент. CLC позволяет вам получить пункты 1-5 из списка выше. Пункты 6-9 - зона ответственности дампера. А за пункты 10-11, а также за правильный запуск CLC и последущую сортировку файлов после его работы, отвечает Mission_Extract.

## Где найти данные программы?

Программы и их компоненты (CLC, дампер и Mission_Extract) входят в состав редактора WF MOD SDK. CLC и Mission_Extact располагаются по пути \[MSDK_Editor/Mission_Extract/\], а CryDumper - \[MSDK_Editor/Bin64/\].

## Мне нужно что-то приготовить перед началом?

Да, для правильной работы CLC вам необходимо найти и перенести в папку \[MSDK_Editor/Mission_Extract/\] папку \[EntityArchitypes\], она расположена по пути \[GameData.pak/Libs/\].

## Как пользоваться программами?

Следуйте следующей инструкции:
1. В папке с игрой вы ищете карту, которую хотите извлечь (она должна быть разработана не позднее 2020 года);
2. Как только вы определились, копируйте из папки с картой pak-архив \[level.pak\] по следующему пути: \[MSDK_Editor/Mission_Extract/\];
3. Если это необходимо, расшифровываете при помощи PakDecrypt \[level.pak\]. После расшифровки у вас появится файл \[level.pak.zip\, удаляете оригинал \[level.pak\] и переименовываете zip-архив вот так \[level.pak\] (то есть  просто убираете расширение \[.zip\]);
4. Далее запускаете [Mission_Extract.exe] и следуете указаниям программы;
5. Итогом работы программы станет папка с названием карты, полученную папку вам необходимо ПЕРЕМЕСТИТЬ в папку \[MSDK_Editor/Game/Levels/\];
6. Далее вы ищете \[CryDumper.exe\], который расположен в папке \[MSDK_Editor/Bin64/\]. Запускаете его, и вы должны увидеть консоль CryEngine. Введите команду:

```
  map Name_Level
```

Name_Level (Название уровня) - копируйте с папки уровня, которую вы извлекли (например: ``` map tdm_downtown ```)

7. Теперь нажмите Enter. После завершения процесса в папке \[MSDK_Editor/\] будут доступны файлы: .
8. Все данные файлы нужно переместить в папку с картой \[MSDK_Editor/Game/Levels/ВАША_КАРТА/Setting/\] и по желанию, но я всё же буду настаивать, вам нужно их отсортировать, по имеющимся папкам;

Поздравляю! Вы извлекли всё возможное содержимое уровня (на данный момент).

## Источники

Часть документации была создана при помощи материалов с удалённого сайта [WFCRYDOC](https://wfcrydoc.fandom.com/ru/wiki/CryLevelConvert_и_CryDumper). Автор не претендует на авторство к оригинальным материалам.

Документация по CryLevelConvert: https://github.com/prophetl33t/CryLevelConvert

Документация по Mission_Extract: https://github.com/wfom/Mission-Extract