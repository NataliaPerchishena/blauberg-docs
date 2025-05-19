
> [!info]- Необходимо поменять подход на расчет по двум сезонам одновременно 
# Type of Unit
- `ERV` (энтальпийные, они же `hygroscopic`)
- `HRV` (конденсационные)

*Отображается и в `automatic`, и в `manual` режимах*
# Recovery type
- `counterflow`
- `crossflow`
- `rotary`

*Отображается только в `automatic` режиме*
## Связь между Type of Unit и Recovery type
- Данные поля взаимозависимы
- Выбираются в любой последовательности
- При выборе `HRV` доступны все три типа `Recovery type`
- При выборе `ERV` доступны только `crossflow` и `rotary`
- По умолчанию в `automatic` режиме выбран `ERV` `crossflow`
- Если выбран `counterflow`, то не должно быть возможности выбрать `ERV`
- Также если выбрать `ERV`, то не должно быть опции выбрать `counterflow`
- Если в ручном режиме выбран `ERV`, то в список моделей не должны попадать установки с `Recovery type` `counterflow`
## Комбинация ERV Counterflow
На данный момент такая комбинация не доступна, но может появиться в будущем
## Используемые DLL
- Для `counterflow` и `crossflow` используется `Blauberg DLL`
- Для Rotary используется `Heatex DLL`
## Loсation
В данном калькуляторе Location не используется вообще
## Структура Akeneo
В `Akeneo` три поля будут ответственны за `Heat Exchanger`
- `erv_hrv_heat_exchanger_recovery_type` (required)
- `erv_hrv_heat_exchanger_sku` (**required**)
- `erv_hrv_heat_exchanger_enthalpy_sku` (not required)
### Терминология
Все рекуператоры делятся на конденсационные и энтальпийные
По типу рекуперации они также делятся на 
- `counterflow`
- `crossflow`
- `rotary`

`counterflow` и `crossflow` относят в группу `plate` (пластинчатые)
