# KMY MMD-1 Circuit Analyzer and Fault Detection Device User Guide

The KMY MMD-1 is a professional fault detection and testing device that enables the detection of defective components on electronic cards without applying any power to the card. When two probes are brought into contact with the terminals of the suspected component, the device applies a low-level test signal to the component, graphically normalizing the dynamic relationship between voltage and current on the screen. This resulting characteristic curve is considered the electrical "fingerprint" of the component. Depending on the form of the curve in the graph, it can be immediately determined whether the component is a resistor, capacitor, or a defective diode. An oscilloscope and a two-channel voltmeter are also integrated within the system.

The device can be utilized by connecting it to a computer running the Windows operating system via a USB cable, or it can be operated using the wireless connection option. Furthermore, the control software is fully compatible with smartphone and tablet devices running the Android operating system.

*(Note: The English user guide [user-guide-en.md](user-guide-en.md) is currently out of date. Until the English version is updated, the technical information in this updated English guide must be taken as the primary reference.)*

---

## Table of Contents

* **A. Introduction**
  1. [What Does This Device Do?](#1-what-does-this-device-do)
  2. [A First Look at the Device](#2-a-first-look-at-the-device)
  3. [Requirements and Preliminary Preparation](#3-requirements-and-preliminary-preparation)
* **B. Installation and Initial Connection**
  4. [Software Installation](#4-software-installation)
  5. [Initial Connection to the Device](#5-initial-connection-to-the-device)
  6. [Your First Measurement](#6-your-first-measurement)
* **C. Curve Tracer (V-I Analyzer)**
  7. [Working Principle of Curve Testing](#7-working-principle-of-curve-testing)
  8. [Basic Measurement Settings](#8-basic-measurement-settings)
  9. [Reading the Curve: Component Signatures Gallery](#9-reading-the-curve-component-signatures-gallery)
  10. [Advanced Measurement Settings](#10-advanced-measurement-settings)
  11. [Dual Probe Usage and Synchronous Mode](#11-dual-probe-usage-and-synchronous-mode)
* **D. Comparison Mode and Board Testing**
  12. [Comparison Functions](#12-comparison-functions)
  13. [Board Recording and Board Testing System](#13-board-recording-and-board-testing-system)
* **E. Other Auxiliary Tools**
  14. [Oscilloscope Mode](#14-oscilloscope-mode)
  15. [Multimeter Mode](#15-multimeter-mode)
* **F. System Settings, Calibration, and Connection**
  16. [System Settings](#16-system-settings)
  17. [Calibration Wizard](#17-calibration-wizard)
  18. [Wireless Usage and Wi-Fi Setup](#18-wireless-usage-and-wi-fi-setup)
  19. [Usage on Mobile Devices (Phone/Tablet)](#19-usage-on-mobile-devices-phonetablet)
  20. [Software Updates](#20-software-updates)
* **G. Reference Information**
  21. [Technical Limits and Parameters](#21-technical-limits-and-parameters)
  22. [Troubleshooting and Solutions](#22-troubleshooting-and-solutions)
  23. [Technical Support and Contact](#23-technical-support-and-contact)

---

## Section A — Introduction

### 1. What Does This Device Do?

In the process of testing a faulty electronic board, applying power directly to the board is a common method, but this operation generally leads to permanent damage to other intact components on the board. The KMY MMD-1 is designed specifically to eliminate these risks. By means of the device, the health status of components can be safely analyzed by contacting them individually without applying power to the board.

The device performs this detection using three different methods:

* **Curve Testing (V-I Analysis):** Applies a low-level test signal to the component to obtain the voltage-current curve. In most cases, the system automatically detects the type and value of the component. Each component class, such as resistor, capacitor, inductor, diode, and zener, draws a unique curve. These curves can be examined with real examples in Section 9.
* **Board Recording and Board Testing:** This method is developed especially for organizations engaged in mass production or technical personnel conducting repetitive work on the same board model. The test points on an approved reference board are recorded into the system once. Subsequently, boards suspected of being faulty are automatically compared with these recorded data. The device clearly reports the points deviating from the reference values to the user.
* **Oscilloscope and Multimeter:** After the board is energized, the same probes and the same software interface can be utilized to monitor live signals or make precise voltage measurements.

In summary, the KMY MMD-1 is a professional auxiliary hardware designed for technical personnel engaged in electronic design, fault detection, and repair activities, as well as manufacturers wishing to perform rapid validation on mass production lines.

### 2. A First Look at the Device

There are 4 pieces of 4 mm banana-type socket inputs on the front panel of the device. The sockets positioned on the far left and far right are active probes (Probe 1 and Probe 2). Curve testing, oscilloscope, and multimeter measurements are all carried out through these two active inputs. The middle two sockets are chassis (GND) connection points.

During the measurement of any component, one terminal of the component must be connected to the active probe (Probe 1 or Probe 2), and the other terminal must be connected to the adjacent GND socket. For example, when testing a two-terminal resistor or diode, one terminal is connected to Probe 1, and the other terminal is connected to the adjacent chassis (GND) line.

![Device overview](images/shared/device-overview.svg)


There are two connection points on the rear panel of the device:
* **USB-C Input (Right):** Provides computer connection and data transfer. The device also obtains the energy required for its operation through this port.
* **External Power Input (Left):** Reserved for alternative power supply requirements.


There are no physical buttons or notification LEDs on the device chassis. The status information, connection, and active operating modes of the device must always be monitored from the software screen running on the computer or mobile device.

### 3. Requirements and Preliminary Preparation

To operate the system, the KMY MMD-1 device, a USB cable, and a computer with a 64-bit Windows 10 or Windows 11 operating system are sufficient. In case of wireless use, a smartphone or tablet running Android 7.0 and above can be preferred. Installation is highly simplified, and the software can be installed on Windows without requiring administrator privileges.

⚠️ **Important Safety Warning:** Before making contact with the board with the probes, it must be absolutely ensured that the board to be tested is **completely powered off** and that all **capacitors on it are fully discharged**. While the curve tracer is active, it applies its own test signal from the probes. An energized circuit can distort this signal and cause permanent damage to both the board and the KMY MMD-1 device.

---

## Section B — Installation and Initial Connection

### 4. Software Installation

#### Windows Operating System Installation Steps
1. Visit the official GitHub release page: [https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest)
2. Download and run the current **KMY-MMD-1-Kurulum.exe** file.
3. At the beginning of the installation, a language selection screen will be displayed. This selection only covers the installation steps; the application's own interface language can be changed at any time from the "Settings" menu.
4. Follow the steps in the installation wizard. To avoid administrator barriers on the system, the program is installed directly into the user directory instead of "Program Files" (`%LocalAppData%\Programs\KMY MMD-1`). In this way, the installation is completed successfully even if there are no administrator privileges on the computer.

All components and firmware required by the device and software are included in this single installation file; no additional downloads are necessary. The `.imza` extension file on the download page is the security verification of the installation. The application automatically checks future updates with this signature file; no manual action is required.

*Note: Even if the application is uninstalled from the system, the created board projects, calibration profiles, and exported test reports continue to be safely stored in the **Documents** folder. Only user preferences, such as language selection, are reset during the uninstallation process.*

#### Android Operating System Installation Steps
1. Download the **KMY-MMD-1-Mobil.apk** file from the relevant release page to the mobile device and open the file.
2. The Android operating system will request permission to install from sources outside the store due to security protocols. After the "Allow from this source" option is enabled, the installation will be completed automatically.
3. The mobile application operates smoothly on all 64-bit ARM architecture devices with Android 7.0 and above.

*Important Note: The mobile application can only connect to the device wirelessly via Wi-Fi. Direct connection via USB is not supported on mobile devices. The only practical difference of this is that the device firmware cannot be updated via the mobile device. In terms of measurement, analysis, and testing functions, there is no functional difference between the mobile version and the desktop version. For detailed information, the [Usage on Mobile Devices](#19-usage-on-mobile-devices-phonetablet) section can be examined.*

### 5. Initial Connection to the Device

After connecting the USB cable to the computer, run the **KMY MMD-1** application. Your device will be displayed in the list of available devices at the top of the screen; press the **Connect** button to initiate the connection.

To guarantee accuracy, the device automatically calibrates itself according to the internal voltage references at each startup (self-calibration process). This process takes **approximately 13-15 seconds**. During this critical process, the controls in the software are temporarily locked; the output cannot be activated, and the operating modes cannot be selected. During this period, the device must be expected to complete its preparation process. When the connection status indicator turns green, the device is ready for use.

> 🖼️ **[IMAGE PLACEHOLDER - THIS BLOCK MUST BE COMPLETELY DELETED AFTER THE IMAGE IS ADDED]**
> **Image Description:** Screenshot of the KMY MMD-1 software main window during the startup calibration phase. The connection list must be visible at the top, showing the device as "Calibrating..." or "Connecting...", and all controls must be greyed out/locked with a 13-15 second countdown indicator.
> **Filename Suggestion:** `software-connection.png`
> **Usage Instructions:** After the image is placed here, this description box (placeholder) must be completely deleted.

*If an error is received when clicking the "Connect" button immediately after plugging in the cable, the hardware may not have completed its startup routine yet. It is recommended to repeat the process after waiting a few seconds.*

### 6. Your First Measurement

To test the device, obtain a standard resistor of known value. Although its value is not highly critical, any resistor **between 100 Ω and 10 kΩ** is extremely suitable for the first test.

1. Connect one terminal of the resistor to the active input designated as **Probe 1**, and the other terminal to the adjacent **GND** socket.
2. Leave the parameters in the left panel at their default settings. The initial settings of **Voltage: Low** and **Current Range: Medium** are sufficient to measure a resistor.
3. Click the **Output: Off** button in the lower-left corner of the screen to change the status to **Output: On**.
4. An oblique, angled line will appear in the middle of the screen. This straight line is the electrical "signature" of the resistor component. You can view the calculated value of the resistor in the information card right below the graph.
5. To terminate the test, press the **Output** button again to turn off the output or remove the resistor from the socket.

> 🖼️ **[IMAGE PLACEHOLDER - THIS BLOCK MUST BE COMPLETELY DELETED AFTER THE IMAGE IS ADDED]**
> **Image Description:** Screenshot of the first measurement screen in the software. A perfect oblique linear curve of a standard resistor must be displayed on the grid, and the result card underneath must show "RESISTOR" and its calculated value (e.g., 1.0 kΩ) with high confidence.
> **Filename Suggestion:** `first-measurement-resistor.png`
> **Usage Instructions:** After the image is placed here, this description box (placeholder) must be completely deleted.

In Section 9, the characteristic signatures of all other components on the screen will be examined in detail. For now, it has been observed how practically and quickly the system operates.

---

## Section C — Curve Tracer (V-I Analyzer)

### 7. Working Principle of Curve Testing

![Main window](images/shared/main-window.png)

In the software interface; the test parameters are located on the left side, the graph screen in the center, and the Comparison, Board Recording, and Board Testing tabs on the right edge.

In the curve test, the device applies a voltage in the form of an alternating (AC) sine wave to the measured component. During this time, it plots the amount of current passing through the component on the graph simultaneously against the applied voltage value.

* **Resistor:** Since current and voltage change completely simultaneously, a straight, angled line is formed on the screen.
* **Capacitor:** Since the current reaches its peak value before the voltage, an ellipse shape is drawn on the screen.
* **Diode:** Since it passes current in only one direction, a sharp break (knee) occurs on the screen.

Each component family draws a unique graph depending on its physical structure. This graph is of the nature of an identity card for that component. There are two independent probes in the device; these can be used individually or simultaneously (Synchronous Mode) as desired (details are in Section 11).

### 8. Basic Measurement Settings

The **Simple** view mode in the left panel offers the three basic settings most critical for measurements. In this mode, instead of complex technical numbers, clear level designations such as **Low, Medium-1, Medium-2, High** are preferred for ease of use. Both Voltage and Frequency parameters utilize these four levels.

The actual technical values corresponding to these levels are as follows:

| Level Name | Voltage (Peak Value) | Frequency |
| :--- | :---: | :---: |
| **Low** | 2.5 V | 10 Hz |
| **Medium-1** | 5 V | 50 Hz |
| **Medium-2** | 10 V | 100 Hz |
| **High** | 15 V | 1000 Hz |

* **Voltage:** The maximum (peak) voltage level applied to the component. When measuring a suspected component of unknown type, one must always start with the lowest level. If the line on the screen remains horizontal and flat, the voltage level must be increased step by step. Semiconductors, such as diode and transistor junctions, require a certain threshold voltage to enter conduction; passive components like resistors and capacitors do not look for such a threshold.
* **Frequency:** The most important parameter to distinguish frequency-sensitive (reactive) components like capacitors and inductors from resistors. The straight line drawn by the resistor is not affected by frequency changes. On the other hand, for example, a 100 nF capacitor appears as a thin and closed line at 10 Hz, whereas when the frequency is increased to 1000 Hz, it opens up to take the shape of a perfect ellipse. The fastest way to verify if the component is a capacitor is to observe the width of the ellipse on the screen by changing the frequency.
* **Current Range:** Determines with what level of current sensitivity the device will operate during measurement.

| Range | Ideal Area of Use |
| :--- | :--- |
| **Sensitive** | Capacitors, high-value resistors, and all sensitive components drawing very low current. |
| **Medium** | A safe starting point for unknown components. |
| **High** | Low-value resistors, conducting diodes, and robust parts drawing high current. |

*If the upper parts of the curve on the screen appear flattened (clipped) or if the software gives a signal limit warning, reduce the test voltage or switch to a higher (coarser) current range. Similarly, if a sensitive component drawing very little current is measured in the "High" current range, the curve on the screen may turn into a completely horizontal line, and the component may be mistaken for being defective (open circuit). In such suspicious cases, repeat the measurement by setting the current range to "Sensitive".*

### 9. Reading the Curve: Component Signatures Gallery

The result card right below the graph screen names the component detected by the device, calculates its value, and provides a confidence rate showing how certain it is of this detection. The 12 basic component examples listed below have been established in line with real electrical behaviors, and the expressions written on the result card are exactly the same as the texts you will see on the device screen.

⚠️ **Important Hardware Detail:** The KMY MMD-1 is a two-terminal (probe) curve tracer; therefore, it cannot software-identify three-terminal component classes such as "MOSFET" or "Transistor" on its own. You must know which two terminals of the three-terminal elements you are measuring. The device interprets the electrical behavior between those two contacted terminals. Thus, the transistor and MOSFET examples in the guide are explained based on "the behavior seen by the device" and the actual screen texts on the result card.

#### Resistor
A straight, angled line crossing the graph screen exactly in the middle. As the resistor value decreases, the line takes an angle close to vertical; as the resistor increases, the line flattens horizontally. When the frequency is changed, the angle of this line never changes. This is the clearest feature that distinguishes the resistor from all other components.

![Resistor curve](images/shared/curve-resistor.png)


#### Capacitor
Forms a clear ellipse on the screen. When the frequency is increased, the inside of the ellipse opens and becomes distinct, whereas when the frequency is decreased, it closes toward a thin line.

![Capacitor curve](images/shared/curve-capacitor.png)


#### Inductor
The exact mirror image of the capacitor. It also draws an ellipse, but its response is in the opposite direction: when the frequency is increased, the ellipse narrows, whereas when the frequency decreases, it widens.

![Inductor curve](images/shared/curve-inductor.png)


#### Capacitor + ESR (Equivalent Series Resistance)
The characteristic ellipse of a capacitor, but it stands slightly tilted to the right or left on the graph. The series resistance (ESR) here makes the ellipse angled. The capacitance value of the capacitor and the parallel/series resistance values are shown separately on the result card.

![Capacitor + ESR curve](images/shared/curve-capacitor-esr.png)


#### Diode
Forms a flat line in one direction (cut-off) and a distinct "knee" shape in the other direction (conduction). The position of this knee point on the voltage axis is the conduction threshold (forward voltage) of the diode. While this threshold is around 0.6 V - 0.7 V in silicon diodes, it is further to the left (at lower voltage) in Schottky diodes, and distinctly further to the right (at higher voltage) in LEDs.

![Diode curve](images/shared/curve-diode.png)


#### Zener Diode
Knee breaks are observed in both directions of the graph. The break on the right shows the normal conduction threshold of the diode, and the break on the left shows the zener breakdown voltage ($V_z$). Zener diodes up to 15 V can be easily analyzed with this device; for higher voltage zeners, the test voltage limit of the device will not be sufficient.

![Zener curve](images/shared/curve-zener.png)


#### TVS Diode
A uni-directional TVS diode exhibits electrically the exact same characteristics as a zener diode. The device also automatically classifies it as **ZENER** (there is no separate "TVS" label on the result card). The symmetric breakdown of bi-directional TVS diodes in both directions does not fit perfectly into any of the standard component classes. When measured, it may be reported as **|Z|** or **Undefined** on the card.

![Bidirectional TVS curve](images/shared/curve-tvs-bidirectional.png)


#### MOSFET — Gate-Source Terminals
The gate terminal of MOSFETs is like a very small capacitor insulated from the body, and almost no current passes through it. In small-signal MOSFETs, this capacitance value is so low (a few picofarads) that the flowing current remains below the detection limit of the device, and the card displays **OPEN CIRCUIT**. This is not a defect but the natural state of the gate. In more powerful power MOSFETs (with a capacitance of a few nanofarads), a thin **Capacitor** ellipse can be observed.

![MOSFET Gate-Source curve](images/shared/curve-mosfet-gs.png)


#### MOSFET — Drain-Source Terminals
Every MOSFET naturally has a body diode formed during production. When the gate is floating or connected to the Source, and you contact Drain-Source, a current is observed passing through this body diode rather than the channel. The device recognizes it directly as a standard **DIODE**; usually with a slightly higher $V_f$ compared to signal diodes.

![MOSFET Drain-Source curve](images/shared/curve-mosfet-ds.png)


#### Transistor — Base-Emitter Junction
The Base-Emitter junction is electrically a diode junction. The device writes **DIODE** on the screen, and the forward voltage ($V_f$) is typically measured between 0.65 V and 0.70 V.

![Transistor Base-Emitter curve](images/shared/curve-transistor-be.png)


#### Transistor — Base-Collector Junction
The Base-Collector junction is similarly a diode junction. However, because this junction is physically spread over a larger area, its threshold voltage generally turns out to be slightly lower than the Base-Emitter junction. **DIODE** is displayed on the result card.

![Transistor Base-Collector curve](images/shared/curve-transistor-bc.png)


#### Transistor — Collector-Emitter Terminals

![Transistor Collector-Emitter curve](images/shared/curve-transistor-ce.png)
If Collector-Emitter is measured without touching the Base, both internal junctions remain closed, and the device detects an **OPEN CIRCUIT**. This is not a defect but the natural state of the transistor; since base triggering is required for the transistor to conduct, it is normally expected to be in an insulating state under these test conditions.

*Important Design Note:* When measuring a component on a board without desoldering it, the curve observed is not the curve of that component alone; it is the sum of the electrical responses of all other paths and elements connected in parallel with it. In case of doubt, lifting a single pin of the component from the board with a soldering iron and repeating the measurement will provide the most reliable result.

### 10. Advanced Measurement Settings

![Advanced panel](images/shared/advanced-panel.png)

When switching to the **Advanced** view in the interface, the three parameters in the Simple panel are no longer step-based but can be controlled millimetrically with precise slider bars (Voltage 0.1 - 15 V, Frequency 1 - 1000 Hz). In this mode, the following advanced features are additionally offered to your control:

* **Waveform:** You can select Sine, Triangle, Square, Sawtooth, and DC wave types. The standard for curve analysis is always the sine wave. The DC option applies a constant voltage to the component.
* **Manual Bias:** Allows shifting the center point (offset) of the test signal above or below the zero level. For adjustment, instead of a classic scroll bar, direction buttons (arrow-pad) that provide continuous increase/decrease when held down are used. The step size can be set to 10 mV, 100 mV, or 1 V, and a one-click **Reset** button is available. It is disabled by default, and it is recommended to remain disabled for almost all standard tests.
* **Current Range:** Unlike the Simple mode, it can be adjusted completely independently for Probe 1 and Probe 2. If you are going to compare two probes with each other, you must equalize the current ranges of both probes; two curves in different ranges will never match, even if you are looking at the exact same components.

Most of the changes made are automatically transmitted to the device the moment you stop interacting with the adjustment dials or buttons. The **Apply** button is used to force the settings to be sent to the hardware immediately without waiting for this automatic period.

At the bottom of the left panel, there are three smart functions that facilitate measurements:

* **Auto-Detect:** When active, the device recognizes the type of component as soon as you touch it with the probe and automatically switches to the ideal voltage, frequency, and current range that shows that type best. To prevent erroneous transitions, the system does not change the settings without confirming the same result at least three times in succession. Thus, when your hand shakes, the screen settings do not jump back and forth continuously.
* **Auto-Optimize:** Performs a one-time ideal parameter search for the component currently on the probe when pressed; it applies the optimum settings if a meaningful result is found, and does not touch the settings if no useful result is obtained.
* **Sweep Mode:** Automatically sweeps through a selected range for one of the voltage, frequency, or current range parameters step-by-step until stopped; the other two parameters remain constant. If there is a component whose identity is unknown, starting a frequency sweep is an excellent method: if its curve changes with frequency, it is reactive (capacitor/inductor); if it does not change, it is resistive.

**Visibility Tab:**
* **Reference:** Overlays a previously recorded reference curve on top of the current live measurement as a template.
* **Equivalent Circuit:** Dynamically draws the simplified circuit diagram decided by the device under the result card.
* **Freeze:** Freezes the current curve on the screen as it is for examination.

### 11. Dual Probe Usage and Synchronous Mode

Normally, the **Probe 1** and **Probe 2** modes drive a single probe at a time. **Synchronous** mode drives both from the same source at the same time. This is the practical way to compare two components side-by-side in a single run.

When operating in synchronous mode, the device continuously monitors the electrical load balance on both probes and displays yellow warning windows on the screen if an imbalance is detected:

* *“The loads on the probes are very different; reading sensitivity may drift in synchronous mode. Use single probe mode for precise measurements.”*
* *“P1 terminal is floating; P2 reading may drift by ~1% during synchronous measurement.”* *(The symmetric warning appears for P1 when P2 is floating.)*

Seeing these warnings does not mean the measurement is completely incorrect. It only reminds you that when the load difference on the two probes is very high, the reading in synchronous mode may drift slightly due to its nature. For comparisons requiring millimetric precision, switching to single probe mode (Probe 1 or Probe 2) is the safest approach.

---

## Section D — Comparison Mode and Board Testing

### 12. Comparison Functions

![Comparison panel](images/shared/compare-panel.png)

The **Comparison** tab on the right edge opens a practical side drawer. Three modes are available:

* **Off:** Disables the comparison mode.
* **Live ↔ Reference:** Compares the active component currently touched by the probe with a reference curve captured earlier. Clicking the **Capture Reference** button saves the curve on the screen as a benchmark; you can save it to a file and reload it later.
* **Probe 1 ↔ Probe 2:** Compares the two probes directly with each other. You connect the component known to be good as a reference to one probe, and the suspected component to the other. This method is much safer because both measurements are made at the exact same time, at the same temperature, and under identical electrical conditions.

The decision is a similarity percentage based on a threshold you define. If the similarity is above the threshold, **MATCHED** (green) is displayed; if below, **MISMATCHED** (red) appears. The factory threshold is 90%. The **Critical Region Sensitivity** (Off, Normal, High) option tightens the comparison in the bending and knee regions of the curve, as the true electrical identity of the component is primarily hidden there.

If neither probe is drawing measurable current, the device does not falsely declare "matched" by comparing the floating noise. Instead, it writes **NO MEASUREMENT**. This warning indicates that either the probe is not making contact or the range is selected too coarse (high) for that component.

By turning on the **Acoustic Warning** feature, you do not need to keep your eyes on the screen; the system will emit an acoustic signal only when the match decision (pass/fail) changes.

### 13. Board Recording and Board Testing System

This is the most ideal method for testing specific board models that you will repair or verify repeatedly: record each test point once, and then rapidly scan all suspected boards against this reference database.

#### Step-by-Step Recording of a Board Reference:

![Board recording interface](images/shared/board-record-interface.png)
1. **Create a Project Folder:** Select a working folder for yourself. The image of the board and all test points are kept in this single folder; you can copy and carry the folder as a whole to another computer.
2. **Add a Board Image:** Upload a clear, shadowless photograph of the board taken from directly above. A photo taken under flat, uniform lighting makes it easier to position the test points accurately on the image.
3. **Define Points:** Touch the test probe to the targeted point on the physical board. At the same time, click on that location on the board photo on the software screen. Give the point a descriptive name (it is recommended to use the board's own markings: R14, C7, U3-1) and click **Save Point**.
4. **Arrange the Sequence:** You can arrange the saved points in the desired test order by dragging and dropping them practically.

* **Multi-Stage Signature:** When active, each test point is recorded not at a single setting, but at 3-4 different voltage and frequency levels. The recording process takes slightly longer, but it is much more difficult for a faulty component to bypass a point recorded this way.

#### Testing a Recorded Board:
Click the **Start Test** button and visit the points in sequence. Each point is measured, compared with its reference, and marked as passed or failed. Mismatched points appear in **red** on the board photograph. Instead of a tedious text list, you obtain a visual map of the fault. You can pause and skip points, and after finishing, use the **Test Remaining** option to return only to the incomplete ones.

![Board test interface](images/shared/board-test-interface.png)


* **Auto Mode:** Automatically proceeds to the next point when the point match is successful. Enable this when you want to look at the board rather than the screen while holding the probes.
* **Create Excel Report:** When the test is finished, clicking this button generates a detailed three-page Excel report: point-by-point details, a summary table, and a visual pass/fail map of the board.

---

## Section E — Other Auxiliary Tools

### 14. Oscilloscope Mode

When switching to the oscilloscope mode, the signal output of the device is completely turned off, and the probes enter a passive listening mode to monitor external signals. The input channels can safely measure **up to 50 V**.

🎨 **Important Note on Channel Color Scheme:** On the oscilloscope screen, Channel 1 is represented by **yellow**, and Channel 2 is represented by **cyan**. This color scheme is the exact opposite of Probe 1 (cyan) and Probe 2 (yellow) in the Curve Tracer screen. The colors of the two modes are deliberately designed to be different so that they are not confused; do not be surprised by this color difference when transitioning between modes.

The device always samples at **5.5 kS/s** (5500 samples per second) due to hardware limits. Changing the timebase in the program does not alter this sampling rate; it only changes the time window displayed on the screen. The practical result of this is that the KMY MMD-1 is a **low-frequency oscilloscope**. It works perfectly for power supply ripples, motor drives, and signals below the audio band, but above 1 kHz, the shape accuracy of the wave will start to become unreliable.

![Oscilloscope mode](images/shared/oscilloscope-mode.png)


* **AUTO:** Analyzes the incoming signal and automatically sets the timebase, vertical voltage scale, and trigger level for you. If no meaningful signal is detected, it does not touch the settings.
* **Trigger Modes:**
  * *Auto:* Refreshes the screen continuously even if no trigger condition is met.
  * *Normal:* Refreshes the screen only when the specified trigger condition occurs.
  * *Single:* Captures the signal once when the trigger condition is met and freezes the screen.

The baseline arrows and the trigger level arrow on the screen edges can be directly dragged with the mouse. This is the fastest way to make quick adjustments without typing values into number boxes. The **Inspect** button allows pausing the live stream and navigating through the **last 20 seconds of recorded history**. Since recording continues in the background while you are looking at the live screen, the event is still captured when you notice a sudden fluctuation.

Four measurements come ready on the lower information bar: **Vpp** (peak-to-peak voltage), **Avg** (average voltage), **Vrms** (effective voltage), and **Frequency**. There are 11 measurement parameters in total in the database; you can add or remove any parameters you wish to this bar.

### 15. Multimeter Mode

In this mode, both probes can read voltage independently at the same time. There are no manual range or function (AC/DC) selection buttons. The KMY MMD-1 analyzes the incoming signal to decide whether it should be measured as DC or AC.

* **REL (Relative Measurement):** Accepts the currently read value as zero reference and shows subsequent changes relative to this value (+/-).
* **MIN/MAX:** Accumulates the lowest and highest voltage values read since the beginning of the measurement and lists them on the screen.
* **HOLD:** Freezes the current measurement value on the screen.

In this mode as well, the active test signal output is completely turned off. Do not forget to keep the channel of the probe you want to measure open. If the probe of a closed channel is left floating in the air, the value read on the screen is not a real voltage, but electromagnetic noise collected by the cable.

---

## Section F — System Settings, Calibration, and Connection

### 16. System Settings

![Settings](images/shared/settings-device.png)

Clicking on the gear icon in the top bar opens the general settings panel. It consists of two basic tabs: **Device** and **Calibration**. Both tabs feature a quick language selection option (Turkish / English) at the top.

#### Device Tab Content:
This section contains the software version, unique device number, Wi-Fi connection setup tools, and an integrated **Update** button. The Update button checks and updates both the computer software and the device firmware with a single click.

Additionally, under the "Service / Diagnostics" heading, there is an emergency tool that allows restoring the device to a stable older firmware version in case of a problem during a new firmware update. This is not an area that needs to be accessed during daily use; it is a special area used only in technical support situations.

### 17. Calibration Wizard

![Calibration intro](images/shared/calibration-intro.png)

The calibration data of the KMY MMD-1 is stored **directly in the device's own internal non-volatile memory (EEPROM/Flash)**, not on the computer. The software reads this calibration table from the device itself at every startup. In this way, no matter which computer or phone you plug the device into, you can continue to use it directly in its calibrated state without needing to recalibrate.

#### Requirements for Calibration:
* Two standard resistors of known value (preferably 1% or better tolerance, **between 300 Ω and 1000 Ω**; one for each probe, both must remain connected simultaneously throughout the calibration process).
* A digital multimeter capable of making precise measurements.
* The calibration process takes **approximately 15 minutes** and proceeds through 5 basic stages.

#### Step-by-Step Calibration Stages:
1. **Open Circuit (Approx. 30 sec):** Both probe tips must be completely floating and must not touch anything. In this stage, the zero points of the current channels and the oscilloscope baseline are calibrated.
2. **P1 Resistor Measurement:** *“Connect a known resistor to BOTH probes; in this step, only Probe 1 will be measured.”* Both resistors remain plugged into their slots, but the device only analyzes the Probe 1 side. When the measurement is finished, enter the **real resistance value** measured with your multimeter on the screen, rather than reading the color codes on the resistor.
3. **P2 Resistor Measurement:** *“Keep both resistors CONNECTED.”* The same two resistors remain in place; this time Probe 2 is measured. 

The first three stages of calibration are followed by a single confirmation window: **Save and Continue**. Writing to flash is combined here.

4. **Voltage Reading (Multimeter):** Remove the probes from their slots and leave them completely floating. The device will output test voltages of $-12	ext{ V}$, $-5	ext{ V}$, $+5	ext{ V}$, and $+12	ext{ V}$ in sequence. At each level, physically measure the voltage at the Probe 1 terminal with your external multimeter and enter the read value into the software.
5. **Output (DAC) DC Calibration (Approx. 45 sec):** The device automatically sweeps through the range $-15	ext{ V}$ to $+15	ext{ V}$ in steps of 1 V and corrects itself based on the voltage measurements entered in the previous step. Immediately following this step, while the probes are still floating, the device automatically measures and corrects the AC driving amplitude and center offset. No extra action is required from you; the process only takes a little longer.

* **Optional 6th Stage (Oscilloscope Calibration):** At the end of the steps, an additional stage is offered for fine-tuning the oscilloscope readings. Since the device cannot drive its own output in oscilloscope mode, you are asked to use an external voltage/signal source of known accuracy. If you do not have such a source, you can safely skip this step; everything else besides the oscilloscope will remain fully calibrated.

*Software Features:* Each confirmation screen allows you to repeat the previous stage if you think you made an error. In the first three stages, if there is already a valid calibration on the device, you can choose to skip that stage and keep previous values. The writing process to the device's flash is deferred until all steps are successfully completed. If you close the wizard halfway through, the old calibration data on the device remains untouched.

*How Often Should Calibration Be Performed?* It is recommended to renew the calibration when you notice that your measurement values deviate visibly from a trusted external multimeter, or when the software reports that the reference baseline has drifted. Otherwise, you do not need to touch the calibration menu under normal operating conditions.

### 18. Wireless Usage and Wi-Fi Setup

![Wi-Fi setup](images/shared/wifi-setup.png)

The KMY MMD-1 supports wireless network connection in two different modes:

1. **Station Mode:** If there is an active Wi-Fi network in your workshop, the device joins this network. Thus, your computer or phone can access the device over the existing network.
2. **Access Point (AP) Mode:** If you are working in the field or if there is no Wi-Fi network in the environment, the device broadcasts its own wireless network. You can connect your computer or phone directly to the device.

#### Wi-Fi Setup via the Application:
While the device is connected via USB, open the **Settings → Wi-Fi Setup** menu, select the desired connection mode, enter the network name (SSID) and password, and send them to the device.

#### Wi-Fi Setup via Browser (Web Interface):
Disconnect the USB cable. Out of the box, the KMY MMD-1 broadcasts an unsecured wireless network named **KMY MMD-1**. When you connect your phone or laptop to this network, the setup page will open automatically; if it does not open, type **192.168.4.1** into your browser's address bar. Advanced network configuration options, such as static IP definition, are only located in this web interface.

#### If the Device is Not Displayed in the List (Manual Connection):
If you are sure that the device is connected to the network but you cannot see it in the software list, you can click on the small **"Enter device address manually"** icon next to the Wi-Fi selector and write its IP address manually. This may be necessary because discovery relies on a broadcast packet sent by the device once every second, and some routers do not forward these broadcast packets to wireless clients. You can learn the IP address from the connected devices list of your router or from the device's own web setup page. The same manual IP entry option is also available under the connection screen in the Android mobile application.

*Important Details to Know:*
* The KMY MMD-1 hardware supports only a single active connection at a time; a device currently in use appears as **BUSY** in the list.
* The **Reset Network Settings** option restores the wireless network configuration to the factory default state at any time.

### 19. Usage on Mobile Devices (Phone/Tablet)

The exact same application used in Windows runs on Android, with no functional deficiency in terms of measurement and analysis. The layout is optimized for narrow mobile screens: there are thin bars that are always visible at the top and bottom of the graph area.

![Mobile interface](images/shared/mobile-interface.png)


* **Pulling Down the Top Status Bar:** Pulling down this bar opens the status panel. It contains the connection status, error or lock reason (if any), and three boxes: **Tools**, **Settings**, and **Connect/Disconnect**. When there is an important warning or error, this panel opens automatically.
* **Pulling Up the Bottom Control Bar:** Pulling up this bar opens the full control panel. It stops at the height you leave your finger; it does not have to be fully open or closed. It contains the exact same settings as the desktop version. The bar always displays the Curve Test, Oscilloscope, Multimeter transition buttons, and (while in Curve Test) the Voltage, Frequency, and Current Range shortcuts.
* **Accessing Functions:** You reach **Comparison, Board Recording, and Board Testing** from the *Tools* box. You reach **General Settings and Calibration** from the *Settings* box. Both are identical to the windows on the desktop, only scaled down for the screen.
* **Connection Panel:** The *Connect* box offers a discovery list, a backup button that tries to connect directly to the device's own network, and a manual IP entry field.

*Mobile Firmware Update Limitation:* The device firmware cannot be updated via mobile devices because writing requires a secure USB protocol and direct USB connection is not supported on mobile. However, updates for the mobile application itself are installed on the phone: when you click **Update**, the application downloads the new version, verifies its signature, and opens Android's own installation screen. The installation is completed with a single confirmation touch, without needing a browser.

### 20. Software Updates

Following **Settings → Update** checks both the application and the device firmware, and installs whatever is outdated. Your calibration data remains untouched.

At the beginning of the update installation, you will see the following on the screen: *“Installation is starting, the application will now close and reopen with the new version.”* It is normal for the window to close suddenly and reopen after a few seconds; this is not a crash.

*Update Details:*
* Application updates work whether the device is plugged in or not.
* Device firmware can only be written via physical **USB connection**. It cannot be written over the network or from a phone; it is included with the installation of the desktop application.
* If there is no internet connection, the update check will inform the user; nothing in the existing running setup is lost or corrupted.

---

## Section G — Reference Information

### 21. Technical Limits and Parameters

| Parameter | Technical Limit and Value |
| :--- | :--- |
| **Test Voltage** | $\pm 15	ext{ V}$ Peak |
| **Test Frequency** | $1	ext{ Hz} - 1000	ext{ Hz}$ |
| **Oscilloscope / Voltmeter Input Limit** | Maximum $50	ext{ V}$ |
| **Oscilloscope Sampling Rate** | $5.5	ext{ kS/s}$ (Hardware fixed) |
| **Oscilloscope Record Depth** | Last $20	ext{ seconds}$ continuous |
| **Power Supply** | Through the USB port |

* **Basic Safety and Operating Rules:**
  * Test boards while their power is disconnected and capacitors are fully discharged.
  * The KMY MMD-1 drives a signal only in the **Curve Test** mode. In the Oscilloscope and Multimeter modes, the output is turned off, and the probes only listen.
  * The red **Emergency Stop** button cuts off the output immediately. It always works as long as the device is connected to the computer, even when there is no calibration.
  * The output is not activated until the device finishes its startup routine and verifies that there is a registered calibration inside.
  * ⚠️ **Important Mains Warning:** None of the hardware here is designed to operate under mains voltage ($220	ext{ V AC}$). Never touch the probes to mains outlets or high-voltage lines.

### 22. Troubleshooting and Solutions

* **The device is not displayed in the list:**
  Check the physical USB cable and your computer's USB port. If it is on the network and still does not appear, try the [Manual IP Entry](#18-wireless-usage-and-wi-fi-setup) method.
* **Controls are locked immediately after connecting:**
  This is not an error. The device performs startup self-calibration to balance the internal hardware. It takes approximately 13-15 seconds and opens automatically.
* **Output cannot be activated (Output does not turn on):**
  The device is either still starting up or there is no calibration saved inside. Open **Settings → Calibration** to check the status.
* **The curve is flat and horizontal:**
  The probes are not touching anything (open circuit) or the test voltage does not reach the conduction threshold of the semiconductor component. Increase the voltage level or switch to a more sensitive current range.
* **A yellow warning bar appears on the screen in synchronous mode:**
  The loads on the probes are very different or one is floating. Switch to single probe mode for precise measurements (details in Section 11).
* **Comparison screen continuously displays "NO MEASUREMENT":**
  No probe is drawing measurable current. Check probe contact, and switch to the **Sensitive** range for high-impedance parts.
* **The device appears as "BUSY" in the status list:**
  Another connection is using the device, either a phone or another computer. Close the application on the other device first.
* **Measurement values and graphs appear drifted:**
  Turn the device off and on; startup self-calibration resolves most drifts. If the application reports that the reference baseline has drifted, perform calibration again.
* **Waveform appears distorted or broken in oscilloscope mode:**
  Check the frequency of the input signal. With a sampling rate of 5.5 kS/s, you cannot reliably view the wave shape of a signal above 1 kHz.
* **The mobile application cannot find the device on the wireless network:**
  Ensure that your phone and the device are connected to the same Wi-Fi network. If the device is broadcasting its own network (Access Point mode), confirm that your phone is connected directly to the **KMY MMD-1** network.

### 23. Technical Support and Contact

For all technical questions, requests, and support regarding the KMY MMD-1, you can visit our official GitHub page or contact us via email:

* **Official GitHub Page:** [https://github.com/kmyelectronicseu-png/kmy-mmd1](https://github.com/kmyelectronicseu-png/kmy-mmd1)
* **Direct E-mail Support:** [kmyelectronics.eu@gmail.com](mailto:kmyelectronics.eu@gmail.com)

To facilitate a rapid solution, noting your device number before contacting the support team will help us greatly. You can find your device number by following **Settings → Device → Device No.** in the software interface.