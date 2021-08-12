# **MoveToTeammate**

Команда предназначена для сопровождения и оказания поддержки члену группы (*Teammate*).

## **Краткое описание**

1. Бот производит поиск члена группы (*Teammate*) и перемещается к нему. <br/>
   - Персонаж и *Teammate* должны находиться на одной карте, в одном инстансе и в одном внутриигровом регионе.
   - Область поиска *Teammate* может быть ограничена опциями [*CustomRegions*](#ref-CustomRegions),  [*ReactionRange*](#ref-ReactionRange) и [*ReactionZRange*](#ref-ReactionZRange).

2. Когда *Teammate* найден, бот следует к нему по кратчайшему пути.


# **Настройки команды**

<!--## **SupportOptions**
Комплексная опция, позволяющая задать *Teammate* и способ оказания ему поддержки.
- ***Teammate*** - переключатель, определяющий правило выбора члена группы:
   + *Leader* : лидер группы;
   + *Tank* : танк;
   + *Healer* : целитель;
   + Sturdiest : наиболее выносливый член группы (c наибольшим значением максимум ХР);
   + *SturdiestDD* : наиболее выносливый (сильный) дамагер (c наибольшим значением максимум ХР).  
   Урон, и хп персонажа сейчас считаются от ОУП'a с разными коэффициентами, поэтому можно принять MaxHP за приблизительную оценку DPS;
   + *Weakest* : слабейший член группы (c наименьшим значением максимума ХР);
   + *WeakestDD* : слабейший дамагер (c наименьшим значением максимума ХР).  
   Урон, и хп персонажа сейчас считаются от ОУП'a с разными коэффициентами, поэтому можно принять MaxHP за приблизительную оценку DPS;
   + *MostInjured* : наиболее израненный член группы (c наименьшим значением ХР);
   + *MostInjuredDD* : наиболее израненный дамагер (c наименьшим значением ХР).

- ***FoePreference*** - переключатель, определяющий правило выбора противника:
   + *TeammatesTarget* : противник, которого атакует заданный член группы;
   + *ClosestToPlayer* : Ближайший к игроку противник;
   + *ClosestToTeammate* : Противник, ближайший к поднадзорному члену группы;
   + *Sturdiest* : Самый выносливый противник (c наибольшим значением максимума ХР);
   + *Weakest* : Наименее выносливый противник (c наименьшим значением максимума ХР);
   + *MostInjured* : Наиболее раненый противник (с наименьшим НР);
 -->       

| **Наименование** | **Описание** 
|:-----------------|:-------------
|**SupportOptions**|**Комплексная опция, позволяющая задать [*Teammate*](#ref-Teammate) и способ оказания ему поддержки [*FoePreference*](#ref-FoePreference).**
|<a name ="ref-Teammate">*SupportOptions.**Teammate***</a> | Переключатель, определяющий правило выбора члена группы:<br/> - ***Leader*** : лидер группы;<br/>- ***Tank*** : танк;<br/>- ***Healer*** : целитель;<br/>- ***Sturdiest*** : наиболее выносливый член группы (c наибольшим значением максимума ХР);<br/>- ***SturdiestDD*** : наиболее выносливый (сильный) дамагер (c наибольшим значением максимум ХР).  <br/>Урон, и хп персонажа сейчас считаются от ОУП'a с разными коэффициентами, поэтому можно принять MaxHP за приблизительную оценку DPS;<br/>- ***Weakest*** : слабейший член группы (c наименьшим значением максимума ХР);<br/>- ***WeakestDD*** : слабейший дамагер (c наименьшим значением максимума ХР). <br/>Урон, и хп персонажа сейчас считаются от ОУП'a с разными коэффициентами, поэтому можно принять MaxHP за приблизительную оценку DPS;<br/>- ***MostInjured*** : наиболее израненный член группы (c наименьшим значением ХР);<br/> - ***MostInjuredDD*** : наиболее израненный дамагер (c наименьшим значением ХР).
|<a name ="ref-Teammate">*SupportOptions.**FoePreference***</a>|Переключатель, определяющий правило выбора противника:<br/> - ***TeammatesTarget*** : противник, которого атакует заданный член группы;<br/>- ***ClosestToPlayer*** : Ближайший к игроку противник;<br/>- ***ClosestToTeammate*** : Противник, ближайший к поднадзорному члену группы;<br/>- ***Sturdiest*** : Самый выносливый противник (c наибольшим значением максимума ХР);<br/>- ***Weakest*** : Наименее выносливый противник (c наименьшим значением максимума ХР);<br/>- ***MostInjured*** : Наиболее раненый противник (с наименьшим НР).
||**Дополнительные фильтры *Teammate* <br/>(категория "Optional")**
|<a name ="ref-CustomRegions">***CustomRegions***</a> | набор *CustomRegion*'ов, задающих область поиска *Teammate*. Подробное описание приведено в разделе [CustomRegionSet](../../General/CustomRegionSet-RU.md).
||**Управление боем**
|<a name ="ref-IgnoreCombat">***IgnoreCombat***</a> | флаг, предписывающий активировать режим игнорирования боя *IgnoreCombat* при следовании к *Teammate*.
|<a name ="ref-IgnoreCombatMinHP">***IgnoreCombatMinHP***</a> | минимальный уровень здоровья (в процентах), при котором может быть активирован режим игнорирования боя *IgnoreCombat* при следовании к *Teammate*.
|<a name ="ref-CombatDistance">***CombatDistance***</a> | расстояние до *Teammate*, на котором отключается режим игнорирования боя *IgnoreCombat*. <br/> При установке значения более ``5`` на [Mapper](../../Patches/Mapper/Mapper-RU.md) соответствующая область отображается окружностью, центром которой является соответствующая *Teammate*.
|<a name ="ref-AbortCombatDistance">***AbortCombatDistance***</a> | расстояние от *Entity*, за пределами которого бой принудительно прерывается. <br/> Бой снова активируются на расстоянии [*CombatDistance*](#ref-CombatDistance) от целевой *Entity*. При значении меньшем [*CombatDistance*](#ref-CombatDistance) или при выключенном флаге [*IgnoreCombat*](#ref-IgnoreCombat), опция отключается;
||**Прерывание команды**
|<a name ="ref-StopOnApproached">***StopOnApproached***</a> | флаг, завершающий выполнение команды после того как персонаж приблизился к *Teammate* на расстояние [*CombatDistance*](#ref-CombatDistance).
|<a name ="ref-TeammateSearchTime">***TeammateSearchTime***</a> | Время поиска в миллисекундах, в течение которого бот пытается обнаружить *Teammate*, удовлетворяющего критериям поиска.<br/> Команда прерывается, если до истечения заданного времени *Teammate* не будет обнаружен.<br/> Опция отключается при установке значения ``0``. При этом поиск продолжается неограниченное время.

---

# **Внутренние условия**

Персонаж должен состоять в группе.<br/>
В противном случае команда пропускается.


# **Завершение команды**

Команда завершается в следующих случаях:
- [*Teammate*](#ref-Teammate) не был найден в течение времени [*TeammateSearchTime*](#ref-TeammateSearchTime).
- Задан флаг [*StopOnApproached*](#ref-StopOnApproached) и персонаж приблизился к [*Teammate*](#ref-Teammate) на расстояние [*CombatDistance*](#ref-CombatDistance).

Принудительное завершение команды возможно одним из [перечисленных в статье способов](./../../General/ForcedQuesterActionTermination-RU.md).


# **Штатные команды - аналоги**

Отсутствуют.



# [Вернуться к содержанию](../../index.md)