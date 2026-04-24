# Duration

`duration.h` provides precise duration calculations, accounting for various sources of error and difference between
time systems. Calculating exactly what duration has passed between two points in time is challenging, due to various 
sources of error:

- There exist several definitions of a day:
  - Sidereal days, between when the Earth rotates 360 degrees.
  - Solar days, between when the same point on Earth faces the sun (~361 degrees due to the Earth orbiting the Sun
    concurrent with its rotation).
- Earth's rotation is slightly elliptical, causing periodic variations in the length of a solar day.
- Earth's rotation has small random variations requiring irregular positive and negative leap-second corrections.
- The period of Earth's orbit around the Earth is not an integer multiple of days, requiring periodic leap-day
  corrections.
- Local time zones introduce offsets between the local solar time of different observers.
  - Daylight Savings Systems introduce further periodic offset.

`duration.h` computes precise durations between two points in time, accounting for these sources of error and
differences.