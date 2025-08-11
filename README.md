# Требования к выполнению задачи

1. **Сделать вёрстку адаптивной** — обеспечить корректное отображение интерфейса на экранах всех размеров (desktop, tablet, mobile).
2. **Заменить иконки соцсетей с PNG на SVG**. При необходимости реализовать использование SVG-спрайта для оптимизации загрузки и удобства управления иконками.
3. **Проверить дизайн на наличие интерактивных элементов** — определить все области с интерактивным поведением (ссылки, кнопки, контролы) и внести изменения в вёрстку для соответствия дизайну.
4. **Использовать null CSS из внутренних наработок** — применить заранее подготовленный сброс/нормализацию стилей.
5. **Единый нейминг для CSS-переменных** — все переменные должны именоваться по единому стандарту с использованием префикса `--color-`.  
   Названия цветов берутся с ресурса [color-name.com](https://www.color-name.com/).

**Пример:**

```css
:root {
  --color-white: #ffffff;
  --color-black: #000000;
  --color-black-80: rgba(0, 0, 0, 0.8);
  --color-alice-blue: #ebf2ff;
  --color-true-blue: #0064d9;
  --color-blue-jeans-70: rgba(100, 171, 255, 0.7);
  --color-bright-gray: #eceff1;
  --color-light-slate-gray: #78909c;
  --color-nyanza: #e0f4e0;
}
```

6. **Подровнять весь CSS без БЭМ** — придерживаться единых принципов наименования классов и структуры без использования методологии БЭМ.

**Пример:**

```css
.managerContainer {
  display: grid;
  row-gap: 32px;
  justify-items: center;
}

.managerContainer.many {
  grid-template-columns: 1fr auto;
  gap: 73px;
}

@media (max-width: 767px) {
  .managerContainer.many {
    gap: 9px;
  }
}

.managerInfo {
  display: grid;
  row-gap: 4px;
  justify-items: center;
}

.managerInfo.many {
  grid-auto-flow: row;
  gap: 8px;
}

@media (max-width: 767px) {
  .managerInfo {
    row-gap: 10px;
  }
}

.managerName {
  color: var(--color-light-slate-gray);
  font-size: 18px;
  font-weight: 500;
  line-height: 1;
  text-align: center;
}

@media (max-width: 767px) {
  .managerName {
    font-size: 24px;
  }
}

.managerAddressContainer,
.managerPhoneContainer {
  display: grid;
  grid-auto-flow: column;
  column-gap: 4px;
}

.managerAddressContainer.many,
.managerPhoneContainer.many {
  grid-template-columns: auto 1fr;
}

.managerAddressContainer,
.managerAddressContainer.many {
  color: var(--color-true-blue);
  align-items: start;
}

.managerPhoneContainer,
.managerPhoneContainer.many {
  align-items: center;
}

.managerAddressIcon {
  display: inline-block;
  margin-top: 2px;
}

.managerAddress,
.managerPhone {
  font-size: 12px;
  font-weight: 500;
  line-height: 22px;
  text-align: center;
}

.contactContainer {
  display: grid;
  grid-auto-flow: column;
  column-gap: 60px;
}

.contactContainer.many {
  gap: 10px;
  height: fit-content;
}

@media (max-width: 767px) {
  .contactContainer.many {
    display: grid;
    grid-auto-flow: column;
  }
}

.contact {
  display: grid;
  grid-auto-flow: row;
  row-gap: 4px;
  justify-items: center;
}

.contactText {
  color: var(--color-light-slate-gray);
  font-size: 14px;
  font-weight: 600;
  line-height: 16px;
}

.iconCircle {
  width: 62px;
  height: 62px;
  border-radius: 100%;
  display: grid;
  justify-content: center;
  align-items: center;
}

.iconCircle.phone {
  background-color: var(--color-alice-blue);
}

.iconCircle.whatsapp {
  background-color: var(--color-nyanza);
}

.iconCircle.many {
  width: 42px;
  height: 42px;
}

.phoneIcon {
  font-size: 36px;
}

.phoneIcon.many {
  font-size: 24px;
}

.whatsappIcon {
  font-size: 42px;
}

.whatsappIcon.many {
  font-size: 34px;
}

@media (max-width: 767px) {
  .whatsappIcon.many {
    font-size: 24px;
  }
}

.divider {
  margin: 14px 0px !important;
}

.divider:last-child {
  display: none;
}
```
