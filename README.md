# Aghaas-Core
### Introduction To Our Single-Cycle Core

### Designed by Agha Muqarib
I'm in my senior year currently pursuing bachelors in software engineering at [Usman Institute of Technology, Pakistan.](https://www.uit.edu/). Being a trainee @ [Micro Electronics Research Lab](https://github.com/merledu), I've designed a parameterized RISC-V 32-bit Single Cycle Core(supporting I Type) using functional programming in Scala and Chisel.

## First of all get started by Cloning this repository in your machine
```ruby
git clone https://github.com/Agha-Muqarib/Aghaas-Core.git
```

Open  "instrFile.txt" file and place the instruction(Hexa-Decimal) code simulated on ***Venus*** (RISC-V Simulator)\
Each instruction's hexadecimal code must be on seperate line as following. The following is a sample program containing 9 instructions.
```
00500113
00500193
014000EF
00120293
00502023
00002303
00628663
00310233
00008067
```
## Then perform the following step
```ruby
cd Aghaas-Core/src/main/scala/Datapath
```
Open **Config.scala** with this command. You can also manually go into the above path and open the file in your favorite text editor.
```ruby
open Config.scala
```
Find the following line
``` python
val initFile = "Some Path to txt file"
```
Update the .txt file path to match your "instrFile.txt" that you updated above to store your own program instructions.\
After setting up the Config.scala file, go inside the ***Aghaas-Core*** folder.
```ruby
cd Aghaas-Core
```
And enter
```ruby
sbt
```
When the terminal changes to this type
```ruby
sbt:Aghaas-Core>
```
Enter this command
```ruby
sbt:Aghaas-Core> testOnly Datapath.TopFileTest -- -DwriteVcd=1
```
After you get success
```ruby
sbt:Aghaas-Core> test:runMain datapath.Launcher Top --backend-name verilator
```
After success you will get a folder naming ***test_run_dir*** on root of your folder. Go to the examples folder inside.\
There you will find the folder named Top. Enter in it and you can find the Top-File.vcd file which you visualise on **gtkwave** to\
see your program running.


