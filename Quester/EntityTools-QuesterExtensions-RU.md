# **Расширение для роли [*Quester*](./General/Glossary-RU.md#ref-Quester)**

[*Quester*](./General/Glossary-RU.md#ref-Quester) - это [подсистема](https://www.neverwinter-bot.com/forums/viewtopic.php?p=43900#p43900) бота [Astral](https://www.neverwinter-bot.com/forums/index.php), предназначенная для управления одним персонажем и выполнения заранее определенной последовательности действий, которая называется ***профиль (рrofile)***.

Профили создаются в специальном [графическом редакторе](https://www.neverwinter-bot.com/forums/viewtopic.php?p=43901#p43901) путем добавления команд (называемых "*action*"), каждая из которых имеет собственные [настройки](https://www.neverwinter-bot.com/forums/viewtopic.php?p=43902#p43902) и условия запуска ([*conditions*](https://www.neverwinter-bot.com/forums/viewtopic.php?p=43910#p43910)). <br/>
Команды, как правило, управляют игровым персонажем в игре и совершают несколько внутриигровых действий для достижения нужного результата. Например, взаимодействие с неигровым персонажем ([*InteractSpecificNPC*](Actions/Astral-Actions-RU.md#ref-InteractSpecificNPC)), выполняет перемещение игрового персонажа к месту нахождения NPC, активацию диалога и последовательный выбор заранее заданных вариантов ответа.

Плагин **EntityTools** реализует дополнительные команды и условия, которые могут быть использованы в профиля [*Quester'a*](./General/Glossary-RU.md#ref-Quester), а также инструменты для их настройки.

---

## **Команды**
1. [MoveToEntity](Actions/MoveToEntity-RU.md) : патрулирование по заданному маршруту, поиск и нападение на заданную [*Entity*](../../EntityToolsDocs/General/EntityIdentification-RU.md)[^1].
2. [InteractEntities](Actions/InteractEntities-RU.md) : патрулирование по заданному маршруту, поиск и взаимодействие с заданной [*Entity*](../../EntityToolsDocs/General/EntityIdentification-RU.md).
3. [MoveToTeammate](Actions/MoveToTeammate-RU.md) : сопровождение и оказание поддержки члену группы.
4. [PickUpMissionExt](Actions/PickUpMissionExt-RU.md) : взятие квестового задания (миссии) у конкретного неигрового персонажа (NPC) или у вспомогательной внутриигровой диалоговой подсистемы.
5. [TurnInMissionExt](Actions/TurnInMissionExt-RU.md) : сдача квестового задания (миссии) конкретному неигровому персонажу (NPC).
6. [AddIgnoredFoes](Actions/AddIgnoredFoes-RU.md) : задает список противников, игнорируемых во время боя.
7. [RemoveIgnoredFoes](Actions/RemoveIgnoredFoes-RU.md) : удаление противников, игнорируемых во время боя, которые были добавлены командой [*AddIgnoreFoes*](./RemoveIgnoredFoes-RU.md).
8. [ChangeInstanceToLeader](Actions/ChangeInstanceToLeader-RU.md) : переход игрового персонажа на инстанс текущей карты, в котором находится лидер группы.
9. [UpgradeItem](Actions/UpgradeItem-RU.md) : Повышение ранга (уровня) предмета, заданного идентификатором. К таким предметам относятся волшебные камни и руны, знаки скакунов, артефактная экипировка и т.д.

---

## **Условия**
1. [EntityCount](Conditions/EntityCount-RU.md) : подсчёт количества *Entity* и сравнение его с референтным значением.
2. [EntityProperty](Conditions/EntityProperty-RU.md) : сопоставление значения заданного свойства ближайшего *Entity* с референтным значением.
3. [TeamMemberCount](Conditions/TeamMemberCount-RU.md) : подсчёт количества членов группы и сравнивает его с референтным значением.
4. [TeamLeaderMapInstance](Conditions/TeamLeaderMapInstance-RU.md) : сравнение инстанса, в котором находится игрок, с инстансом, в котором находится лидер группы.
5. [CheckShard](Conditions/CheckShard-RU.md) : проверка названия сервера, к которому подключен игровой клиент.
6. [IsInCustomRegionSet](Conditions/IsInCustomRegionSet-RU.md) : проверка местонахождения персонажа относительно области, заданной набором [*CustomRegion'ов*](../General/Glossary-RU.md#ref-CustomRegions).

[^1]: *Entity* - это внутриигровой объект, являющийся частью игрового процесса или декорацией. К *Entity* относятся все игровые или неигровые персонажи, спутники, противники и босы подземелий, некоторые предметы интерьера, порталы и т.д.