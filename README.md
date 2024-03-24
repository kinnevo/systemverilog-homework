# Collection of problems on SystemVerilog for the School of Digital Circuit Synthesis
> **Not a day without a line on Verilog**
>
> Collection of problems of increasing complexity
> 
> Yuri Panchul, 2021-2023

## Links

* [School of Digital Circuit Synthesis](https://engineer.yadro.com/chip-design-school/)
* [Lesson one: introduction to the design route and exercises with combinational logic](https://youtu.be/DFcvEO-gP0c)
  

<!-- Some markdown video embedding tricks from https://stackoverflow.com/questions/4279611/how-to-embed-a-video-into-github-readme-md -->

Lesson 1 (2023-24): Introduction to design route and combinational logic exercises.
[![](https://img.youtube.com/vi/DFcvEO-gP0c/hqdefault.jpg)](https://youtu.be/DFcvEO-gP0c)


## Installation instructions

Problems can be solved with any verilog simulator that supports SystemVerilog. And also with the free Icarus Verilog simulator, which, although it does not support the entire SystemVerilog, does support Verilog 2005 with some SystemVerilog elements sufficient to solve our problems. Icarus Verilog used with GTKWave, a timing diagram program. We won't need GTKWave for the first ten tasks, but it's worth installing along with Icarus Verilog for the future.

<p><img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/5c1/69d/934/5c169d9349c4352399b6cd962cdaa645.png">
<img src="https://habrastorage.org/r/w1560/getpro/habr/upload_files/219/8b5/8d9/2198b58d9b1daa7345c07d2770ca2763.png">
</p>

### Installation on Linux

Under Ubuntu and Simply Linux, you can install Icarus Verilog and GTKWave using the command:

`sudo apt-get install verilog gtkwave`

---
#### Note:

If you have an old version of the Linux distribution (Ubuntu), then when installing Icarus
Verilog, you will get an old version that does not support `always_comb`,
`always_ff` and many other SystemVerilog constructs. How to solve this problem:
1. **Checking iverilog version**
     ```bash
     iverilog -v
     ```

     If the iverilog version is less than 11, go to step 2.

2. **Install pre-packages**
     ```bash
     sudo apt-get install build-essential bison flex gperf readline-common libncurses5-dev nmon autoconf
     ```

3. **Download the latest version of iverilog**

    As of today (10/12/2023), the latest version of iverilog: 12.0
    Follow [link](https://sourceforge.net/projects/iverilog/files/iverilog/12.0/) and download the archive.

4. **Building iverilog**
     - Unpack the archive:
         ```bash
         tar -xzf verilog-12.0.tar.gz
         ```

     - Enter the unzipped folder:
         ```bash
         cd verilog-12.0
         ```

     - Configure iverilog:
         ```bash
         ./configure --prefix=/usr
         ```

     - Test the Icarus build
         ```bash
         make check
         ```
         As a result, several `Hello, world!` messages will appear in the terminal.

     - Install Icarus
         ```bash
         sudo make install
         ```
---

### Installation on Windows

The Windows version of Icarus Verilog can be downloaded [from this site](https://bleyer.org/icarus/)

[Video instructions for installing Icarus Verilog on Windows](https://youtu.be/5Kync4z5VOw)


[![](https://img.youtube.com/vi/5Kync4z5VOw/hqdefault.jpg)](https://www.youtube.com/watch?v=5Kync4z5VOw)

### Installation on Apple Mac

Icarus can even be installed on Apple Mac, which is unusual for EDA (Electronic Design Automation) instrumentation. This can be done in the console using brew:

`brew install icarus-verilog`

[Video instructions for installing Icarus Verilog on MacOS](https://youtu.be/jUYkYoYr8hs)


[![](https://img.youtube.com/vi/jUYkYoYr8hs/hqdefault.jpg)](https://www.youtube.com/watch?v=jUYkYoYr8hs)


## Executing and checking tasks

To check tasks under Linux and MacOS, open the console in the folder with tasks and run the script `./run_all_using_iverilog_under_linux_or_macos_brew.sh`. It will create a _log.txt_ file with the results of the compilation and simulation of all problems in the set.

To check tasks under Windows, open the console in the task folder and run the batch file `run_all_using_iverilog_under_windows.bat`. This will also create a _log.txt_ file with the test results.

After the test for all problems shows **PASS**, you can submit it for review by your teacher.

## Recommended literature that will help in solving problems

<!-- A feature of the Markdown format is that lists are numbered automatically, so to format “as a list” use the sequence “1.” -->

1. [Harris D.M., Harris S.L., “Digital circuit design and computer architecture: RISC-V”](https://dmkpress.com/catalog/electronics/circuit_design/978-5-97060-961- 3). There is a [tablet version for the previous edition](https://silicon-russia.com/public_materials/2018_01_15_latest_harris_harris_ru_barabanov_version/digital_design_rus-25.10.2017.pdf) (based on the MIPS architecture), and there are shorter [slides for lectures](http://www.silicon-russia.com/public_materials/2016_09_01_harris_and_harris_slides/DDCA2e_LectureSlides_Ru_20160901.zip).
![](https://habrastorage.org/r/w1560/getpro/habr/upload_files/26c/817/9c3/26c8179c34c52fa937cd2200f789c3d0.png)

1. [Romanov A.Yu., Panchul Yu.V. and a team of authors. “Digital synthesis. Practical course"](https://dmkpress.com/catalog/electronics/circuit_design/978-5-97060-850-0/)
