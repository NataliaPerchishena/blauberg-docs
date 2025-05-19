> [!info]- різний принцип побудови ключів у формі для MS+PCHRU та BVU+UVU+ERV

# BVU+UVU+ERV форма
- лейбл для `location` - використовується функція `p_trans`
- значення в `drop-down` списках для полів `supply_pre_heater`, `supply_heater`, `supply_post_heater`, `supply_cooler`, `temperature_settings_mode`  - группа `selects`
- лейбл для `інші ключів`, які не перераховані вище - ключі `з відповідної групи`, імʼя якої = імені калькулятора (для bvu це группа ключів nrvu_bvu, uvu - nrvu_uvu, erv - erv_hrv)

# MS+PCHRU форма
- лейбли для полів `supply_cooler_water_temperature_after`, `supply_cooler_water_temperature_in` та ще ряд (**дивись файл группи parametrs**) - функція `p_trans`
- `` - группа selections
- `` - з відповідної групи
- значення в drop-down списку `control manuf` - з **??**

## PDF MS+PCHRU
*вивід назви параметру, без використання ключа*
- `height`, `width`, `lenght` в `overall dimensions` таблиці - виводиться назва параметру (**only pdf**)

# Zern
- значення в drop-down списку для полів `material`  - группа `selects`

# Загальний принцип побудови ключів

  
### Термінологія
- функція `p_trans` - Якщо є переклад ключа в цій группі, тоді переклад береться з цієї группи (спершу пошук перекладу по локалі, потім пошук перекладі по дефолтній локалі), інакше переклад береться з группи відповідного калькулятора 
- `selects` группа ключів - /home/frontend/blaub/laravel/resources/lang/en/selects.php
