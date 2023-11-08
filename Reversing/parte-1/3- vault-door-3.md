#### Description

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java)

---

#### Solución
Modificamos el codigo de la siguiente manera:
```java
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        System.out.print("Enter vault password: ");
        String userInput = "picoCTF{jU5t_a_sna_3lpm18g947_u_4_m9r54f}";
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
        }
    }
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
            
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
            
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
            
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
            
        }
        String s = new String(buffer);
        System.out.println(s);
        return true;
        //return s.equals("jU5t_a_sna_3lpm18g947_u_4_m9r54f");
    }
}
```

Bandera: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}