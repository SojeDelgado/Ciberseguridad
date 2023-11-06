This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/ff2585f7afd21b81f69d2fbe37c081ae/VaultDoor1.java)

#### Solución
Modifique el metodo de la siguiente manera:
```java
public String generatePassword() {
        char[] passwordChars = new char[32];
        passwordChars[0] = 'd';
        passwordChars[29] = '9';
        passwordChars[4] = 'r';
        passwordChars[2] = '5';
        passwordChars[23] = 'r';
        passwordChars[3] = 'c';
        passwordChars[17] = '4';
        passwordChars[1] = '3';
        passwordChars[7] = 'b';
        passwordChars[10] = '_';
        passwordChars[5] = '4';
        passwordChars[9] = '3';
        passwordChars[11] = 't';
        passwordChars[15] = 'c';
        passwordChars[8] = 'l';
        passwordChars[12] = 'H';
        passwordChars[20] = 'c';
        passwordChars[14] = '_';
        passwordChars[6] = 'm';
        passwordChars[24] = '5';
        passwordChars[18] = 'r';
        passwordChars[13] = '3';
        passwordChars[19] = '4';
        passwordChars[21] = 'T';
        passwordChars[16] = 'H';
        passwordChars[27] = '5';
        passwordChars[30] = '2';
        passwordChars[25] = '_';
        passwordChars[22] = '3';
        passwordChars[28] = '0';
        passwordChars[26] = '7';
        passwordChars[31] = 'e';

        return new String(passwordChars);
    }
```

Al imprimir la contraseña:
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_75092e}
