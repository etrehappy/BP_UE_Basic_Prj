
### Скачивание
1) Скачать файлы: git clone -b HW_4_first_mechanic --single-branch https://github.com/etrehappy/BP_UE_Basic_Prj.git 

2) Скачать архив: [Google Диск](https://drive.google.com/drive/folders/1AT4x9XH1Nd9aMRT0jDL8yuACO0efQHsI?usp=drive_link)
    - содержит Characters (Mannequins и Mannequin_UE4) на 400 Мб

3) Извлечь содержимое в папку «BP_UE_Basic_Prj/Content» (рядом с MyContent)

### Что и как сделано 

<details><summary>Задание 2. UI<p></p></summary>

**Что сделано**:
 - добавлено главное меню, кнопки «Старт» и «Выход»

<div style="text-align: center;">
    <img src="./imgs_for_readme/main_menu.jpg" alt="Главное меню" width="500" height="341">
    <p></p>
</div>
    
 - добавлен HP-бар.
 <div style="text-align: center;">
    <img src="./imgs_for_readme/hp_bar.jpg" alt="HP" width="600" height="297">
</div>
<p></p>
  
**Как сделано**:

1) В ./MyContent/Game/ добавлены
    - Level «MainMenu» в /Maps
    - пустой game mode «BP_MainMenuGameMode» в /Blueprints
    - Widget для кнопок "Start" и "Exit" в главном меню в /UI
    - Widget для HealthBar в /UI/UI_HealthBar
    
2) В Level «MainMenu» добавлены ноды для отображения Widget Blueprint

3) В  ./ThirdPerson/Blueprints изменен BP_ThirdPersonCharacter: 
    - добавлен HealthComponent (только прямоугольник HP)

4) Текстуры из интернета: 
    - ./MyContent/Game/UI - для главного меню
    - ./MyContent/Game/UI/UI_HealthBar - для шкалы здоровья

</details>

<details><summary>Задание 4. Первая механика<p></p></summary>

**Что сделано**:
 - изменение HP при уроне\исцелении

 <div style="text-align: center;">
    <img src="./imgs_for_readme/hp_bar_damage.jpg" alt="HP damage" width="600" height="400">
</div>
 
 - обработка смерти 
 <div style="text-align: center;">
    <img src="./imgs_for_readme/zero_health_menu.jpg" alt="Death" width="600" height="400">
</div>
 


<p></p>
  
**Как сделано**:

1) В Level «ThirdPersonMap» добавлено
    - обработка события OnDeathMainCharacter

2) WBP_HUD:
    -  при инициализации сохраняет ссылку на HealthComponent для WBP_HealthBar

3) WBP_HealthBar:
    -  использует HealthComponentRef, чтобы обновлять состояние HealthPercentage

4) BP_ThirdPersonCharacter:
    - обрабатывает состояние смерти    

5) AC_HealthComponent:
    - обрабатывает урон в функции ProcessDamage, вызвает функцию UpdateHealth, уведомляет BP_ThirdPersonCharacter о смерти через "Call On Zero Health"
    - обновляет здоровье в функции UpdateHealth, уведомлеяет WBP_HealthBar через "Call On Health Updated"

6) BP_DamageZone и BP_HealZone
    - устроены одинаковы, но разные названия переменных
    - проверяет пересечение с BP_ThirdPersonCharacter
    - наносит урон всем, кто находится в зоне

</details>


<details><summary>Задание 8. Locomotion<p></p></summary>

**Что сделано**:
 - и

 <div style="text-align: center;">
    <img src="./imgs_for_readme/hp_bar_damage.jpg" alt="HP damage" width="600" height="400">
</div>



<p></p>
  
**Как сделано**:

1) В 
    - о


</details>
