# **Haolin's Xie Lab Report3**
## bug with failure-inducing input 
````Java
  @Test
  public void testReversedWithMultiple(){
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input1));
  }
````
