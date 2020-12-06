## Вопросы

Будут ли в приложении на других экранах использоваться:

- Checkbox;
- SmsKeyboard;
- KeyboardNumbers;
- Note, NoteLink;
- SmsInput?

На экране 3.6 экран 1.0 со статусом ошибки?  
На экране 2.7 экран 1.5 со статусом успеха? (видимо да, если вместо 2.7 написано 1.5😊)  
Ошибка как на экране 1.3 и других экранах свайпается или исчезает сама?  
Условия и согласие в флоу регистрации открываются в отдельном окне?

---

## Декомпозиция

### Пример:

##### Flow:

    AtomicLvl:
        ComponentWithComponent2 (Component, Component2) <Time in minutes>

---

##### Login

    Atoms:
        Note <5>
        NoteButton <5>
    Molecules:
        SignOutQuestion (Note, NoteButton) <3>
    Organisms:
        LoginForm (PhoneInput, ButtonBig) <10>
    Pages:
        LoginPage (PageTemplate, LoginForm, SignOutQuestion/LoaderWithStatus, LoginStatus?) <20>

---

##### Registration

    Molecules:
        CheckboxConfirm (Checkbox, <label>) <5>
    Organisms:
        ButtonWithConfirm (CheckboxConfirm, ButtonBig) <5>
    Pages:
        RegistrationPage (PageTemplate, PhoneInput, Loader?, LoginStatus?) <20>

---

##### Sms

    Atoms:
        SmsInputItem <10>
        KeyboardSingleNumber <5>
        RemoveNumberButton <5>
        ResendSmsButton <5>
        Information <5>
    Molecules:
        SmsInput (SmsInputItem x4) <5>
        Keyboard (KeyboardSingleNumber x10, ResendSmsButton, RemoveNumberButton) <10>
    Organisms:
        SmsKeyboard (SmsInput/Loader, Keyboard) <15>
    Pages:
        SmsPage (PageTemplate, Information, SmsKeyboard, LoginStatus?) <15>

---

##### Shared

    Atoms:
        HeadingText <5>
        Checkbox <15>
        Loader <15>
        UserSvg <5>
        ButtonBig <5>
        ButtonArrowLeft <5>
        Input <15>
    Molecules:
        PhoneInput (Input, <html>) <20>
        Header (ButtonArrowLeft, HeadingText) <5>
        LoaderWithStatus (Loader, <html>) <10>
    Templates:
        PageTemplate (Header, <html>) <10>
        LoginStatus (UserSvg, <html>) <10>
