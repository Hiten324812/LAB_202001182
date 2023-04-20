# NAME - HITEN MISTRY
# ID - 202001182 

## LAB - 8  Unit Testing with JUnit

### 1.   Create a new Eclipse project, and within the project create a package and defining class in given lab exercise pdf.
### 2.   Create a class for a Boa.
![image](https://user-images.githubusercontent.com/107188205/233314152-593c110d-2b7e-4d27-ae70-4c5ea057cb9b.png)

### 3.   Follow the instructions in the JUnit tutorial in the section “Creating a JUnit Test Case in Eclipse”.
![image](https://user-images.githubusercontent.com/107188205/233318978-bfb02955-23be-4e63-8727-35b915385791.png)

### 4.   Modify the setUp() method so that it creates a couple of Boa objects, as follows:

package Boa;

import static org.junit.Assert.assertTrue;
import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.AfterAll;
import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.BeforeAll;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

import Lab8.boa;

class BoaTest {

	private Boa jen ;
	private Boa ken ;

	@BeforeEach
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}
 }

![image](https://user-images.githubusercontent.com/107188205/233321217-4c587167-a5b5-47a1-b7a4-612a3309640e.png)

