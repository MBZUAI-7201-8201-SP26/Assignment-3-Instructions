# Assignment-3-Instructions

Instructions for Assignment 3

This document explains:
- how to accept the assignment,
- what you need to complete for Assignment 3, and
- how the cross-validation (peer check) works for Assignment 3.

Please read it carefully before starting!

## Part 1: Do the Lab

1. (Similar to Assignments 1 and 2) Accept the assignment via the GitHub Classroom link.

2. Read the [Lab 3 instructions](https://github.com/tenstorrent/tt-metal/blob/main/docs/source/tt-metalium/tt_metal/labs/matmul/lab3/lab3.rst).

3. Complete the exercises by following the instructions in the lab document.

4. Save evidence that your code runs correctly, such as terminal outputs, logs, screenshots, profiler outputs, and the required plots/figures where applicable.

5. You will need to submit your source codes for the following exercises particularly:
   - **Exercise 2:** .
   - **Exercise 3:** .
   - **Exercise 4:** .
   - 
6. Required deliverables:
   - A `README.md` with build/run commands for each exercise you implemented
   - Evidence artifacts committed to the repo (or linked with clear paths.

---

## Part 2: Cross-Validation (Peer Review)

You will be randomly assigned with another classmate (details will be announced later).

For cross-validation, you will:

1. Grant access to the classmate you are assigned to (as instructed in class).
2. Follow your assigned classmate’s `README.md` and try to reproduce their results for Assignment 3.
3. Check whether their outputs match what they claim.
4. Save evidence of your cross validation attempts (terminal output, screenshots, notes, profiler outputs).
5. Open an issue on your assigned classmate's repo with your evidence and findings:
   - what you ran,
   - what worked,
   - what did not work (if anything) and how it failed,
   - whether performance numbers/plots look consistent with their claims.
6. Use the Assignment 3 checklist below in your opened issue and feel free to add comments/questions.
7. You can also reply to the issue opened by your assigned classmate in your own repo.

---

## Assignment 3 Checklist

### Part 1: Your Lab

- ⬜ Completed **Exercise 1** (introduced NoC addressing bug + sync bug, used Watcher/logs to diagnose, reverted changes, program passes again)
- ⬜ Completed **Exercise 2** (sender participates; output contains **4** copies; correctness verified)
- ⬜ Profiled Exercise 2 (Release build; Watcher/DPRINT disabled) and recorded firmware time
- ⬜ Completed **Exercise 3** (batched multicast, `tiles_per_batch = 10`, CB resized correctly, divisibility assertion added)
- ⬜ Profiled Exercise 3 and compared firmware time vs Exercise 2 (include result in README)
- ⬜ Completed **Exercise 4** (multicast-enabled multi-core matmul starting from Lab 2 Ex2)
- ⬜ Implemented **4 reader kernels** for the 4 roles (top-left, left-column, top-row, interior)
- ⬜ Created **4 semaphores** (A: receivers-ready + slab-sent, B: receivers-ready + slab-sent) on all cores
- ⬜ Correctness verified for Exercise 4 (matches reference/expected output)
- ⬜ Performance comparison done for Exercise 4 vs Lab 2 (include plots/summary)
- ⬜ Clear instructions to reproduce results in `README.md`
- ⬜ All work committed and pushed to your GitHub Classroom repository

### Part 2: Cross-Validation

- ⬜ Read and followed the assigned classmate’s `README.md`
- ⬜ Successfully reproduced and verified their results (or documented failures clearly)
- ⬜ Opened an issue on their repo with evidence and the checklist
- ⬜ Documented and pushed your reproduction attempts (evidence/logs) to your own repo
