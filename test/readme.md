# Test filer

* Makefile
  * Makefile til CocoTB
* tb.v
  * Testbench til Tiny tape out, den instantierer tiny tapeout toplevel, og mapper til testporte. Den producerer også en vcd fil til GTKwave viewer
* Variable_PWM_tb.v
  * Testbench til Variable_PWM.v, der bruges sammen med iverilog og GTKWave
* Test.py
   * Testbench der bruges med cocoTB, anvender tb.v
