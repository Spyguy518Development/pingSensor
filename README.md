pingSensor
==========

Arduino ping sensor support class


## Hardware Requirements
* SR-04 Ping))) Sensor

## Installation
Copy the pingSensor library directory to the `<SKETCHBOOK>/libraries/` directory.

## Usage
The pingSensor library is very easy to use.

1. Import the library:
```cpp
#include <pingSensor.h>
```

2. Create an object:
```cpp
// trigger pin, echo pin
pingSensor *mySensor = new pingSensor( TRIGGER_PIN, ECHO_PIN );
```
or
```cpp
// trigger pin, echo pin, max ping distance
pingSensor *mySensor = new pingSensor( TRIGGER_PIN, ECHO_PIN, 200 );
```
or
```cpp
// trigger pin, echo pin, max ping distance, conversion method (CONV_CM | CONV_INCHES)
pingSensor *mySensor = new pingSensor( TRIGGER_PIN, ECHO_PIN, 200, CONV_INCHES );
```

3. Get Ping))) results:
```cpp
mySensor->doPing();
```

4. Check range:
```cpp
if( mySensor->checkRange() == true ) {
  // Sensor is in range, so do stuff.
}
```

5. If you need the actual distance travelled.
```cpp
// Returns a value in units specified with conversion method.
long distTraveled = mySensor->getDistance();
```

## License
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## About The Author
Kotori is a hobbist programmer/circuit builder.

## Website
GitHub Page (http://github.com/kotori)

GitHub (https://github.com/kotori/pingSensor)
