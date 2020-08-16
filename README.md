So Shivam had just learned about OOP. He had written a program before that did two things,
- Find distance between two points
- Find direction (angle) between two points in Radians.

He has this code in the `org.procedural.DistanceAndDirectionCalculator` It looks like this for the reference - 

```java
public class DistanceAndDirectionCalculator {
    public static double distance(double x1, double y1, double x2, double y2) {
        double xDistance = x1 - x2;
        double yDistance = y1 - y2;
        return Math.sqrt(Math.pow(xDistance, 2) + Math.pow(yDistance, 2));
    }

    public static double direction(double x1, double y1, double x2, double y2) {
        double xDistance = x2 - x1;
        double yDistance = y2 - y1;
        return Math.atan2(yDistance, xDistance);
    }
}
```
He thought it'll be a good idea to convert this to Object Oriented Programming. So he wrote a new implementation in package `org.oop`, he got 2 classes - 
- `org.oop.DistanceAndDirectionCalculator`
- `org.oop.Point`

However, his trainer told him that what he did is not Object Oriented programming and asked Shivam to try again. 
- Try to articulate problems with Shivam's OOP solution. (Write it somewhere and share it with your trainer)
- Fork the project and fix the design related problem with Shivam's OOP solution. Share that with your trainer too.

**Articulation**
- The first thing came to my mind when I saw the `Point` class was the redundant setters.
- The second thing was that `Point` class had only state and no behaviour.
- The `DistanceAndDirectionCalculator` was having only the methods which acts like a helper class.
- And finally there was no need for `DistanceAndDirectionCalculator` class since the `Point` class itself can be encapsulated with the necessary behaviours, i.e calculate distance and direction.

**Modifications**
- The `DistanceAndDirectionCalculator` class has been removed.
- The `Point` class is updated with the methods(behaviours).
- The setters were removed.
- The test cases were updated accordingly.
