# Usage
``` bash
sh deploy.sh
java -jar DynamicTest.jar
```

# Outcome
A file named `slow_control.dat` and several files, which are named with an indicator and two sets of nominal numbers starting from zero, are to be generated by the application.
The `slow_control.dat` contains the present settings of the instruments and the ambient temperatures during the test.
Each numbered file contains the trace points of the s-parameter in the complex format, denoted by a real and an imaginary part.
The reference files begin with `0`, whilst the perturbation files begin with `1`.

# Notice
- It is user's duty to pass the appropriate center frequency and span, as well as profiling range and spacing to the Java application as command-line arguments.
  For more information, run `java -jar DynamicTest.jar -h`.
- More importantly, the VNA should be calibrated prior to any test.
  The calibration file ought to be saved to the local disk of the VNA, and the calibration filename in `VectorNetworkAnalyser.java` ought to be overridden by the new one.
