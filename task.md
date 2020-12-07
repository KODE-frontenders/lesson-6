# KODE lesson 6

## Вопросы

1. Для полей ввода телефона или email на экрана авторизации для телефона указана маска. Необходима ли какая-либо маска для этого поля?
2. Экран 1.6. При каких условиях должна сниматься блкировка с кнопки "Войти", например, любые изменения значения поля и отличное значение от
только что не прошедего проверку?
3. Экран 2.5. Отображаемое сообщение об ошибке - ответ сервера?
4. После успешной регистрации, какое окно должно отобразиться: запрос авторизации / подтвержение. Путает на экране 1.5 лоадер с текстом 
"Отправляем код подтверждения..."
5. Когда должны пропадать сообщения об ошибке, при начале ввода значения в поле, или должна быть какая-то задержка, после которой сообщение пропадет?

---

## Components
### Atoms

- PrevButton - кнопка "Назад"
  * path - путь для перенаправления
  * clickHandler - обработчик клика
- InputField - поле ввода
  * placeholder
  * inputHandler - обработчик ввода
  * disabled
  * value
- Button
  * text - текст кнопки
  * clickHandler - обработчик клика
  * disabled - состояние кнопки
- LinkButton
  * path - путь для перенаправления
- Checkbox 
  * checked - сосотояние чекбокса
  * changeHandler - обработчик изменения состояния чекбокса
- UserIcon
- Loader
- FailureLoader
- SuccessLoader
- Title - заголовок страницы
  * text - текст поля
- KeyboardKey 
- KeyboardInput

### Molecules 

- Header - заголовок

  Atoms:
  * PrevButton
  * Ttile

  props: 
  * path
  * clickHandler 
  * text

- FormInput - поле ввода с заголовком, подскаской и сообщением об ошибке

  Atoms:
  * InputField

  props:
  * title - заголовое инпута
  * helpMessage - подсказка
  * errorMessage - сообщение об ошибке
  * placeholder
  * error - сосотояние ошибки
  * inputHandler - обработчик ввода инпута
  * disabled
  * value

- SubmitMessage - сообщение о результате запроса

  Atoms:
  * UserIcon

  props: 
  * text - текст сообщения
  * error - тип сообщения 

- LoaderWithText

  Atoms: 
  * Loader
  * FailureLoader
  * SuccessLoader

  props: 
  * type - тип лоадера
  * text - текст лоадера

- PPDBlock - блок СОПД

  Atoms: 
  * Checkbox

  props: 
  * checked
  * error
  * disabled

- RegistrationOffer - блок предложения зарегистрироваться
  
  Atoms: 
  * LinkButton

  props: 
  * path

- Keyboard - кастомная клавиатура

  Atoms: 
  * KeyboardInput
  * KeyboardInput



### Organisms

- AutorizationForm - форма авторизации

  Molecules:
  * Header
  * FormInput
  * RegistrationOffer
  * SubmitMessage
  * LoaderWithText

  Atoms: 
  * PrevButton

- RegistrationForm - форма регистрации

  Molecules:
  * Header
  * FormInput
  * PPDBlock
  * SubmitMessage


  Atoms:
  * Loader
  * FailureLoader
  * SuccessLoader

- ConfirmationForm - форма подтверждения

  Molecules:
  * Header
  * registrationData (tel / email)
  * RegistrationOffer
  * SubmitMessage
  * Keyboard

  Atoms: 
  * Loader
  * FailureLoader
  * SuccessLoader
  * Button
  * InputField

### Templates

/* *** */

### Pages

- AutorizationPage
- RegistrationPage
- ConfirmationPage

---

## Временные затратыё

Атомы: 3 часа

Моделкулы: 5 - 6 часов

Организмы: 6 - 7 часов 

Страницы: 5 - 6 часов

