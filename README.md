Download Link: https://assignmentchef.com/product/solved-cap4621-hw3-tracking-complete-the-first-3-parts-of-project-4-ghostbusters
<br>
<hr>

<hr>

<hr>

<hr>

<hr>

<hr>

<hr>

<hr>

<hr>

<hr>

<h3>Submission</h3>

You’re not done yet! Follow your instructor’s guidelines to receive credit on your project!

5/5 - (1 vote)

<h3>Table of Contents</h3>

<ul>

 <li><a href="http://ai.berkeley.edu/tracking.html#Introduction">Introduction</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Welcome">Welcome</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q1">Q1: Exact Inference: Observation</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q2">Q2: Exact Inference: Time Elapse</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q3">Q3: Exact Inference: Full System</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q4">Q4: Approximate Inference: Observation</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q5">Q5: Approximate Inference: Time Elapse</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q6">Q6: Joint Particle Filter: Observation</a></li>

 <li><a href="http://ai.berkeley.edu/tracking.html#Q7">Q7: Joint Particle Filter: Time Elapse</a></li>

</ul>

<blockquote>




 <center>

  <img decoding="async" alt="GHOSTBUSTERS" px data-recalc-dims="1" data-src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/busters.png?w=400" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/busters.png?w=400" alt="GHOSTBUSTERS" px data-recalc-dims="1">

  </noscript>

 </center>

 <center>

  I can hear you, ghost.Running won’t save you from myParticle filter!

 </center>




</blockquote>

<h3><a name="Introduction"></a>Introduction</h3>

Pacman spends his life running from ghosts, but things were not always so. Legend has it that many years ago, Pacman’s great grandfather Grandpac learned to hunt ghosts for sport. However, he was blinded by his power and could only track ghosts by their banging and clanging.

In this project, you will design Pacman agents that use sensors to locate and eat invisible ghosts. You’ll advance from locating single, stationary ghosts to hunting packs of multiple moving ghosts with ruthless efficiency.

The code for this project contains the following files, available as a <a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/tracking.zip">zip archive</a>.

<table class="intro" border="0" cellpadding="10">

 <tbody>

  <tr>

   <td colspan="2"><b>Files you’ll edit:</b></td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/bustersAgents.html">bustersAgents.py</a></code></td>

   <td>Agents for playing the Ghostbusters variant of Pacman.</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/inference.html">inference.py</a></code></td>

   <td>Code for tracking ghosts over time using their sounds.</td>

  </tr>

  <tr>

   <td colspan="2"><b>Files you will not edit:</b></td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/busters.html">busters.py</a></code></td>

   <td>The main entry to Ghostbusters (replacing Pacman.py)</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/bustersGhostAgents.html">bustersGhostAgents.py</a></code></td>

   <td>New ghost agents for Ghostbusters</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/distanceCalculator.html">distanceCalculator.py</a></code></td>

   <td>Computes maze distances</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/game.html">game.py</a></code></td>

   <td>Inner workings and helper classes for Pacman</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/ghostAgents.html">ghostAgents.py</a></code></td>

   <td>Agents to control ghosts</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/graphicsDisplay.html">graphicsDisplay.py</a></code></td>

   <td>Graphics for Pacman</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/graphicsUtils.html">graphicsUtils.py</a></code></td>

   <td>Support for Pacman graphics</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/keyboardAgents.html">keyboardAgents.py</a></code></td>

   <td>Keyboard interfaces to control Pacman</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/layout.html">layout.py</a></code></td>

   <td>Code for reading layout files and storing their contents</td>

  </tr>

  <tr>

   <td><code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/util.html">util.py</a></code></td>

   <td>Utility functions</td>

  </tr>

 </tbody>

</table>

<strong>Files to Edit and Submit:</strong> You will fill in portions of <code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/bustersAgents.html">bustersAgents.py</a></code> and <code><a href="http://ai.berkeley.edu/projects/release/tracking/v1/001/docs/inference.html">inference.py</a></code> during the assignment. You should submit these files with your code and comments. Please <em>do not</em> change the other files in this distribution or submit any of our original files other than these files.

<strong>Evaluation:</strong> Your code will be autograded for technical correctness. Please <em>do not</em> change the names of any provided functions or classes within the code, or you will wreak havoc on the autograder. However, the correctness of your implementation — not the autograder’s judgements — will be the final judge of your score. If necessary, we will review and grade assignments individually to ensure that you receive due credit for your work.

<strong>Academic Dishonesty:</strong> We will be checking your code against other submissions in the class for logical redundancy. If you copy someone else’s code and submit it with minor changes, we will know. These cheat detectors are quite hard to fool, so please don’t try. We trust you all to submit your own work only; <em>please</em> don’t let us down. If you do, we will pursue the strongest consequences available to us.

<strong>Getting Help:</strong> You are not alone! If you find yourself stuck on something, contact the course staff for help. Office hours, section, and the discussion forum are there for your support; please use them. If you can’t make our office hours, let us know and we will schedule more. We want these projects to be rewarding and instructional, not frustrating and demoralizing. But, we don’t know when or how to help unless you ask.

<strong>Discussion:</strong> Please be careful not to post spoilers.

<h3><a name="Welcome"></a>Ghostbusters and BNs</h3>

In the cs188 version of Ghostbusters, the goal is to hunt down scared but invisible ghosts. Pacman, ever resourceful, is equipped with sonar (ears) that provides noisy readings of the Manhattan distance to each ghost. The game ends when Pacman has eaten all the ghosts. To start, try playing a game yourself using the keyboard.

<pre>python busters.py</pre>

The blocks of color indicate where the each ghost could possibly be, given the noisy distance readings provided to Pacman. The noisy distances at the bottom of the display are always non-negative, and always within 7 of the true distance. The probability of a distance reading decreases exponentially with its difference from the true distance.

Your primary task in this project is to implement inference to track the ghosts. For the keyboard based game above, a crude form of inference was implemented for you by default: all squares in which a ghost could possibly be are shaded by the color of the ghost. Naturally, we want a better estimate of the ghost’s position. Fortunately, Bayes’ Nets provide us with powerful tools for making the most of the information we have. Throughout the rest of this project, you will implement algorithms for performing both exact and approximate inference using Bayes’ Nets. The lab is challenging, so we do encouarge you to start early and seek help when necessary.

While watching and debugging your code with the autograder, it will be helpful to have some understanding of what the autograder is doing. There are 2 types of tests in this project, as differentiated by their <code>*.test</code> files found in the subdirectories of the <code>test_cases</code> folder. For tests of class <code>DoubleInferenceAgentTest</code>, your will see visualizations of the inference distributions generated by your code, but all Pacman actions will be preselected according to the actions of the staff implementation. This is necessary in order to allow comparision of your distributions with the staff’s distributions. The second type of test is <code>GameScoreTest</code>, in which your <code>BustersAgent</code> will actually select actions for Pacman and you will watch your Pacman play and win games.

As you implement and debug your code, you may find it useful to run a single test at a time. In order to do this you will need to use the -t flag with the autograder. For example if you only want to run the first test of question 1, use:

<pre>python autograder.py -t test_cases/q1/1-ExactObserve</pre>

In general, all test cases can be found inside test_cases/q*.

<h3><a name="Q1"></a>Question 1 (3 points): Exact Inference Observation</h3>

In this question, you will update the <code>observe</code> method in <code>ExactInference</code> class of <code>inference.py</code> to correctly update the agent’s belief distribution over ghost positions given an observation from Pacman’s sensors. A correct implementation should also handle one special case: when a ghost is eaten, you should place that ghost in its prison cell, as described in the comments of <code>observe</code>.

To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q1</pre>

As you watch the test cases, be sure that you understand how the squares converge to their final coloring. In test cases where is Pacman boxed in (which is to say, he is unable to change his observation point), why does Pacman sometimes have trouble finding the exact location of the ghost?

<em>Note:</em> your busters agents have a separate inference module for each ghost they are tracking. That’s why if you print an observation inside the <code>observe</code> function, you’ll only see a single number even though there may be multiple ghosts on the board.

Hints:

<ul>

 <li>You are implementing the online belief update for observing new evidence. Before any readings, Pacman believes the ghost could be anywhere: a uniform prior (see <code>initializeUniformly</code>). After receiving a reading, the <code>observe</code> function is called, which must update the belief at every position.</li>

 <li>Before typing any code, write down the equation of the inference problem you are trying to solve.</li>

 <li>Try printing <code>noisyDistance</code>, <code>emissionModel</code>, and <code>PacmanPosition</code> (in the <code>observe</code> function) to get started.</li>

 <li>In the Pacman display, high posterior beliefs are represented by bright colors, while low beliefs are represented by dim colors. You should start with a large cloud of belief that shrinks over time as more evidence accumulates.</li>

 <li>Beliefs are stored as <code>util.Counter</code> objects (like dictionaries) in a field called <code>self.beliefs</code>, which you should update.</li>

 <li>You should not need to store any evidence. The only thing you need to store in <code>ExactInference</code> is <code>self.beliefs</code>.</li>

</ul>

<h3><a name="Q2"></a>Question 2 (4 points): Exact Inference with Time Elapse</h3>

In the previous question you implemented belief updates for Pacman based on his observations. Fortunately, Pacman’s observations are not his only source of knowledge about where a ghost may be. Pacman also has knowledge about the ways that a ghost may move; namely that the ghost can not move through a wall or more than one space in one timestep.

To understand why this is useful to Pacman, consider the following scenario in which there is Pacman and one Ghost. Pacman receives many observations which indicate the ghost is very near, but then one which indicates the ghost is very far. The reading indicating the ghost is very far is likely to be the result of a buggy sensor. Pacman’s prior knowledge of how the ghost may move will decrease the impact of this reading since Pacman knows the ghost could not move so far in only one move.

In this question, you will implement the <code>elapseTime</code> method in <code>ExactInference</code>. Your agent has access to the action distribution for any <code>GhostAgent</code>. In order to test your <code>elapseTime</code> implementation separately from your <code>observe</code> implementation in the previous question, this question will not make use of your <code>observe</code> implementation.

Since Pacman is not utilizing any observations about the ghost, this means that Pacman will start with a uniform distribution over all spaces, and then update his beliefs according to how he knows the Ghost is able to move. Since Pacman is not observing the ghost, this means the ghost’s actions will not impact Pacman’s beliefs. Over time, Pacman’s beliefs will come to reflect places on the board where he believes ghosts are most likely to be given the geometry of the board and what Pacman already knows about their valid movements.

For the tests in this question we will sometimes use a ghost with random movements and other times we will use the GoSouthGhost. This ghost tends to move south so over time, and without any observations, Pacman’s belief distribution should begin to focus around the bottom of the board. To see which ghost is used for each test case you can look in the .test files.

To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q2</pre>

As an example of the GoSouthGhostAgent, you can run

<pre>python autograder.py -t test_cases/q2/2-ExactElapse</pre>

and observe that the distribution becomes concentrated at the bottom of the board.

As you watch the autograder output, remember that lighter squares indicate that pacman believes a ghost is more likely to occupy that location, and darker squares indicate a ghost is less likely to occupy that location. For which of the test cases do you notice differences emerging in the shading of the squares? Can you explain why some squares get lighter and some squares get darker?

Hints:

<ul>

 <li>Instructions for obtaining a distribution over where a ghost will go next, given its current position and the <code>gameState</code>, appears in the comments of <code>ExactInference.elapseTime</code> in <code>inference.py</code>.</li>

 <li>We assume that ghosts still move independently of one another, so while you can develop all of your code for one ghost at a time, adding multiple ghosts should still work correctly.</li>

</ul>

<h3><a name="Q3"></a>Question 3 (3 points): Exact Inference Full Test</h3>

Now that Pacman knows how to use both his prior knowledge and his observations when figuring out where a ghost is, he is ready to hunt down ghosts on his own. This question will use your <code>observe</code> and <code>elapseTime</code> implementations together, along with a simple greedy hunting strategy which you will implement for this question. In the simple greedy strategy, Pacman assumes that each ghost is in its most likely position according to its beliefs, then moves toward the closest ghost. Up to this point, Pacman has moved by randomly selecting a valid action.

Implement the <code>chooseAction</code> method in <code>GreedyBustersAgent</code> in <code>bustersAgents.py</code>. Your agent should first find the most likely position of each remaining (uncaptured) ghost, then choose an action that minimizes the distance to the closest ghost. If correctly implemented, your agent should win the game in <code>q3/3-gameScoreTest</code> with a score greater than 700 at least 8 out of 10 times. <em>Note:</em> the autograder will also check the correctness of your inference directly, but the outcome of games is a reasonable sanity check.

To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q3</pre>

<i>Note:</i> If you want to run this test (or any of the other tests) without graphics you can add the following flag:

<pre>python autograder.py -q q3 --no-graphics</pre>

Hints:

<ul>

 <li>When correctly implemented, your agent will thrash around a bit in order to capture a ghost.</li>

 <li>The comments of <code>chooseAction</code> provide you with useful method calls for computing maze distance and successor positions.</li>

 <li>Make sure to only consider the living ghosts, as described in the comments.</li>

</ul>

<h3><a name="Q4"></a>Question 4 (3 points): Approximate Inference Observation</h3>

Approximate inference is very trendy among ghost hunters this season. Next, you will implement a particle filtering algorithm for tracking a single ghost.

Implement the functions <code>initializeUniformly</code>, <code>getBeliefDistribution</code>, and <code>observe</code> for the <code>ParticleFilter</code> class in <code>inference.py</code>. A correct implementation should also handle two special cases. (1) When all your particles receive zero weight based on the evidence, you should resample all particles from the prior to recover. (2) When a ghost is eaten, you should update all particles to place that ghost in its prison cell, as described in the comments of <code>observe</code>. When complete, you should be able to track ghosts nearly as effectively as with exact inference.

To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q4</pre>

Hints:

<ul>

 <li>A particle (sample) is a ghost position in this inference problem.</li>

 <li>The belief cloud generated by a particle filter will look noisy compared to the one for exact inference.</li>

 <li><code>util.sample</code> or <code>util.nSample</code> will help you obtain samples from a distribution. If you use <code>util.sample</code> and your implementation is timing out, try using <code>util.nSample</code>.</li>

</ul>

<h3><a name="Q5"></a>Question 5 (4 points): Approximate Inference with Time Elapse</h3>

Implement the <code>elapseTime</code> function for the <code>ParticleFilter</code> class in <code>inference.py</code>. When complete, you should be able to track ghosts nearly as effectively as with exact inference.

Note that in this question, we will test both the <code>elapseTime</code> function in isolation, as well as the full implementation of the particle filter combining <code>elapseTime</code> and <code>observe</code>.

To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q5</pre>

For the tests in this question we will sometimes use a ghost with random movements and other times we will use the GoSouthGhost. This ghost tends to move south so over time, and without any observations, Pacman’s belief distribution should begin to focus around the bottom of the board. To see which ghost is used for each test case you can look in the .test files. As an example, you can run

<pre>python autograder.py -t test_cases/q5/2-ParticleElapse</pre>

and observe that the distribution becomes concentrated at the bottom of the board.

<h3><a name="Q6"></a>Question 6 (4 points): Joint Particle Filter Observation</h3>

So far, we have tracked each ghost independently, which works fine for the default <code>RandomGhost</code> or more advanced <code>DirectionalGhost</code>. However, the prized <code>DispersingGhost</code> chooses actions that avoid other ghosts. Since the ghosts’ transition models are no longer independent, all ghosts must be tracked jointly in a dynamic Bayes net!

The Bayes net has the following structure, where the hidden variables G represent ghost positions and the emission variables E are the noisy distances to each ghost. This structure can be extended to more ghosts, but only two (a and b) are shown below.



<center>

 <img decoding="async" px data-recalc-dims="1" data-src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/dbn.png?w=500" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/dbn.png?w=500" px data-recalc-dims="1">

 </noscript>

</center>You will now implement a particle filter that tracks multiple ghosts simultaneously. Each particle will represent a tuple of ghost positions that is a sample of where all the ghosts are at the present time. The code is already set up to extract marginal distributions about each ghost from the joint inference algorithm you will create, so that belief clouds about individual ghosts can be displayed.



Complete the <code>initializeParticles</code>, <code>getBeliefDistribution</code>, and <code>observeState</code> method in <code>JointParticleFilter</code> to weight and resample the whole list of particles based on new evidence. As before, a correct implementation should also handle two special cases. (1) When all your particles receive zero weight based on the evidence, you should resample all particles from the prior to recover. (2) When a ghost is eaten, you should update all particles to place that ghost in its prison cell, as described in the comments of <code>observeState</code>.

You should now effectively track dispersing ghosts. To run the autograder for this question and visualize the output:

<pre>python autograder.py -q q6</pre>

<h3><a name="Q7"></a>Question 7 (4 points): Joint Particle Filter with Elapse Time</h3>

Complete the <code>elapseTime</code> method in <code>JointParticleFilter</code> in <code>inference.py</code> to resample each particle correctly for the Bayes net. In particular, each ghost should draw a new position conditioned on the positions of all the ghosts at the previous time step. The comments in the method provide instructions for support functions to help with sampling and creating the correct distribution.

Note that completing this question involves removing the call to util.raiseNotDefined(). This means that the autograder will now grade both question 6 and question 7. Since these questions involve joint distributions, they require more computational power (and time) to grade, so please be patient!

As you run the autograder note that <code>q7/1-JointParticleElapse</code> and <code>q7/2-JointParticleElapse</code> test your <code>elapseTime</code> implementations only, and <code>q7/3-JointParticleElapse</code> tests both your <code>elapseTime</code> and <code>observe</code> implementations. Notice the difference between test 1 and test 3. In both tests, pacman knows that the ghosts will move to the sides of the gameboard. What is different between the tests, and why?



<center>

 <img decoding="async" px data-recalc-dims="1" data-src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/disperse.png?w=500" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/ai.berkeley.edu/projects/release/tracking/v1/001/disperse.png?w=500" px data-recalc-dims="1">

 </noscript>

</center>To run the autograder for this question use:



<pre>python autograder.py -q q7</pre>