# Continuous Integration # 
In software engineering, continuous integration (CI) is the practice of merging all developer working copies to a shared mainline(trunk /master) several times a day.

Eventually, the repository may become so different from the developers' baselines that they enter what is sometimes referred to as "merge hell", or "integration hell", where the time it takes to integrate exceeds the time it took to make their original changes.

Continuous integration involves integrating early and often, so as to avoid the pitfalls of "integration hell". The practice aims to reduce rework and thus reduce cost and time.

Jez Humble specifies two fundamental principles of CI. The first is “integrate all their work into trunk,” and the second is “at least dailwithout the full stack, the developers will impair themselves and be less effective and efficient. For the developers, continuous integration is a must as it is one the primary practices in eXtreme Programming and Agiy.” Integrating with trunk, mainline, or master daily is part of the definition of CI. Without it, you are not practicing true CI.

# Continuous Delivery # 
Continuous Delivery means that artifacts are built and made ready to be deployed. But they will not be deployed without a manual decision by a human being.

# Continuous Deployment #
Continuous Deployment implies all processes are automated, and a single commit triggers an automated pipeline that will eventually bring a new version of your application to the production environment without any human intervention.
 
 This approach works well in enterprise environments where you plan to use the user as the actual tester and it can be quicker to release.

While many companies practice Continuous Delivery, few embrace Continuous Deployment. Continuous Deployment is risky because anyone could introduce a bug into production with a simple commit, and you need to introduce processes to reduce this risk.

# PipeLine #

Build pipne line represents the steps to move new code from development into production. The basic steps in the build pipeline are:

1. Develop code
2. Unit test (test the code locally to ensure it works as expected)
3. Integrate (the new code into the existing code base)
4. Acceptance test (test the entire system to ensure it meets the users expectations)
5. Deploy to production