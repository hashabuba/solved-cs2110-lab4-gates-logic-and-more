Download Link: https://assignmentchef.com/product/solved-cs2110-lab4-gates-logic-and-more
<br>



<h1><a name="_Toc3836"></a>1           CircuitSim</h1>

For this lab, and the rest of the class, you will need to familiarize yourself CircuitSim. To do so, you can follow the following tutorial and implement it in the tutorial.sim file using CircuitSim

<ul>

 <li><a href="https://ra4king.github.io/CircuitSim/tutorial/tut-3-tunnels-splitters">https://ra4king.github.io/CircuitSim/tutorial/tut-3-tunnels-splitters</a></li>

</ul>

Implement the logic as described in the above link in the corresponding circuit. Note that this will <strong>not </strong>be corrected by the autograder and is for your practice only.

<h1><a name="_Toc3837"></a>2           OR Gates</h1>

<h2><a name="_Toc3838"></a>2.1         What is an OR Gate</h2>

<ul>

 <li><strong>OR</strong></li>

</ul>

(<em>A</em>|<em>B</em>)

<table width="103">

 <tbody>

  <tr>

   <td width="26">A</td>

   <td width="26">B</td>

   <td width="51">(<em>A</em>|<em>B</em>)</td>

  </tr>

  <tr>

   <td width="26">0</td>

   <td width="26">0</td>

   <td width="51">0</td>

  </tr>

  <tr>

   <td width="26">0</td>

   <td width="26">1</td>

   <td width="51">1</td>

  </tr>

  <tr>

   <td width="26">1</td>

   <td width="26">0</td>

   <td width="51">1</td>

  </tr>

  <tr>

   <td width="26">1</td>

   <td width="26">1</td>

   <td width="51">1</td>

  </tr>

 </tbody>

</table>

<ul>

 <li><strong>NOR</strong></li>

</ul>

∼ (<em>A</em>|<em>B</em>)

<table width="117">

 <tbody>

  <tr>

   <td width="26">A</td>

   <td width="26">B</td>

   <td width="65">∼ (<em>A</em>|<em>B</em>)</td>

  </tr>

  <tr>

   <td width="26">0</td>

   <td width="26">0</td>

   <td width="65">1</td>

  </tr>

  <tr>

   <td width="26">0</td>

   <td width="26">1</td>

   <td width="65">0</td>

  </tr>

  <tr>

   <td width="26">1</td>

   <td width="26">0</td>

   <td width="65">0</td>

  </tr>

  <tr>

   <td width="26">1</td>

   <td width="26">1</td>

   <td width="65">0</td>

  </tr>

 </tbody>

</table>

1

<ul>

 <li><strong>NOT</strong></li>

</ul>

(∼ <em>A</em>)

<table width="77">

 <tbody>

  <tr>

   <td width="26">A</td>

   <td width="51">(∼ <em>A</em>)</td>

  </tr>

  <tr>

   <td width="26">0</td>

   <td width="51">1</td>

  </tr>

  <tr>

   <td width="26">1</td>

   <td width="51">0</td>

  </tr>

 </tbody>

</table>

<h2><a name="_Toc3839"></a>2.2         Building an OR Gate</h2>

<ul>

 <li>Now that you know what the truth table of an OR gate is, lets try to build one in the <strong>transistors </strong>subcircuit of the <strong>sim </strong>file.</li>

 <li>Since we are using CMOS gate design, we will need a pair of p-type transistors and a pair of n-type transistors to build a NOR gate.</li>

 <li>We will then need one of each of the p-type transistors and n-type transistors to build a NOT gate which we will add to the end of our NOR gate.</li>

 <li>Remember that due to some laws of physics, our p-type transistors will need to be connected to <em>V<sub>dd </sub></em>and our n-type transistors need to be connected to ground.</li>

 <li>Since we want the output to be low for our NOR gate when A or B or both are high, we will need to put our p-type transistors in series so that power does not flow to the output when either is on.</li>

 <li>Because we are using CMOS logic, we know that to complement our p-type transistors being in series, we need to connect our n-type transistors in parallel to the ground.</li>

 <li>Play around with the settings for the transistors until you have a working NOR Gate.</li>

 <li>Now you can use one p-type and one n-type transistor in series to negate the output of our NOR gate, by passing the output to both the transistors and getting the final output from the wire connecting them, making it an OR gate.</li>

 <li>Note: You are only allowed to use the elements in the wiring tab of CircuitSim for this subcircuit. Do <strong>not </strong>use elements in the gates tab of CircuitSim.</li>

</ul>

<h1><a name="_Toc3840"></a>3           Synthesizing Logic</h1>

<h2><a name="_Toc3841"></a>3.1         ANDs, ORs and DeMorgan’s Law</h2>

In this section you will be synthesizing a logical statement into gates for testing. This circuit must be made in the <strong>deMorgan </strong>subcircuit of the <strong>lab.sim </strong>file. Feel free to use the pre-made gates in the gates tab of CircuitSim.

<ul>

 <li>Logic: (∼ (∼ <em>A</em>&amp;<em>B</em>)| ∼ (∼ <em>B</em>|<em>C</em>))</li>

</ul>

See the corresponding circuits and implement the logic as described above. Do <strong>not </strong>change the names of the inputs or outputs. If you do, our little autograder will cry!!

<h1><a name="_Toc3842"></a>4           Autograder</h1>

Once complete, run the autograder

java -jar lab4-tester.jar

at a command prompt in the same directory as all your .sim files.

Show your TAs the tests pass to get checked off early!