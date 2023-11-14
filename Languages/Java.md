## Exception Handling
Exceptions (not to be confused with errors) are handled with try-catch blocks.
```java
import java.util.Scanner;
import java.util.InputMismatchException;

try {
	myInt = scnr.nextInt();
	if (myInt % 2) {
		throw new Exception("Divisible by 2");
	}
	System.out.println(myInt);
}
catch (InputMismatchException e) {
	System.out.println("Error: Invalid input type");
}
catch (Exception e) {
	System.out.println(except.getMessage());
}
```
### Common unchecked exceptions:
| Exception                 | Notes                                                                                               |
| ------------------------- | --------------------------------------------------------------------------------------------------- |
| NullPointerException      | Indicates a null reference                                                                          |
| IndexOutOfBoundsException | Indicates that an index is outside appropriate range                                                |
| ArithmeticException       | Indicates occurrence of exceptional arithmetic condition (div 0)                                    |
| IOError                   | Failure of an I/O operation                                                                         |
| ClassCastException        | Invalid attempt to cast an object to type of which the object is not an instance (Double to String) |
| IllegalArgumentException  | Illegal or inappropriate method argument                                                                                                    |

