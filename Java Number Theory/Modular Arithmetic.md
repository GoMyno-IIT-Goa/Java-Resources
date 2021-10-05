<<!-- Author : Rohith-->>

## Modular Arithmetic

Modular arithmetic is a technique for solving problems that involve arithmetic on numbers that are not necessarily in the range of a normal integer.
Quite often, the numbers involved are very large, and the arithmetic is done modulo a large number.

```java

//Modular Arithmatic functions
	int modular_addition(int a, int b, int mod)
	{
	    int result = ((a%mod) + (b%mod)) % mod;
	    return result;
	}
	
	int modular_subtraction(int a, int b, int mod)
	{
	    int result = ((a%mod) - (b%mod) + mod) % mod;
	    return result;
	}
	
	int modular_multiplication(int a, int b, int mod)
	{
	    int result = (int)((long)(a%mod)  * (b%mod)) % mod;
	    //Here first we convert it to long to avoid overflow and then again to int 
	    return result;
	}
	
	int modular_division(int a, int b, int mod)
	{
	    int result = (int) ((a%mod) *(Math.pow(b, mod-2)%mod) % mod);    
	    /* You can also compute b^(mod-2) using Binary exponentation a*b^(mod-2) % mod */
	    return result;
	}
//If you are calling these functions inside the main method then make all these functions static since the main method is by default static and a non-static method can't be called inside a static method.

```
