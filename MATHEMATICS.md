# Mathematics
Learning resources and tools for the mathematics of audio DSP.

DSP (Digital Signal Processing) is the study of using a digital computer to process what is normally thought of as an analogue signal (such as sound). Unfortunately (or fortunately depending on who you are 😉), the reality is that DSP is quite a math heavy field. However, the math needed to get started is not *too* difficult in my opinion. Knowing high-school level math and some of the basics of college-level math will get you most of the way there.

## Prerequisites
I recommend knowing at least these fundamental concepts in order best get started with learning DSP:
- Algebra dealing with polynomials, fractions, and exponents (exponents are especially important here)
- Basic trigonometry like sine, cosine, tangent, arctangent, etc.
- Logarithms (especially the natural logarithm and the number "e")
- Complex (imaginary) numbers & complex algebra (using algebra with complex numbers). (Yes, imaginary numbers do actually have a real-world use and are a core pillar of DSP mathematics.)
- Basic knowledge of linear algebra (the study of transforming data with matrices). (You *can* get by without this, but this is really helpful when it comes to actually implementing the mathematics into code.)
- Basic knowledge of calculus such as derivatives and integrals. (You *can* get by without this, but it will really help you to understand why things are the way they are.)
  - In the topic of calculus, basic knowledge of what differential equations are why there are important will also help (although I'm not talking about how to actually *solve* differential equations, because they are "really freakin' hard to solve" to put it lightly)

## Learning Resources

- [`3Blue1Brown`] - An excellent YouTube channel on complex algebra, linear algebra, calculus, and differential equations.
  - His videos on [`Euler's Formula`] and the [`Fourier Transform`] are particularly excellent.
- [`Paul's Online Math Notes`] - Excellent resources written and used by a professor at Lamar University.
- [`Paul's Cheat Sheets`] - Cheat sheets for many common identities and formulas in algebra, trig, calculus, and laplace transformations. Because who can remeber all this stuff?
- [`katjaas`] - Neat visual explanations of DSP mathematics and techniques.
- This video on the [`Laplace Transform`] by Zach Star.
- [`Khan Academy`] - Free college-level courses.

## Tools
- [`Desmos`] - Free online graphing calculator.
- [`Wolfram Alpha`] - A helpful math partner.
- [`Symbolab`] - Another helpful math partner.
- [`GNU Octave`] - An open-source alternative to MATLAB. There is also an [`online version of GNU Octave`] available.
  - [`Signal package`] - Signal processing tools for [`GNU Octave`], including filtering, windowing and display functions.
- [`Curcuit JS`] - A cool little circuit simulation tool.
- [`Russell`] - A collection of tools that assist in the development of scientific computations (and by extension audio DSP). It includes numerical methods and solvers for differential equations, tools for statistical analysis, and other linear algebra tools. It is written in the [`Rust`] programming lanugage.

[`3Blue1Brown`]: https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw
[`Euler's Formula`]: https://www.youtube.com/watch?v=mvmuCPvRoWQ
[`Fourier Transform`]: https://www.youtube.com/watch?v=spUNpyF58BY
[`Paul's Online Math Notes`]: https://tutorial.math.lamar.edu/
[`Paul's Cheat Sheets`]: https://tutorial.math.lamar.edu/Extras/CheatSheets_Tables.aspx
[`katjaas`]: http://www.katjaas.nl/home/home.html
[`Laplace Transform`]: https://www.youtube.com/watch?v=n2y7n6jw5d0
[`Khan Academy`]: https://www.khanacademy.org/math
[`Desmos`]: https://www.desmos.com/calculator
[`Wolfram Alpha`]: https://www.wolframalpha.com/
[`Symbolab`]: https://www.symbolab.com/
[`GNU Octave`]: https://www.gnu.org/software/octave/index
[`online version of GNU Octave`]: https://octave-online.net/
[`Signal package`]: https://octave.sourceforge.io/signal/index.html
[`Curcuit JS`]: https://www.falstad.com/circuit/circuitjs.html
[`Russell`]: https://github.com/cpmech/russell
[`Rust`]: https://www.rust-lang.org/