# **Haolin's Xie Lab Report3**
## Bug with failure-inducing input 
````Java
  @Test
  public void testReversedWithMultiple(){
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input1));
  }
````

## Bug without failure-inducing input
````Java
  @Test public void testReversedWithEmpty(){
    int[] input1 = {};
    assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1));
  }
````
## Symtomps of the outputs
![Image](Image3.1.png)

## Bug before the fix 
```Java
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
````

## After the fix 
````Java
 static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
````

