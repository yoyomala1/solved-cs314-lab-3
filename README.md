Download Link: https://assignmentchef.com/product/solved-cs314-lab-3
<br>
<span class="kksr-muted">Rate this product</span>

Part I

Modify the Minix3 source code such that the string “PID &lt;pid&gt; swapped in” is printed, whenever a user-level process is brought in by the scheduler.

To do this, you will need to understand how the scheduler works. These pages https://minixnitc.github.io/scheduling.html​ , ​http://www.minix3.org/docs/scheduling/report.pdf give a good explanation. You have to look at the code in : ​minix/servers/sched​ and minix/kernel/proc.c​ .

Part II

You can test by using the UnixBench benchmark suite as instructed below:

<ol>

 <li>Get the source code from ftp://​ftp.iitdh.ac.in/opensource/tools/byte-unixbench-mod.zipand copy it to your home folder in the Minix3 VM.(Note that this is a modified version of the suite. The original benchmarks were designed as “fixed duration” benchmarks: they each repeat a certain pattern over and over until a timer expires. The modification was done to make some of the benchmarks (namely, arith,​ ​fstime​, ​pipe​, ​spawn​, ​syscall​) as “fixed work”: they do a certain fixed amount of work, regardless of the time it takes to do that work.).</li>

 <li>Run the command “gmake” to build the benchmarks in the Minix3 VM.</li>

 <li>The compiled benchmarks are in the pgms folder. The folder ​workload_mix​ containssome scripts: ​workload_mix*.sh.​ Each spawns a batch of UnixBench benchmarks. You may study the behavior of the scheduler by seeing the sequence of “PID” prints when these workloads are run. Feel free to create workload mixes of your own (you can write your own benchmarks other than the UnixBench ones as well).</li>