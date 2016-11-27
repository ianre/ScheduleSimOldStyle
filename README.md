# ScheduleSimOldStyle

If you have any questions about the project, email me or read the README

The project consists of 2 html files

    homepage.html    -    The video, the gif of the library and the instructions
    index.html       -    Everything else, ie. course selection and the schedule itself

I don't know yet what scheduleLayout does. Probably just formatting for the schedule

There is also 1 js file (all in javascript):

    indexScripts.js  -    As the name might imply, all the scripts that generate the schedule are here
                          Without the class info at the bottom, the scripts occupy about 500 lines of code

    The person that made the calendar printout moved to Texas. What you see is what you get.
    But the code is very navigable. If you look at the bottom of indexScripts.js , you can find all
    the classes and the information that makes up each of those classes.

    for example on line 727:
    Sports[i++]=({header: "spring", name: "Tennis (Boys)", hourStart: [16, 15, 16, 15, 16, 0, 0], minStart: [0, 30, 0, 30, 0, 0, 0], hourEnd: [17, 18, 17, 18, 17, 0, 0], minEnd: [15, 45, 15, 45, 15, 0, 0]});

    theres 7 ints in hours start. Those correspond to the 7 days of the week.
    So, on a typical Monday, Boy's Tennis meets from 16:00 to 17: 15
    In all likelihood, the 0 in hours start means they do not meet that day.

    This format only applies to sports. There's a different format for clubs and classes.

    Now, there's also some intentionally obfuscated parts:
    on lines 57 & 58
        clubsIn.push(Stupid[0]);
        clubsIn.push(Stupid[1]);
    That means MUN
    the function on line 134: function funcy()
    that's also for MUN


There are about 8 CCS files:

    All CSS stylesheets do is specify the font, size, color, spacing(padding), border and location of HTML information on a web page

    normalize.css   -   /**
                         * 1. Change the default font family in all browsers (opinionated).
                         * 2. Correct the line height in all browsers.
                         * 3. Prevent adjustments of font size after orientation changes in
                         *    IE on Windows Phone and in iOS.
                         */
                         more info: https://github.com/necolas/normalize.css/blob/master/README.md
    homepageStyle.css   -   takes care of smaller screens
                            "
                            Responsive web design makes your web page look good on all devices.
                            Responsive web design uses only HTML and CSS.
                            Responsive web design is not a program or a JavaScript.
                            "

    and the other 6 CCS, which do things, probably

And now, problems:

        *   The entire schedule is written on javascript, so styling is complicated.
        The last group managed to change the colors a bit.
        Ideally we would make the schedule fit in one page, and also make it look nicer.
        Or convert some of it to html to have more room for formatting

        *   It only works (well) on Chrome. If testnav can force us to use only one browser, so can we.
        HTML boilerplate focuses on compatibility a lot. If we ever decide to use their framework, It'd be easier to make every browser work.
        If we're gonna do it on our own, I think we can manage to have close to 100% compatibility
        across all platforms if we use bootstrap well.

        *   Some classes are missing.

        *   The instructions run off outside of the page on Homepage.html

        *   There are also actual coding errors that webstorm picked up. I'll try to resolve them later


"yeah.... have fun" - Emily
