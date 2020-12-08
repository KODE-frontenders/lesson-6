## Домашнее задание

### Вопросы:

1. Как будет происходить валидация при потере фокуса в странице SignIn, на основе каких данных? Нужна ли она вообще при потере фокуса, если в инпуте емайл или телефон? Лучше сделать валидацию при регистрации на телефон(там она отсутствует).
2. На экране 1.6, после появления ошибки, нужно ли мне ставить фокус на инпут или пользователь сам на него нажмет?
3. Слева есть векторная стрелочка. Несет ли она в себе какой-то смысл?
4. Во вкладке components компоненты bottom и top это дефолтный низ и верх мобильных браузеров?
5. Экран 3.4, что должно происходить дальше?
6. Экраны 3.2, 3.3 подсвечивается цифра 7, почему?
7. Какой функционал у кнопки "Не пришло письмо" из подтверждения?
8. На макетах везде одинаковое доменное имя. Маршрутизацию не придумывать?
9. В макетах с подтверждения нужно делать инпуты или просто по нажатию на цифру, она должна появляться над полоской?
10. Почему в signup отступ до инпута в обычном состоянии меньше, чем когда есть алерт(всплывающая подсказка). Я думаю, лучше сделать всплывающую подсказку fixed.
### Разбивка UI на атомарные компонентики:

#### Atoms
1. Loaders(LoaderLoading, LoaderFailure, LoaderSuccess) - 20 мин
2. Btn - 5 мин
3. Input (Номер телефона или email) - 20 мин
4. Checkbox - 30 мин
5. confirm-DigitDiv(цифра над полоской) - 7 мин
6. confirm-DigitBtn - 30 мин
7. confirm-DelBtn - 10 мин
#### Moleculs
1. signin-InputCorrect = input + label 20 мин
2. signin-InputIncorrect = input + 2labels 20 мин
3. Allert = icon + span 30 мин
4. signin-RegistrationLink = span + link 10 мин
5. signin-LoadingRequest = LoaderLoading + span 9 мин
6. signin-LoadingFailure = LoaderFailure + span 7 мин
7. signin-LoadingSuccess = LoaderSuccess + span 7 мин
8. signup-Agreements = Checkbox + p + span + btn 25 мин
9. signup-RegistrationInput = input + 2span 15 мин
11. confirm-Blocks = 4 DigitBtn 20 мин
#### Organisms
1. signin-SignInForm = input + btn 30 мин
2. signup-SignUpForm = RegistrationInput + Agreements 1 ч.
3. confirm-DigitalsSms = 10DigitBtn + DelBtn + SmsBtn 2 ч.
4. confirm-DigitalsPost = 10DigitBtn + DelBtn + PostBtn 15 мин
#### Templates
1. Header 20 мин
2. Body 7 мин
3. confirm-SmsOrEmailBody(text1/text2 + Blocks + DigitalsSms/DigitalsPost) 30 мин
#### Pages
1. SignIn 30 мин
2. SignUp 45 мин
3. ConfirmSms,ConfirmPost 1-2 ч