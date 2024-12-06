# Additional experiments for WWW25

## Exp 1: Testing Wukong with different $\Delta$ parameters

### 1. Pic1
#### Setting: 
- node number: $n=10$ 
- favorable situation: $f=0$
- $\Delta$: 0.5s and 1s
#### Results:
Wukong with $\Delta$ as 1s outperforms that with 0.5s in the favorablt situation.

### 2. Pic2
#### Setting: 
- node number: $n=10$ 
- unfavorable situation: $f=3$
- $\Delta$: 1s and 4s
#### Results:
Wukong with $\Delta$ as 1s outperforms that with 4s in the unfavorable situation.



## Exp 2: Testing Wukong with random message delay

### Setting: 
- node number: $n=10$ 
- favorable situation: $f=0$
- $\Delta$: 1s
- Random message delay: Each message has a 10% probability of incurring a 50-millisecond delay.

### Results:
- Pic1: Latency v.s.batch size
- Pic2: Throughput v.s. batch size
- Pic3: Latency v.s. throughput

The three pictures show that even with random message delays, Wukong still outperforms the others by a significant margin.

## Exp 3: Adding a new baseline: LightDAG

Due to time constraints, we have currently added only one new baseline, LightDAG. We obtained the source code for LightDAG from its authors and conducted the corresponding experiments, as shown below. We will consider adding one or two more baselines in the future.
We specifically choose LightDAG1 from [IPDPS'24] LightDAG: A Low-latency DAG-based BFT Consensus through Lightweight Broadcast [10.1109/IPDPS57955.2024.00093](https://doi.ieeecomputersociety.org/10.1109/IPDPS57955.2024.00093) as our additional baseline.

### Setting: 
- node number: $n=10$ 
- favorable situation: $f=0$
- $\Delta$: 1s

### Results:
- Pic1: Latency v.s.batch size
- Pic2: Throughput v.s. batch size
- Pic3: Latency v.s. throughput

Since LightDAG overlooks the latency optimization of non-leader blocks, it also performs worse than Wukong.

