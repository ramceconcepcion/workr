# workr
A web worker library aimed at making the Web Workers API easier to work with.

Disclaimer: This mini project is made with old code and is currently unmaintained.

To use it nonetheless:

Basic Workr Template:

    const myworker = Workr.basic({
        url: 'my-worker.js',
        data: null,
        success: function () { },
        error: function () { },
        beforeCreate: function () { },
        beforeTerminate: function () { }
    });

    const myworkers = Workr.multi([
        {},
        {}
    ]);

--------------------------

Prepared Workr Template:

    const myworker = Workr.prepared({
        url: 'my-worker.js',
        success: function () { },
        error: function () { },
        beforeCreate: function () { },
        beforeTerminate: function () { }
    });

    myworker.run(params);

    const myworkers = Workr.multiprepd([
        {
        url: 'my-worker.js',
        success: function () { },
        error: function () { },
        beforeCreate: function () { },
        beforeTerminate: function () { }
        },
        {}
    ]);

    myworkers[0].run(params);

-------------------------

Embedded Workr Template:

    const myworkers = Workr.embedded([
        {
            method: myFunction,
            data: [1, 2, 3],
            success: function () { },
            error: function () { },
            beforeCreate: function () { },
            beforeTerminate: function () { }
        },
        {}
    ]);

-----------------------

Prepared Embedded Workr Template:

    const myworkers = Workr.embeddedprepd([
        {
            method: myFunction,
            success: function () { },
            error: function () { },
            beforeCreate: function () { },
            beforeTerminate: function () { }
        },
        {}
    ]);

    myworkers[0].run(params);

-----------------------
