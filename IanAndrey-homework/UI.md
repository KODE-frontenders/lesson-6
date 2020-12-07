
# Атомы
   1. Иконки, как ReactComponents
      ( _Иконки 8шт разместить в папку подправить какие-то свойства, проверить что все открываются, **примерно, 20-30мин**_ )
      
      > ![](images/atoms/Subtract.png) ![](images/atoms/Vector-2.png) ![](images/atoms/Vector.png)
      

   2. Прямоугольная кнопка (GreyButton, BlueButton), например есть свойства (active, title)
      ( _Кнопки сверстать, для каждой написать свой ui, написать для них Story, потестировать **примерно, 60мин**_ )
      
      > ![](images/atoms/button-fixed-2.png)
      >
      > ![](images/atoms/button-fixed.png)
      


   3. Текст(например AppText), будет содержать свойство (text)
      ( _Попробовал бы реализовать компонент, как в react-native {Text}, затем каждый компонент, обернул в стили, + Story **навскидку, 60мин**_ )

        > ![](images/atoms/your-phone-number.png)
        > 
        > ![](images/atoms/sms-code.png) 
        > 
        > ![](images/atoms/send-verification-code.png)
        > 
        > ![](images/atoms/wrong-text.png)
        


   4. Загрузчики принимают, например, в качестве необязательного свойства текст состояния (text),
   ( _Стилизуем ellipse и в нее кладем иконку как компонент и текст? + Story, **примерно, 60мин**_ )

   4.1 Loading, LoadingWithText
   > ![](images/atoms/loading.png)
   >
   > ![](images/atoms/send-verification-code.png)

   4.2 LoaderSuccess, LoaderSuccessWithText
   > ![](images/atoms/loader%20(success).png)
   >
   > ![](images/atoms/Success.png)

   4.3 LoaderError, LoaderErrorWithText
   > ![](images/atoms/loader%20(failure).png)
   >
   > ![](images/atoms/Error.png)

   
   5. Ссылка (Назад, Зарегистрируйтесь), принимает (path, children).
   ( _Стилизуем тег "a" внутрь кладем children + Story, **примерно, 60мин**_ )


   6. Checkbox
   ( _Стилизуем + Story **примерно, 60мин**_ )

   > ![](images/atoms/checkbox.png) ![](images/atoms/checkbox-error.png) ![](images/atoms/checked.png)
      

   7. Кнопка клавиатуры (KeyboardButton), принимает свойство (title)
      ( _Стилизуем + Story **примерно, 60мин**_ )
      
   > ![](images/atoms/3.png) 
   > 
   > ![](images/atoms/no-code.png)


   8. Кнопки подвала, (**_если это не меню телефона_**)
      ( _Стилизуем + Story **примерно, 60мин**_ )
      
   ### Итого: 
     Думаю с атомами управился бы за рабочий день
***    

# Молекулы

   ### 1. Из 2x атомов (ссылки и текста)
   ( _Стилизуем + Story **примерно, 30мин**_ )

   > ![](images/molecules/no_account_reg.png)
      
      
   ### 2. Уведомления
   ( _Стилизуем + Story **примерно, 30-40мин**_ )

   Принимают в качестве свойства текст сообщения (text) 

   2.1 ErrorNotification
   > ![](images/molecules/notification.png)

   2.2 SuccessNotification
   > ![](images/molecules/notification-2.png)
 
   
   ### 3 Поле ввода
  ( _Стилизуем + Story **примерно, 60-120мин**_ )

   Например:
   > ![](images/molecules/input.png)  

   > ![](images/molecules/telephone.png)

   > ![](images/molecules/telephone-2.png)
    
   > ![](images/molecules/telephone-3.png)
 
   > ![](images/molecules/code.png)


   ### 4 Соглашение
   ( _Стилизуем + Story **примерно, 30мин**_ )
   > ![](images/molecules/agreements.png)
 

   ### 5 Клавиатура
   ( _Стилизуем + Story **примерно, 60мин**_ )
   > ![](images/molecules/keyboard.png)

   ### 6 Заголовок
   ( _Стилизуем + Story **примерно, 30мин**_ )
   Принимает свойства (children?, path)   

   > ![](images/atoms/icon-back.png)  ![](images/atoms/Title.png)


### Итого:
     Думаю с молекулами управился бы за рабочий день,
***

# Организмы
   
   ### Форма входа
   ( _Стилизуем + Story **примерно, 60мин**_ )
   > > ![](images/molecules/telephone-3.png)
   > >
   > > ![](images/atoms/button-fixed.png)
   > >
   > или
   > > ![](images/molecules/telephone.png)
   > >
   > > ![](images/atoms/button-fixed.png)
   
   
   ### Форма регистрации
   ( _Стилизуем + Story **примерно, 60мин**_ )
   > > ![](images/molecules/telephone-2.png)
   > > 
   > > ![](images/atoms/loading.png)
   > >
   > > ![](images/molecules/agreements.png)
   > >
   > > ![](images/atoms/button-fixed-3.png)
   
   
   ### Форма подтверждения
   ( _Стилизуем + Story **примерно, 60мин**_ )
   > > ![](images/molecules/code.png)
   > >
   > > ![](images/molecules/keyboard.png)
   
   
   ### Подвал
   ( _Стилизуем + Story **примерно, 60мин**_ )
   _Возможно это меню телефона_
   > ![](images/organisms/footer.png)

### Итого:
     Думаю с организмами управился бы за 4 часа


***
# Шаблоны
   
   ### Header
   Например, на уровне шаблона регулируем текст заголовка
   * Ссылка назад
   * Текст заголовка

   ### Body
   * Форма ввода
   * Загрузчик

   ### Footer
   * Кнопки
      * Вперед
      * Назад
      * Увеличить
      * Переключение
      * Меню

   ### Page
   * Заголовок
   * Тело
   * Подвал

### Итого: 
     На шаблоны думаю затратить пару часов
***

# Страницы
   ### 1. Входа

   ### 2. Регистрации

   ### 3. Подтверждения входа

### Итого:
     На страницы думаю заратить пару часов

***
# Мысли в слух
     Оценить время выполнения мне довольно не просто. Бывает, что работа идет быстро, 
     а порой могу зависнуть на чем-нибудь казалось бы простом. 
     Итого за 3 дня, думвю, сверстал бы это приложение, без логики взаимодействия
        
      
    
    