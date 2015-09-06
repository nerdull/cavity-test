# Usage
``` bash
sh deploy.sh
java -jar StaticTest.jar
```

# Outcome
A file named `slow_control.dat` and several files named with nominal numbers starting from zero are to be generated by the application.
The `slow_control.dat` contains the present settings of the instruments and the ambient temperatures during the test.
Each numbered file contains the trace points of the s-parameter in the complex format, denoted by a real and an imaginary part.

# Notice
- It is user's duty to pass the appropriate center frequency and span to the Java application as command-line arguments.
  For more information, run `java -jar StaticTest.jar -h`.
- More importantly, the VNA should be calibrated prior to any test.
  The calibration file ought to be saved to the local disk of the VNA, and the calibration filename in `VectorNetworkAnalyser.java` ought to be overridden by the new one.