# OOP_CS_2022 :triangular_ruler:

## [Class](#create-class)





 ---
 ### Create Class
 ```js
 class Valid {
    constructor(email, password, isValid) {
        this.email = email
        this.password = password
        this.isValid = isValid
    }
    validate() {
        if (`${(this.password).length}` >= 6) {
            this.isValid = true
            console.log('isValid = ' + this.isValid);
        } else {
            console.log('isValid = ' + this.isValid);
        }
    }
}
```

---
### Class Extends
```js
class Valid2 extends Valid {
    constructor(email, password, isValid, emailError = '', passwordError = '') {
        super(email, password, isValid)
        this.emailError = emailError
        this.passwordError = passwordError
    }
    // Метод переопределяется если такое же имя в родительском классе
    validate() {
        if (this.password.length >= 6 && this.email) {
            this.isValid = true
            console.log('isValid = ' + this.isValid);
        }

        if (this.password.length < 6) {
            this.isValid = false
            this.passwordError = 'min length 6'
            console.log('isValid = ' + this.isValid);
            console.log('Password Error: ' + this.passwordError);
        }
        if (!this.email) {
            this.emailError = 'emailEmpty'
            console.log('Email Error: ' + this.emailError);
        }
    }
}
```

---
### Instance of Class
```js
let valid6 = new Valid2('qwe@mail.yy', '12345678')

// Class method
valid6.validate()
```

