# ee451-assignment-6b-solved
**TO GET THIS SOLUTION VISIT:** [EE451 Assignment 6b Solved](https://www.ankitcodinghub.com/product/ee451-assignment-6b-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100481&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE451 Assignment 6b Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
1. Examples

Copy example files to your home directory.

1. Login to HPC 2. Copy

cp -r /project/xuehaiqi_652/6a .

The hello.cu contains the CUDA implementation of HelloWorld.

<ol>
<li>Login to HPC</li>
<li>Setup MPI toolchain:</li>
<li>Compile
nvcc -O3 hello.cu
</li>
<li>Run
The option -t specifies the limit of run time. Setting it as a small number will get your program scheduled earlier. For more information on srun options, you can use man srun to find out.
</li>
<li>Profile (optional)
srun -n1 –gres=gpu:p100:1 –partition=debug nvprof ./a.out
</li>
<li>Allocate a machine</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
module purge

module load gcc /8.3.0 cuda /10.1.243

</div>
</div>
<div class="layoutArea">
<div class="column">
srun -n1 –gres=gpu:1 -t1 ./a.out

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
salloc -n1 –gres=gpu:1 –mem=16G -t10

// After the allocation, you will log on the machine and have 10 minutes to perform multiple operations

./a.out

// edit , compile , and run again without waiting for a new allocation

./a.out ./a.out

</div>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ol start="2">
<li>(15 points) Refer to the kernel setRowReadColPad in the file checkSmemSquare.cu. Make a new kernel named setColRedRowPad that pads by one column. Then, implement the operation of writing by columns and reading from rows. Run your code and observe the output. Optional: check memory transactions with nvrpof.</li>
<li>(15 points) Refer to the kernel setRowReadCol in the file checkSmemRectangle.cu. Make a new kernel named setColRedRow that writes by columns and reads by rows. Run your code and observe the output. Optional: check memory transactions with nvrpof.</li>
<li>(15 points) Design a CUDA program to perform matrix multiplication C = A×B. The size of each matrix is 1K×1K. Each element is 1 byte. The matrices are initially stored in the global memory of GPU. The GPU has one streaming multiprocessor (SM) with 1K CUDA cores. Each CUDA core runs at 1GHz and can perform one floating point operation in each clock cycle. The peak bandwidth between the GPU and the global memory is 100 GB/s and the cache of GPU has been disabled.
• Design a simple CUDA program using straightforward vector inner product ap- proach.

– Write the pseudo code for your CUDA program including both kernel function and host function.

– Derive a lower bound on the execution time of your kernel function? Explain. • Assuming the GPU has an on-chip buffer (shared memory) which can store 3 ×

32 × 32 elements and has a peak access bandwidth of 1 TB/s.

<ul>
<li>– &nbsp;Write the pseudo code for an optimized CUDA program using block matrix
multiplication approach including both kernel function and host function.
</li>
<li>– &nbsp;Derive a lower bound on the computation time, the local data access time in SM, and the global data access time of your optimized kernel function. Explain.</li>
</ul>
</li>
<li>(10 points) If a kernel is launched with only one Warp (32 threads) in each thread block,</li>
</ol>
the syncthreads() instruction can be left out. Do you think this is correct? Explain.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
6. (30 points) Odd-even transposition sort algorithm (https://www.geeksforgeeks.org/ odd-even-transposition-sort-brick-sort-using-pthreads/) is a parallel sorting algorithm. Design a CUDA program to sort a 2K-element integer array using odd-even sort transposition algorithm with 1K threads. The array is initially stored in the host memory. Write the pseudo code of your host function and kernel function. State any assumptions you may make.

</div>
</div>
</div>
