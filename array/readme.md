# Array in Datastructure
An array is a collection of items stored at **contiguous memory locations**. The idea is to store multiple items of the same type together. This makes it easier to calculate the position of each element by simply adding an offset to a **base value, i.e., the memory location of the first element**

## Summary
* Contiguous memory locaion
* Base value - the momory location of the first element
* Random access
* Search Complexity O(n), insertion and deletion complexity O(1)

## Array Comparison - equals(), deepEquals()

**equals() method**

```
// ==, equals(), deepEquals()
int[] array1 = {1,2,3};
int[] array2 = {1,2,3};
boolean isEqual = array1  == array2;  //false
isEqual = array1.equals(array2);      //true

Object[] newArray1 = {array1};
Object[] newArray2 = {array2};

isEqual = newArray1 == newArray2; //false
isEqual = newArray1.equals(newArray2); //false
isEqual = Arrays.deepEquals(newArray1, newArray2); //true


// DeepEquals Method in java
  public static boolean deepEquals(Object[] a1, Object[] a2) {
        if (a1 == a2)
            return true;
        if (a1 == null || a2==null)
            return false;
        int length = a1.length;
        if (a2.length != length)
            return false;

        for (int i = 0; i < length; i++) {
            Object e1 = a1[i];
            Object e2 = a2[i];

            if (e1 == e2)
                continue;
            if (e1 == null)
                return false;

            // Figure out whether the two elements are equal
            boolean eq = deepEquals0(e1, e2);

            if (!eq)
                return false;
        }
        return true;
    }
```

## Arrays in Java
* Clonable
* Linear Array - One dimentional array
* Two dimentional array - matrix
* Multidimentional Array
* ArrayIndexOutOfBoundsException
## Cloning of Arrays
* one dimentional array - clone - deep copy
* multidimentional array - clone - shallow copy

