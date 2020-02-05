# Changes Required for incorporating test
    (1) added "alarm-mega" to the tests[] array and associated it with a 'test_alarm_mega' function (tests.c)
    (2) declared the 'test_alarm_mega' function on a global scope (tests.h)
    (3) implemented the 'test_alarm_mega' function (alarm-wait.c)
        - copied the 'test_sleep' statement from the 'test_alarm_multiple' function
        - but changed the second parameter from 7 -> 70

# CODE CHANGES
    extern test_func test_alarm_mega; // tests.h
    {"alarm-mega", test_alarm_mega}, // tests.c
    void test_alarm_mega (void) { test_sleep (5, 70); } // alarm-wait.c

Jake Willson (1/26/2020)