How to use
Create a new TimeSpan object
From zero

    const ts = TimeSpan.zero;
    
From milliseconds

    const milliseconds = 10000; // 1 second

    // by using the constructor
    const ts1 = new TimeSpan(milliseconds);

    // or as an alternative you can use the static factory method
    const ts2 = TimeSpan.fromMilliseconds(milliseconds);
From seconds

    const seconds = 86400; // 1 day
    const ts = TimeSpan.fromSeconds(seconds);
From minutes

    const minutes = 1440; // 1 day
    const ts = TimeSpan.fromMinutes(minutes);
From hours

    const hours = 24; // 1 day
    const ts = TimeSpan.fromHours(hours);
From days

    const days = 1; // 1 day
    const ts = TimeSpan.fromDays(days);
From time with given hours, minutes and seconds

    const hours = 1;
    const minutes = 1;
    const seconds = 1;
    const ts = TimeSpan.fromTime(hours, minutes, seconds);
From time2 with given days, hours, minutes, seconds and milliseconds

    const days = 1;
    const hours = 1;
    const minutes = 1;
    const seconds = 1;
    const milliseconds = 1;
    const ts = TimeSpan.fromTime(days, hours, minutes, seconds, milliseconds);
From maximal safe integer

    const ts = TimeSpan.maxValue;
From minimal safe integer

    const ts = TimeSpan.minValue;
From minimal safe integer

    const ts = TimeSpan.minValue;
Add

    const ts1 = TimeSpan.fromDays(1);
    const ts2 = TimeSpan.fromHours(1);
    const ts = ts1.add(ts2);

    console.log(ts.days);               // 1
    console.log(ts.hours);              // 1
    console.log(ts.minutes);            // 0
    console.log(ts.seconds);            // 0
    console.log(ts.milliseconds);           // 0
Subtract

    const ts1 = TimeSpan.fromDays(1);
    const ts2 = TimeSpan.fromHours(1);
    const ts = ts1.subtract(ts2);

    console.log(ts.days);               // 0
    console.log(ts.hours);              // 23
    console.log(ts.minutes);            // 0
    console.log(ts.seconds);            // 0
    console.log(ts.milliseconds);           // 0
Getting the intervals

    const days = 1;
    const hours = 1;
    const minutes = 1;
    const seconds = 1;
    const milliseconds = 1;
    const ts = TimeSpan.fromTime2(days, hours, minutes, seconds, milliseconds);

    console.log(ts.days);               // 1
    console.log(ts.hours);              // 1
    console.log(ts.minutes);            // 1
    console.log(ts.seconds);            // 1
    console.log(ts.milliseconds);           // 1

    console.log(ts.totalDays)           // 1.0423726967592593;
    console.log(ts.totalHours)          // 25.016944722222224;
    console.log(ts.totalMinutes)            // 1501.0166833333333;
    console.log(ts.totalSeconds)            // 90061.001;
    console.log(ts.totalMilliseconds);      // 90061001;
