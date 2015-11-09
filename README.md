# Converter

See the live demo [here](http://sebpearce.com/converter/).

A JavaScript training exercise.

I wanted to see if I could make a number converter that converts between binary, hex, ASCII and so on that is modular, meaning that you can add your own formats/conversion functions.

Because of this, the HTML is all generated in JS.

A sample converter module looks like this:

    {
      name: 'Hexadecimal',
      type: 'hex',
      base: 16,
      convert: function (n) { return '0x' + (+n).toString(16).toUpperCase(); },
      convertToDec: function (n) { return parseInt(n, 16); },
    }
    
`name`: The label you see on the page  
`type`: The shorthand used to refer to the module within the script  
`base`: the base for this notation (if applicable; if not, leave blank)  
`convert`: a function that takes a decimal number (`string` or `int` OK) and returns it in the target notation  
`convertToDec`: a function that takes a number in the target notation and returns it as decimal (`int`)
