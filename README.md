Started by upstream project "ELIS-Non-Prod/ELIS-Dashboard-Pipeline" build number 2310originally caused by:
 Operations Center Trigger
 Started by user Donkor, Vincent Started by upstream project "ELIS-Non-Prod/ELIS-Dashboard-Pipeline" build number 2308 originally caused by:
  Operations Center Trigger
Running as SYSTEM
Building remotely on NonProd Arm64 Permanent (arm64-docker arm64 arm) in workspace /var/lib/jenkins/workspace/ELIS-Non-Prod/GitVersion
[WS-CLEANUP] Deleting project workspace...
[WS-CLEANUP] Deferred wipeout is used...
[WS-CLEANUP] Done
The recommended git tool is: NONE
using credential Jenkins-ent-ssh-node
Cloning the remote Git repository
Cloning repository git@git.uscis.dhs.gov:USCIS/elis-dashboard.git
 > git init /var/lib/jenkins/workspace/ELIS-Non-Prod/GitVersion # timeout=10
Fetching upstream changes from git@git.uscis.dhs.gov:USCIS/elis-dashboard.git
 > git --version # timeout=10
 > git --version # 'git version 2.40.1'
using GIT_SSH to set credentials Git SSH Key - Node
Verifying host key using known hosts file
 > git fetch --tags --force --progress -- git@git.uscis.dhs.gov:USCIS/elis-dashboard.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url git@git.uscis.dhs.gov:USCIS/elis-dashboard.git # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
 > git rev-parse refs/remotes/origin/CI_BRANCH^{commit} # timeout=10
JENKINS-19022: warning: possible memory leak due to Git plugin usage; see: https://plugins.jenkins.io/git/#remove-git-plugin-buildsbybranch-builddata-script
Checking out Revision 86ed794a69bf31999955688dd4379cc6b66e8886 (refs/remotes/origin/CI_BRANCH)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 86ed794a69bf31999955688dd4379cc6b66e8886 # timeout=10
Commit message: "Merge pull request #1044 from USCIS/Hornet-126335-nav-fix"
 > git rev-list --no-walk 86ed794a69bf31999955688dd4379cc6b66e8886 # timeout=10
The recommended git tool is: NONE
using credential Jenkins-ent-ssh-node
 > git tag -l 1.1.2310-ci # timeout=10
 > git tag -a -f -m Jenkins Git plugin tagging with 1.1.2310-ci 1.1.2310-ci # timeout=10
ERROR: Failed to push tag 1.1.2310-ci to origin
hudson.plugins.git.GitException: Could not apply tag 1.1.2310-ci
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.tag(CliGitAPIImpl.java:1921)
	at hudson.plugins.git.GitAPI.tag(GitAPI.java:354)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at hudson.remoting.RemoteInvocationHandler$RPCRequest.perform(RemoteInvocationHandler.java:924)
	at hudson.remoting.RemoteInvocationHandler$RPCRequest.call(RemoteInvocationHandler.java:902)
	at hudson.remoting.RemoteInvocationHandler$RPCRequest.call(RemoteInvocationHandler.java:853)
	at hudson.remoting.UserRequest.perform(UserRequest.java:211)
	at hudson.remoting.UserRequest.perform(UserRequest.java:54)
	at hudson.remoting.Request$2.run(Request.java:377)
	at hudson.remoting.InterceptingExecutorService.lambda$wrap$0(InterceptingExecutorService.java:78)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628)
	at java.base/java.lang.Thread.run(Thread.java:829)
	Suppressed: hudson.remoting.Channel$CallSiteStackTrace: Remote call to NonProd Arm64 Permanent
		at hudson.remoting.Channel.attachCallSiteStackTrace(Channel.java:1784)
		at hudson.remoting.UserRequest$ExceptionResponse.retrieve(UserRequest.java:356)
		at hudson.remoting.Channel.call(Channel.java:1000)
		at hudson.remoting.RemoteInvocationHandler.invoke(RemoteInvocationHandler.java:285)
		at com.sun.proxy.$Proxy126.tag(Unknown Source)
		at org.jenkinsci.plugins.gitclient.RemoteGitImpl.tag(RemoteGitImpl.java:585)
		at hudson.plugins.git.GitPublisher.perform(GitPublisher.java:258)
		at hudson.tasks.BuildStepMonitor$1.perform(BuildStepMonitor.java:20)
		at hudson.model.AbstractBuild$AbstractBuildExecution.perform(AbstractBuild.java:818)
		at hudson.model.AbstractBuild$AbstractBuildExecution.performAllBuildSteps(AbstractBuild.java:767)
		at hudson.model.Build$BuildExecution.post2(Build.java:179)
		at hudson.model.AbstractBuild$AbstractBuildExecution.post(AbstractBuild.java:711)
		at hudson.model.Run.execute(Run.java:1924)
		at hudson.model.FreeStyleBuild.run(FreeStyleBuild.java:44)
		at hudson.model.ResourceController.execute(ResourceController.java:101)
		at hudson.model.Executor.run(Executor.java:442)
Caused by: hudson.plugins.git.GitException: Command "git tag -a -f -m Jenkins Git plugin tagging with 1.1.2310-ci 1.1.2310-ci" returned status code 128:
stdout: 
stderr: Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <jenkins@ip-10-193-134-105.aws.uscis.dhs.gov>) not allowed

	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.launchCommandIn(CliGitAPIImpl.java:2842)
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.launchCommandIn(CliGitAPIImpl.java:2762)
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.launchCommandIn(CliGitAPIImpl.java:2757)
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.launchCommand(CliGitAPIImpl.java:2051)
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.launchCommand(CliGitAPIImpl.java:2063)
	at org.jenkinsci.plugins.gitclient.CliGitAPIImpl.tag(CliGitAPIImpl.java:1919)
	... 16 more
Build step 'Git Publisher' marked build as failure
Finished: FAILURE
