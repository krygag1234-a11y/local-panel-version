# local-panel-version

Стабильный fork [olcrtc-manager-panel](https://github.com/BigDaddy3334/olcrtc-manager-panel) с применёнными патчами для [Olc-cost-l](https://github.com/krygag1234-a11y/Olc-cost-l).

## Назначение

Этот репозиторий служит **fallback-версией** manager панели на случай, если upstream обновится и сломает совместимость с нашими патчами.

## Ветки

- `stable-v1` — проверенная версия на базе `ad8ec6f` с патчами
  - Включает golden-panel изменения
  - Поддержка bridge profiles
  - Совместима с текущей версией olcrtc

## Использование

```bash
# Вместо upstream:
git clone https://github.com/BigDaddy3334/olcrtc-manager-panel.git

# Используйте stable fork:
git clone -b stable-v1 https://github.com/krygag1234-a11y/local-panel-version.git
```

## Обновление

При обновлении stable версии:

1. Клонировать нужный коммит из upstream
2. Применить патчи из Olc-cost-l
3. Протестировать сборку
4. Запушить в новую ветку (например, `stable-v2`)

## Связь с Olc-cost-l

- Патчи: `Olc-cost-l/scripts/apply-olcrtc-patches.sh`
- Конфигурация: `Olc-cost-l/data/upstream-pins.json`
- Golden panel: `Olc-cost-l/packaging/golden-panel/`
