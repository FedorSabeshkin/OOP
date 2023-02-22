## Классы поведения
На данном этапе мне необходимо задать возможный каркас поведения объектов системы и их взаимодействие друг с другом.  

Для всех классов справедливо наличие метода equals от общего предка General, который позволяет определять равны ли объекты.   
Для каждого метода меняющего состояние объекта - существуют методы получения статуса выполнения операции - успешна, вызвал ошибку, ранее не вызывался.  
Logger, ErrorHandler - стандартные реализации, по аналогии с другими проектами  

**Health** - Обертка над числовым типом данных  

*Поля:*  
Integer currentHealth - числовое представление значения текущего здоровья  
Integer maxHealth - числовое представление значения Мах здоровья  
 
*Методы:*   
damage(Health damage) - уМеньшает здоровье на переbodyданное кол-во единиц  
treat(Health addingHealth) - уВеличивает здоровье на переданное кол-во единиц    
toString() - показывает внутреннее числовое значение     

**Power** - Обертка над числовым типом данных      
*Поля:*    
Integer value - числовое представление значения  

*Методы:*    
take(Power tookPower) - уМеньшает силу на переданное кол-во единиц  
add(Power addingPower) - уВеличивает силу на переданное кол-во единиц    
toString() - показывает внутреннее числовое значение   

**Warrior**  
*Поля:*    
Health health  
Power power    
Outfit outfis - обмундирование бойца     
WarriorId Id - идентификатор бойца    
  
*Методы:*     
hit(BodyPart bodyPartTarget) - наносит удар в заданную часть противника. Удар будет нанесен с имеющимся значением Power.  
protect(BodyPart bodyPartTarget) - защищает заданную часть бойца от удара противника.  

**Battle**  
*Поля*  
Hod hod  

*Методы:*   
matchHitProtect(BodyPart bodyPartTargetForHit, BodyPart bodyPartTargetForProtect) - сопоставление 

**Hod**  
*Поля*  
WarriorId beatingWarriorId    
WarriorId protectiveWarriorId    
BodyPart bodyPartTargetForHit  
BodyPart bodyPartTargetForProtect  
