Download Link: https://assignmentchef.com/product/solved-uwee572-final-project-2-4-ghz-balanced-amplifier
<br>
The objective of this assignment is to design a 2.4 GHz balanced amplifier with characteristics of at least 10dB at operating frequency and -20dB attenuation beyond 5GHz.

<h1>Introduction</h1>

A balanced amplifier has two amplifying circuits that operate in quadrature ( apart). The amplifier is composed of two couplers; the first splits the signal and the second recombines the signal back in phase. One effect of the balanced amplifier is the signal is amplified in parallel, achieving twice the amount of gain compared to a regular amplifier. Another important effect is that it has great impedance matching and minimizes the reflection coefficient. The couplers in the balanced amplifier have the desired response up to 5GHz, however the magnitude of  has a large peak at 7GHz that needs to be minimized. A series of Butterworth filters are designed to reduce the undesired response. The overall design is hybrid-gain-hybrid-filter.

<h1>Summary</h1>

The attached system layout achieves all the project objectives using the hybrid-gain-hybrid-filter design. The transmission line uses Roger Duroid 5870 with 0.5 ounce copper and 1.57mm thickness. The magnitude of is 27.07dB at operating frequency and -8.60dB at 5GHz.  In respect to , the attenuation is -31dB at 5GHz and more than -20dB for all further frequencies. A 4.7mm gap is provided for the ERA_2SM _48mA_Plus25 amps and 5.3mm for the 47pF capacitors.

<em>Figure 1: 2.4GHz Balanced Amplifier Fabrication</em>

<table width="252">

 <tbody>

  <tr>

   <td width="118">Parameter</td>

   <td width="117">EM Response (</td>

   <td width="16">)</td>

  </tr>

  <tr>

   <td width="118"></td>

   <td width="117">27.07 dB</td>

   <td width="16"> </td>

  </tr>

  <tr>

   <td width="118"></td>

   <td width="117">-43.39 dB</td>

   <td width="16"> </td>

  </tr>

  <tr>

   <td width="118"></td>

   <td width="117">-33.97 dB</td>

   <td width="16"> </td>

  </tr>

  <tr>

   <td width="118"></td>

   <td width="117">-17.30 dB</td>

   <td width="16"> </td>

  </tr>

 </tbody>

</table>

<em>Table 1: Balanced Amplifier S-Parameters</em>

<h1>Results</h1>

The balanced amplifier was designed in multiple stages to meet the objectives. Each stage was designed using physical models and electromagnetism (EM) simulations. The couplers were calculated first and required tuning to meet all criteria. In addition to -3dB with             phase difference on the output ports, the following goals were met:

equals (D, C) and (A, D) equals (B, C). Using the layout modification technique, the physical model was successfully tuned. I found modifying variables  and  had the greatest effect in tuning the coupler and the final results are shown in <em>Figure 6</em>. It is noted that EM simulations often do not yield the same results as the circuit models, however the physical transmission line model is used as a benchmark  and starting point. The lengths for  are included for the untuned physical circuit, tuned physical circuit, and tuned EM simulations.

<table width="474">

 <tbody>

  <tr>

   <td width="114">Parameter</td>

   <td width="125">Untuned Physical</td>

   <td width="120">Tuned Physical</td>

   <td width="115">Tuned EM</td>

  </tr>

  <tr>

   <td width="114">x (mm)</td>

   <td width="125">21.83</td>

   <td width="120">24.21</td>

   <td width="115">24</td>

  </tr>

  <tr>

   <td width="114">y (mm)</td>

   <td width="125">22.19</td>

   <td width="120">15.34</td>

   <td width="115">24</td>

  </tr>

  <tr>

   <td width="114">z (mm)</td>

   <td width="125">7.56</td>

   <td width="120">8.30</td>

   <td width="115">7.9</td>

  </tr>

 </tbody>

</table>

<em>Table 2: Hybrid Coupler Tuning</em>

Results for the hybrid EM simulations are provided in <em>Figure 7</em>. After tuning, the EM response greatly resembled the physical model and very close to the ideal response.

<table width="252">

 <tbody>

  <tr>

   <td width="109">Parameter</td>

   <td width="125">EM Response (</td>

   <td width="18">)</td>

  </tr>

  <tr>

   <td width="109"> </td>

   <td width="125">-3.17 dB</td>

   <td width="18"> </td>

  </tr>

  <tr>

   <td width="109"></td>

   <td width="125">-3.10 dB</td>

   <td width="18"> </td>

  </tr>

  <tr>

   <td width="109"></td>

   <td width="125">-3.10 dB</td>

   <td width="18"> </td>

  </tr>

  <tr>

   <td width="109"></td>

   <td width="125">-3.17 dB</td>

   <td width="18"> </td>

  </tr>

 </tbody>

</table>

<em>Table 3: Hybrid </em>S-Parameters

The hybrid had the following performance metrics:

where to characterize the Butterworth filters. The response of this system is shown in <em>Figure 10</em>. The gain at 2.4GHz is 14.34dB and meets the project objective, however the gain at 5GHz is 7.35dB. This

<em>Figure 2: Attenuation Elements and Performance</em>

in calculating Kuroda

The 2.5GHz Butterworth filter from lab 5 is used as a starting point. To adjust the cutoff frequency of the filter, the physical length of each transmission line is multiplied by variable           .  Looking at the response of the unfiltered system, I chose the cutoff frequency at 3.3GHz. Also note that wavelength is inversely proportional to frequency such that . The value of  is tuned until I got the desired response at .  The physical transmission line model results are provided in <em>Figure 8.</em>

The physical response performs well, however it was not easy to implement in the EM simulation. The shunts in the filter have small impedance resulting in wide transmission lines that did not fit with the other TLs. Instead, a shunt can be divided into two symmetric shunts as long as the total admittance remains the same. Let          be the small impedance shunt and  by the equivalent shunts, then

. The symmetric shunts are calculated using the values from lab 5.

<table width="450">

 <tbody>

  <tr>

   <td width="231">Previous Shunt</td>

   <td width="219">Symmetric Shunts</td>

  </tr>

  <tr>

   <td width="231">                  Z = 27.1</td>

   <td width="219">                Z = 54.2</td>

  </tr>

  <tr>

   <td width="231">                 W = 10.76mm</td>

   <td width="219">                W = 4.10mm</td>

  </tr>

  <tr>

   <td width="231">                  P = 10.35mm*$a</td>

   <td width="219">                P = 10.69*$a</td>

  </tr>

  <tr>

   <td width="231">Previous Shunt</td>

   <td width="219">Symmetric Shunts</td>

  </tr>

  <tr>

   <td width="231">                  Z = 37.1</td>

   <td width="219">                Z = 74.2</td>

  </tr>

  <tr>

   <td width="231">                 W = 7.12mm</td>

   <td width="219">               W = 2.41mm</td>

  </tr>

  <tr>

   <td width="231">                  P = 10.50mm*$a</td>

   <td width="219">                P = 10.87*$a</td>

  </tr>

 </tbody>

</table>

<em>Table 4: Symmetric Shunts</em>

The EM simulations strongly agree with the physical response.  magnitudes are provided in <em>Table 5</em>.

<table width="475">

 <tbody>

  <tr>

   <td width="124">   Simulation</td>

   <td width="120">2.4 GHz</td>

   <td width="122">3.3 GHz</td>

   <td width="109">5 GHz</td>

  </tr>

  <tr>

   <td width="124">   Physical</td>

   <td width="120">-0.21 dB</td>

   <td width="122">-0.21 dB</td>

   <td width="109">-30.38 dB</td>

  </tr>

  <tr>

   <td width="124">   EM</td>

   <td width="120">-1.02 dB</td>

   <td width="122">-3.11 dB</td>

   <td width="109">-18.44 dB</td>

  </tr>

 </tbody>

</table>

<em>Table 5: 3.3GHz Butterworth Filter Response</em>

A key characteristics of the Butterworth filter is that ~1dB is lost at the operating frequency. This is a necessary trade-off in order to reduce the unwanted frequencies. Also, the magnitude at 5GHz does not meet the 20dB attenuation for the project, however it is close. Now the system is examined with the 3.3GHz Butterworth filter and results are included in <em>Figure 11</em>.

The physical transmission line model with 3.3GHz Butterworth filter has 14.13dB gain at 2.4GHz and

-25.81GHz gain at 5GHz. Both of these magnitudes meet the specifications of the project, however the 20dB attenuation is not maintained after 5GHz. Between 8GHz and 10GHz the magnitude of  approaches 0dB and no longer meets the requirements. In order to account for this behavior, a second Butterworth filter is introduced.

The same approach from the 3.3GHz Butterworth filter is used. The physical length of the transmission lines from lab5 are multiplied by variable . The desired cutoff frequency is chosen at 5GHz, so  is defined as . The procedure of creating symmetric impedance shunts is repeated for this filter and the results are included in <em>Figure 9</em>.  The EM simulation did not perform exactly as the physical transmission line. The cutoff frequency for the EM simulation is shifted to ~4.2GHz and 0.22dB is lost at the operating frequency. The responses for the physical and EM simulations are provided in <em>Table 6</em>.

<table width="330">

 <tbody>

  <tr>

   <td width="118">   Simulation</td>

   <td width="110">2.4GHz</td>

   <td width="103">5GHz</td>

  </tr>

  <tr>

   <td width="118">   Physical</td>

   <td width="110">-0.05 dB</td>

   <td width="103">-3.01 dB</td>

  </tr>

  <tr>

   <td width="118">   EM</td>

   <td width="110">-0.22 dB</td>

   <td width="103">-5.83 dB</td>

  </tr>

 </tbody>

</table>

<em>Table 6: 5GHz Butterworth Filter Response</em>

Now both filters are included in the physical system and results are shown in <em>Figure 12</em>. The system performed well and filter effects are seen with minimums at 6.6GHz and 10GHz. Overall, 20dB attenuation is maintained after 5GHz and requirements for the project are met. The EM layout required little modification because each component was previously tuned during the design. <em>Figure 13</em> includes the EM simulation and <em>Table 7 </em>shows the magnitudes for both simulations.  A key difference is the EM results have larger magnitudes across all frequencies. I found that removing the decoupling capacitor brought the magnitude back into alignment with the physical simulation.

<table width="330">

 <tbody>

  <tr>

   <td width="102">   Simulation</td>

   <td width="16"> </td>

   <td width="110">2.4GHz</td>

   <td width="103">5GHz</td>

  </tr>

  <tr>

   <td width="102">   Physical (</td>

   <td width="16">)</td>

   <td width="110">14.13 dB</td>

   <td width="103">-23.44 dB</td>

  </tr>

  <tr>

   <td width="102">   EM ()</td>

   <td width="16"> </td>

   <td width="110">27.85 dB</td>

   <td width="103">-1.92 dB</td>

  </tr>

 </tbody>

</table>

<em>Table 7: Balanced Amplifier – </em>

<em>2.4GHz &amp; 5GHz Butterworth Filters</em>

At this point, the system meets all the requirements, but I was curious if I could improve it further. To decrease the magnitude at 5GHz, I added two           shunts. This is a known tool to create band reject filters. The transmission line acts like a capacitor with          . For the specified frequency, the  shunt has very little impedance and becomes an effective short. I chose  shunts at 4.75GHz and 5.25GHz to reduce the magnitude around 5GHz. The results of these changes are shown in <em>Figure 14</em> and <em>Figure 15</em>.

<table width="330">

 <tbody>

  <tr>

   <td width="102">   Simulation</td>

   <td width="16"> </td>

   <td width="110">2.4GHz</td>

   <td width="103">5GHz</td>

  </tr>

  <tr>

   <td width="102">   Physical (</td>

   <td width="16">)</td>

   <td width="110">13.54 dB</td>

   <td width="103">-58.22 dB</td>

  </tr>

  <tr>

   <td width="102">   EM ()</td>

   <td width="16"> </td>

   <td width="110">27.07 dB</td>

   <td width="103">-8.60 dB</td>

  </tr>

 </tbody>

</table>

<em>Table 8: Balanced Amplifier – </em>

<em>2.4GHz &amp; 5GHz Butterworth Filter </em>

<em>4.75 &amp; 5.25GHz Shunts</em>

The final design uses all the stages discussed including the 3.3GHz Butterworth filter, 5GHz

Butterworth filter, 4.75Ghz shunt, and 5.25 GHz shunt. The             magnitude of this system is 27.07dB at operating frequency and -8.60dB at 5GHz. In respect to       , the attenuation is -31dB at 5GHz and more than -20dB for all further frequencies. The attached figures show the performance of each component and the system as a whole.

<em>Figure 6: 90 Hybrid Physical Model Simulation</em>

<em>Figure 7: 90 Hybrid Physical Model Simulation </em>Physical     EM

<em>Figure 8: 3.3GHz Butterworth Filter</em>

Physical                                                                                                    EM

<em>Figure 9: 5GHz Butterworth Filter</em>

<em>Figure 10: Balanced Amplifier Physical; No Filters</em>

<em>Figure 11: Balanced Amplifier Physical; 3.3GHz Butterworth Filter</em>

<em>Figure 12: Balanced Amplifier Physical; 3.3 &amp; 5GHz Butterworth Filters</em>

<em>Figure 13: Balanced Amplifier EM; 3.3 &amp; 5GHz Butterworth Filters</em>

<em>Figure 14: Balanced Amplifier Physical; 3.3 &amp; 5GHz Butterworth Filters; 4.75 &amp; 5.25GHz Shunts</em>

<em>Figure 15: Balanced Amplifier EM; 3.3 &amp; 5GHz Butterworth Filters; 4.75 &amp; 5.25GHz Shunts</em>

<h1>Discussion</h1>

Throughout the design process, I came across several challenges. I observed tuning EM simulations can take multiple iterations and require patience. From designing the Butterworth filters, I found more symmetric filters performed better in EM simulations. My suspicion is the position of the duroid transmission line and the surface area connected between them are the cause of this. Another challenge was choosing the cutoff frequency for the Butterworth filter such that all the project requirements were met. I greatly enjoyed designing the 2.4GHz balanced amplifier and look forward to building future microwave circuits.