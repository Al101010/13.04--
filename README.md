# 13.04--
Листинг:
    - сбока не проходит из-за этого файла:
        НЕУДАЧНЫХ  тестов src /js /_____/widget.test.js:

import { InnFormWidget } from '../widget';
или
FAIL  src/js/__tests__/widget.test.js
  ● widget should render


test('widget should render', () => {
  document.body.innerHTML = '<div class="container"></div>';

  const container = document.querySelector('.container');
  const widget = new InnFormWidget(container);

  widget.bindToDOM();

  expect(container.innerHTML).toEqual(InnFormWidget.markup);
});

test('widget should add valid class', () => {
  document.body.innerHTML = '<div class="container"></div>';

  const container = document.querySelector('.container');
  const widget = new InnFormWidget(container);

  widget.bindToDOM();

  widget.input.value = '7715964180';
  widget.submit.click();

  expect(widget.input.classList.contains('valid')).toEqual(true);
});


    - удалил этот файл, но записал его в READMY.md:


import { InnFormWidget } from '../widget';

test('widget should render', () => {
  document.body.innerHTML = '<div class="container"></div>';

  const container = document.querySelector('.container');
  const widget = new InnFormWidget(container);

  widget.bindToDOM();

  expect(container.innerHTML).toEqual(InnFormWidget.markup);
});

test('widget should add valid class', () => {
  document.body.innerHTML = '<div class="container"></div>';

  const container = document.querySelector('.container');
  const widget = new InnFormWidget(container);

  widget.bindToDOM();

  widget.input.value = '7715964180';
  widget.submit.click();

  expect(widget.input.classList.contains('valid')).toEqual(true);
});
