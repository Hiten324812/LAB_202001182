# NAME - HITEN MISTRY
# ID - 202001182 

## LAB - 8  Unit Testing with JUnit

### 1.   Create a new Eclipse project, and within the project create a package and defining class in given lab exercise pdf.
### 2.   Create a class for a Boa.
![image](https://user-images.githubusercontent.com/107188205/233314152-593c110d-2b7e-4d27-ae70-4c5ea057cb9b.png)

### 3.   Follow the instructions in the JUnit tutorial in the section “Creating a JUnit Test Case in Eclipse”.
![image](https://user-images.githubusercontent.com/107188205/233318978-bfb02955-23be-4e63-8727-35b915385791.png)

### 4.   Modify the setUp() method so that it creates a couple of Boa objects, as follows:

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

### 5.  testIsHealthy() method in the BoaTest class :

    public void testIsHealthy() {
		 // check that jen is not healthy
	       assertFalse(jen.isHealthy());
	    
	    // check that ken is healthy
	    assertTrue(ken.isHealthy());
	}



   ### testFitsInCage() method in the BoaTest class :
   
  
	@Test
	 public void testFitsInCage() {
	     // Test when cage length is less than boa length
	     assertFalse(jen.fitsInCage(1));
	     assertFalse(ken.fitsInCage(2));

	     // Test when cage length is equal to boa length
	     assertTrue(jen.fitsInCage(2));
	     assertTrue(ken.fitsInCage(3));

	     // Test when cage length is greater than boa length
	     assertTrue(jen.fitsInCage(3));
	     assertTrue(ken.fitsInCage(4));
	  }

### 6 Run your test cases 

![image](https://user-images.githubusercontent.com/107188205/233330194-45ce005f-ff6f-4db8-9936-0c082feb63a0.png)

### Now modified code now we get green bar in Junit Pane
![image](https://user-images.githubusercontent.com/107188205/233332102-8c87bf9a-7f1b-4b49-b64b-72e149fe66c9.png)


### 7 Add a new method to the Boa class, with this purpose and signature:


	public class Boa {
		private String name;
		private int length; // the length of the boa, in feet
		private String favoriteFood;
		public Boa (String name, int length, String favoriteFood){
		this.name = name;
		this.length = length;
		this.favoriteFood = favoriteFood;
		}
		// returns true if this boa constrictor is healthy
		public boolean isHealthy(){
		return this.favoriteFood.equals("granola bars");
		}
		// returns true if the length of this boa constrictor is
		// less than the given cage length
		public boolean fitsInCage(int cageLength){
		return this.length < cageLength;
		}

		  public int lengthInInches() {
			return this.length * 12;
		    }
	}

### 8 
![image](https://user-images.githubusercontent.com/107188205/233333844-08831db5-c439-49e0-94e5-1192c1e89816.png)




