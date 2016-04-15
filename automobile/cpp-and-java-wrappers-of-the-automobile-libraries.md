## C++ and Java wrappers of the automobile libraries

The [driver](driver-library.md) and [car](car-library.md) libraries are also
available as oriented-object wrappers for the C++ and the Java languages.

The [Driver](cpp-libraries.md#cppdriver) and [Car](cpp-libraries.md#cppcar))
classes are containing all the methods described in the C API. Camel case is
used to define the method names. The `init` and `cleanup` functions are called
automatically from the constructor/destructor of the
[Driver](cpp-libraries.md#cppdriver) and [Car](cpp-libraries.md#cppcar) classes.

> **note** [Java]:
The following program shows how to set the cruising speed and the steering angle
in Java:

>
>     import com.cyberbotics.webots.controller.Robot;
>     import com.cyberbotics.webots.automobile.Driver;
>
>     public class VehicleDriver {
>      public static void main(String[] args) {
>        Driver driver = new Driver();
>        driver.setCruisingSpeed(20.0);
>
>        while (driver.step() != -1) {
>          double angle = 0.3 * Math.cos(driver.getTime());
>          driver.setSteeringAngle(angle);
>        };
>      }
>     }
