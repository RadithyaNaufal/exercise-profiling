## 1. All Students Name (`/all-student-name`)
![All Student Name Results](./screenshots/all-student-name.png)

## 2. Highest GPA (`/highest-gpa`)
![Highest GPA Results](./screenshots/highest-gpa.png)

## 3. Test Result (All Students Name)
![All Student Name jtl Results](./screenshots/testresults2.png)

## 4. Test Result (Highest GPA)
![Highest GPA jtl Results](./screenshots/testresults3.png)

## 5. Refactoring Result
![Before Refactoring](./screenshots/highest-gpa.png)
![After Refactoring Results](./screenshots/refactor.png)
After refactoring, the average time is 19ms while before refactor was 40ms.

# Reflection
1. JMeter is testing from outside like a user to see how fast the response is for the web. But profiler is looking deep inside the Java code to find which method is using all the CPU power.
2. Profiling process show us the name of the slow method in the flame graph. It help because we don't need to guess which part is bad. We just look at the wide bar and we find the weak point of the code.
3. I think it is very effective because it show clear details about the bottleneck. Without this tool, I'll spend much time to search the problem manually in many files.
4. The challenge is when JMeter get connection refused and the terminal is confused. I overcome this with open many terminal and check the port 8080 is still on or not.
5. The benefit is we get very detail information like total time and CPU time. It help me to optimize the code with better logic like database sorting and join fetch.
6. If the results is different, I will do the testing several times to get stable numbers. I trust profiler more for code logic but trust JMeter for the user experience speed.
7. My strategy is using database query like ORDER BY or JOIN FETCH to solve N+1 problem. I check the browser and run the test again to make sure the data is still same and not broken. This way the app is fast but the function still work perfectly.