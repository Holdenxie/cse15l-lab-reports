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

