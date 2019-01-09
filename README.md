
Veriwell 3
==========

Veriwell is a Verilog simulator. It is compliant to Verilog-95, but does not
fully support it.

This package also integrates support for dumping lxt waveform files. These files
can be used with the gtkwaves waveform viewer.

[Veriwell 3](https://github.com/balanx/veriwell) is forked from
[Veriwell](http://sourceforge.net/projects/veriwell) and adds some Verilog-2001
features and fixes some bugs (see change log below).

Installation
------------

Pre-compiled binaries for can be found on the following Github Releases Page:

https://github.com/niosHD/veriwell/releases

Alternatively, Veriwell can be compiled using the following commands:

    $ git clone https://github.com/niosHD/veriwell.git
    $ cd veriwell
    $ ./configure --prefix=$(pwd)/install
    $ make install

Usage
-----
It's very similar to Verilog-XL, so it will be very friendly if you are a long-term experienced IC engineer.
Try the following in the DOS command window.

    $ veriwell
    $ veriwell  a.v  b.v  c.v
    $ veriwell  tb.v  +libext+.v  -y dir1  -y dir2
    $ veriwell  -f  sim.f

Change Log
----------
2015-10-30 :

- add : Power (**) operator
- add : generate-if
- add : generate-case
- mod : disable specify-block
- add : bit-select for 2-dimensional array
- fix : task enable
- fix : searching top module
- add : non-declared wire
- fix : multi-modules in one file
- add : permit variable in 'delay control'
- add : permit function reference in parameter declaration
- add : $fscanf(), $sscanf()
- add : block-declaration in module

2014-10-9 :

- add : port definition in Verilog-2001
- add : named parameter
- add : parameter declaration before port definition
- add : part-select operator '+:' and '-:'
- add : sensitive list wildcard
- add : `ifndef support
- add : reg initialization like 'reg a = 0, b = 0;'
- add : (* synthesis comments *) support
- fix : '-y' option
