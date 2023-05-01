Download Link: https://assignmentchef.com/product/solved-biomedical-robotics-eeg-data-analysis-assignment-2
<br>
EMG data preprocessing

<strong> </strong>

<strong> </strong>

<ul>

 <li>Load the EMG file EMG_data.mat</li>

</ul>

<em>(Fs=1000Hz; 1<sup>st</sup> row Events: 1=’Cue’; 2=’Go’; 2<sup>nd</sup> row EMG signal Right Biceps; 3<sup>rd</sup> row: Triceps) </em>




<ul>

 <li>For each muscle implement the following steps:</li>

</ul>




<ol>

 <li>Filter (band pass 30-450 Hz) advise FIR filter, recover phase delay 2 with ‘filtfilt’. b. rectify

  <ol>

   <li>compute the envelop of the muscle signals (low pass 3-6 hz)</li>

   <li>down-sample the signal</li>

  </ol></li>

</ol>




<ul>

 <li>Load the motion data kinem_####.mat</li>

</ul>

<em>(Fs=100hz; 1<sup>st</sup> raw Time points; 2<sup>nd </sup>raw Events 1 STOP, 2 CUE, 3 GO, 4 TARGET, 8       longer  than target; 3<sup>rd</sup> raw x cursor, 4<sup>th</sup> raw y cursor; 5<sup>th</sup> raw x target; 6<sup>th</sup> y target) </em>




<ul>

 <li>Considering the experimental design (see below); extract EMG and Motion Data of the first set of movements; the first and last sets of force field; the first set of washout</li>

</ul>




<table width="608">

 <tbody>

  <tr>

   <td width="78">set</td>

   <td width="32">1</td>

   <td width="41">2</td>

   <td width="44">3</td>

   <td width="44">4</td>

   <td width="44">5</td>

   <td width="44">6</td>

   <td width="44">7</td>

   <td width="44">8</td>

   <td width="44">9</td>

   <td width="44">10</td>

   <td width="50">11</td>

   <td width="53">12</td>

  </tr>

  <tr>

   <td width="78">Epoch_start</td>

   <td width="32">1</td>

   <td width="41">97</td>

   <td width="44">193</td>

   <td width="44">289</td>

   <td width="44">385</td>

   <td width="44">481</td>

   <td width="44">577</td>

   <td width="44">673</td>

   <td width="44">769</td>

   <td width="44">865</td>

   <td width="50">961</td>

   <td width="53">1057</td>

  </tr>

  <tr>

   <td width="78">Epoch_end</td>

   <td width="32">96</td>

   <td width="41">192</td>

   <td width="44">288</td>

   <td width="44">384</td>

   <td width="44">480</td>

   <td width="44">576</td>

   <td width="44">672</td>

   <td width="44">768</td>

   <td width="44">864</td>

   <td width="44">960</td>

   <td width="50">1056</td>

   <td width="53">1152</td>

  </tr>

  <tr>

   <td width="78">Condition</td>

   <td width="32">NF</td>

   <td width="41">NF</td>

   <td width="44">NF</td>

   <td width="44">NF</td>

   <td width="44">NF</td>

   <td width="44">FF</td>

   <td width="44">FF</td>

   <td width="44">FF</td>

   <td width="44">FF</td>

   <td width="44">FF</td>

   <td width="50">WA</td>

   <td width="53">WA</td>

  </tr>

 </tbody>

</table>




Each set contains 96 movements (48 out and 48 back movements). NF= No Force; FF=Force Field; WA=Washout. Remember: each movement has a Cue and a Go events which help you segmenting into sets







Questions:

Why the down sampling is computed at the end of the EMG processing?










When the muscle activation starts with respect to the movement (see motion signal)?










Which differences can you detect between the sets with and without the application of the force field?
















The final folder of the assignment must be named Group_# and it must contain:




The Matlab code with comments and generating the following figures for each muscle and each of the 4 sets you extracted (tip: subplots are easier to understand and follow):

<ul>

 <li>EMG row signal with on top the filtered signal plotted with a different color.</li>

 <li>EMG rectified with on top the Envelope plotted with a different color.</li>

 <li>The movement signal X and Y in time</li>

 <li>The xy movements signal together with the targets – this pdf files filled out</li>

</ul>




Please, do not put additional files in the final folder