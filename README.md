
### Скачивание
1) Скачать файлы: git clone -b HW_2_Interface --single-branch https://github.com/etrehappy/BP_UE_Basic_Prj.git 

2) Скачать архив: [Google Диск](https://drive.google.com/drive/folders/1AT4x9XH1Nd9aMRT0jDL8yuACO0efQHsI?usp=drive_link)
    - содержит Characters (Mannequins и Mannequin_UE4) на 400 Мб

3) Извлечь содержимое в папку «BP_UE_Basic_Prj/Content» (рядом с MyContent)

### Что и как сделано 

<details><summary>Задание 2. UI</summary>

**Что**:
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
  
**Как**:

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
