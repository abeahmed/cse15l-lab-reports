# Lab Report 2: 

## Part 1. **String Server**: ##

This server keeps track of a string that is added onto by incoming requests. The code for it is shown below:	

    import java.io.IOException;
    import java.net.URI;

    class Handler implements URLHandler {
        String outputString = "";
        String firstParameter;
        String secondParameter;
        public String handleRequest(URI url) {
            if (url.getPath().contains("/add-message")) {
                String[] URLparameters = url.getQuery().split("=");
                firstParameter = URLparameters[0];
                secondParameter = URLparameters[1];
                if (firstParameter.equals("s")) {
                    outputString = outputString + secondParameter + "\n";
                }
                return outputString;
            }
            return "invalid";
        }
    }


    class StringServer {
        public static void main(String[] args) throws IOException {
            if (args.length == 0) {
                System.out.println("Missing port number");
                return;
            }
            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }
   
Here are some screenshots of the server running on a localhost:

![Server1](Server1.png)
![Server2](Server2.png)

The methods called in the code are the *handleRequest* and *main* methods

* The argument to the __*handleRequest*__ method is the *url* variable, which is of the URI type. This, is the unparsed URL.
* The argument to the __*main* method__ is the *args* variable, which is of the String type. This is the port number, in this case.

## Part 2. **Lab 3 Bugs**: ##

     static void reverseInPlace(int[] arr) {
            for(int i = 1; i < arr.length; i += 1) {
              arr[i] = arr[arr.length - i];
            }
    }
---
This is the faulty code for the reverseInPlace method.

When the input `[3, 3, 3]` is used to test this method, it doesn't induce a failure, as shown below:

  	 @Test 
	public void testReverseInPlace() {
		int[] input1 = {3, 3, 3};
		ArrayExamples.reverseInPlace(input1);
		assertArrayEquals(new int[]{3, 3, 3}, input1);
	}

![testOuput1](JUnit2.png)

However, when another input like `[1, 2, 3, 4, 5, 6, 7, 8]` is used, for example, the test does not pass:
    
  	@Test 
        public void testReverseInPlace() {
            int[] input1 = {1, 2, 3, 4, 5, 6, 7, 8};
            ArrayExamples.reverseInPlace(input1);
            assertArrayEquals(new int[]{8, 7, 6, 5, 4, 3, 2, 1}, input1);
        }



![testOutput2](JUnit.png)

This is because this method does not correctly reverse the input array, and ends up only working for half of the array

To fix this, we would need to properly swap the elements from the beginning and end of the array, by using a temporary variable to store overwritten contents, as shown in the fix below:

__Before__:

	static void reverseInPlace(int[] arr) {
	    for(int i = 1; i < arr.length; i += 1) {
	      arr[i] = arr[arr.length - i];
	    }
	}
	
__After__:

	static void reverseInPlace(int[] arr) {
	    for(int i = 0; i < arr.length / 2; i += 1) {
		int temp = arr[i];
		arr[i] = arr[arr.length - 1 - i];
		arr[arr.length - 1 - i] = temp;
            }
	}

## Part 3. **What I learned**: ##

