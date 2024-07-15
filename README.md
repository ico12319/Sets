You need to create a tree-like structure of sets(using composite design pattern). It consists of the following classes:
1. Set - a basic abstract class representing a set. It has a pure virtual function bool isNumberIncluded(unsigned int) which will determine whether a given element is in the set or not.
2. SetByCriteria<T> - a templated derivative of Set, which holds an object of template type T. For this object, a pointer to a function or an object behaving like a function will be provided. The composed object will be given in the constructor (it must be able to be accepted by copying or moving). The isNumberIncluded() function returns the result of calling the operator() of the T object on the given input number.
3. UnionOfSets - a derivative of SetOperation, which in its constructor accepts an array of pointers to other sets and stores them (by copying or moving). It overrides the isNumberIncluded() function, calling it on the elements it holds, and the result is a conjunction of the results.
4. IntersectionOfSets - a derivative of SetOperation, which in its constructor accepts an array of pointers to other sets and stores them (by copying or moving). It overrides the isNumberIncluded() function, calling it on the elements it holds, and the result is a disjunction of the results.
Tasks:
1. Craft a set that contains all even positive numbers.
2. Craft a set that contains only the elements that are contained in the binary file included.dat
3. Craft a set that contains all positive numbers except those contained in the binary file excluded.dat
4. Craft an Intersection set containing all numbers contained in all previously crafted sets.





