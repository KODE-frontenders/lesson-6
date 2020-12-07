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
10. Почему у SignIn нет заголовка.

### Разбивка UI на атомарные компонентики:

#### Atoms
1. Loaders(LoaderLoading, LoaderFailure, LoaderSuccess)
2. Btn
3. Input (Номер телефона или email)
4. Checkbox
5. confirm-DigitDiv
6. confirm-DigitBtn
7. confirm-DelBtn
#### Moleculs
1. signin-InputCorrect = input + label
2. signin-InputIncorrect = input + 2labels
3. Allert = icon + span
4. signin-RegistrationLink = span + link
5. signin-LoadingRequest = LoaderLoading + span
6. signin-LoadingFailure = LoaderFailure + span
7. signin-LoadingSuccess = LoaderSuccess + span
8. signup-Agreements = Checkbox + p + span + btn
9. signup-RegistrationInput = input + span
10. signup-RegistrationInputWithPhone = span + input + span
11. confirm-Blocks = 4 div
12. confirm-DigitalsSms = 10DigitBtn + DelBtn + SmsBtn
13. confirm-DigitalsPost = 10DigitBtn + DelBtn + PostBtn
#### Organisms
1. signin-SignInForm = input + btn
2. signup-SignUpForm = RegistrationInput + Agreements
#### Templates
1. Header 
2. Body
3. confirm-SmsOrEmailBody(text1/text2 + Blocks + DigitalsSms/DigitalsPost)
#### Pages
1. SignIn
2. SignUp
3. Confirm