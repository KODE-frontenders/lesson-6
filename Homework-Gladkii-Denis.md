**Вопросы по реализации:**
 - Экран 1.3: При фокусе на input модальное окно ошибки убирается, и выделение текста красным отменяется? (аналогичы й вопрос для остальных экранов с ошибкой)
 - Экран 1.6: В какое состояние должен вернуться UI после нажатия на кружок с крестиком?
 - Экран 1.7: При успешном запросе вход в приложение осуществляется автоматически (с задержкой по таймеру), или же пользователь должен кликнуть на кружок с галкой?
 - Экран 2.0: При фокусе на input должно ли происходить автоматическое начальное заполнение номера или появление шаблона: "+7 () - -" ?
 - Экран 2.1: Реакция UI при вводе телефона в невалидном формате и попытке "продолжить" такая же как и на форме авторизации?
 - Экран 2.5: Состояние UI после нажатия на кружок с крестиком?
 - Экран 2.6-1.5: Запрос авторизации происходит автоматически (с задержкой по таймеру) или по клику пользователя на кружок с галкой?
 - Экран 3.0: Реакция UI при нажатии "Не пришло SMS?"/"Не пришло письмо?" ?
 - Экран 3.4: Состояние UI после нажатия на кружок с крестиком?
 - Экран 3.5: При успешном вводе OTP вход в приложение осуществляется автоматически или по нажатию на кружок с галкой?

**User Interface:**
* /features
    * /signIn
        - /atoms
        - /molecules
            - InputSignIn (ввод телефона или Email) ()
            - RegistrationLink ("Нет аккаунта? Зарегистрируйтесь")
        - /organisms
            - SignInForm
        - /pages
            - SignInPage

    * /signUp
        - /atoms
        - /molecules
            - Checkbox
            - InputSignUp (ввод телефона)
            - DataProcessingAgreement (Text + Checkbox)
        - /organisms
            - SignUpForm
        - /pages
            - SignUpPage

    * /oneTimePassword
        - /atoms
            - KeyboardDigit
            - KeyboardButtonErase
            - KeyboardButtonRepeatSending
            - InputOtpInfoTop
        - /molecules
            - InputOtp
        - /organisms
            - Keypad
            - OtpForm
        - /pages
            - OtpPage

* /shared:
    - /atoms
        - BackButton
        - LoaderSpinner
        - LoaderFailure
        - LoaderSuccess
        - LoaderInfoBottom
        - InputInfoTop
        - InputInfoBottom
    - /molecules
        - Header
        - ButtonSign (кнопка "Войти" или "Продолжить" в зависимости от входящих props: Title, onSubmit)
        - InfoModal
        - LoaderBox (Loader + Info)
    - /templates
        - ModalTemplate
        - PageTemplate (Header + Body)