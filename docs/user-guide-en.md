# KMY MMD-1 — User Guide

**Multifunctional Measurement Device**

Three instruments in one box: a curve tracer that identifies components by the
shape of their voltage–current curve, a two-channel oscilloscope, and a
two-channel voltmeter. It connects to a Windows PC over USB, or over Wi-Fi once
you have set the network up.

> Türkçe sürüm: [user-guide-tr.md](user-guide-tr.md)

---

## Contents

1. [What you need](#1-what-you-need)
2. [Installing the software](#2-installing-the-software)
3. [First connection](#3-first-connection)
4. [The main window](#4-the-main-window)
5. [Curve Test](#5-curve-test)
6. [Comparing](#6-comparing)
7. [Board Record and Board Test](#7-board-record-and-board-test)
8. [Oscilloscope](#8-oscilloscope)
9. [Multimeter](#9-multimeter)
10. [Settings](#10-settings)
11. [Calibration](#11-calibration)
12. [Using it over Wi-Fi](#12-using-it-over-wi-fi)
13. [Updates](#13-updates)
14. [Safety and limits](#14-safety-and-limits)
15. [If something goes wrong](#15-if-something-goes-wrong)

---

## 1. What you need

- The KMY MMD-1 and its USB cable.
- A PC running 64-bit Windows 10 or 11.
- Nothing else. The device is powered from the USB port, and the software
  installs without administrator rights.

**Before you touch anything with the probes:** the circuit under test must be
switched off and its capacitors discharged. The instrument drives its own test
signal into whatever the probes touch, and a live circuit fighting that signal
damages both sides.

---

## 2. Installing the software

1. Open the releases page:
   <https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest>
2. Download **KMY-MMD-1-Kurulum.exe**.
3. Run it. The first screen asks which language you want the installer in —
   this only affects the installer; the application has its own language
   setting you can change at any time.
4. Follow the wizard. It installs into your own user folder, so Windows does
   not ask for an administrator password.

The `.imza` file next to the installer is its signature. The application uses
it to verify updates it downloads later; you do not need to do anything with it.

Everything the device needs — including its firmware — comes inside this one
installer. There is nothing else to download.

---

## 3. First connection

Plug the USB cable in and start **KMY MMD-1**.

The device appears in the list at the top of the window. Press **Connect**.

The first thing the device does after power-up is calibrate itself against its
internal voltage references. This takes about fifteen seconds, and the controls
stay locked until it finishes — that is normal, and waiting is all you have to
do. The dot next to the connection state turns green when the device is ready.

---

## 4. The main window

![Main window](images/en/01_curve_tracer.png)

| # | What it is |
|---|---|
| 1 | Connection state and the Connect / Disconnect button. |
| 2 | The three instruments: Curve Test, Oscilloscope, Multimeter. |
| 3 | Settings — language, Wi-Fi, updates, calibration. |
| 4 | Simple / Advanced. Simple shows the three settings that matter most; Advanced opens the rest. |
| 5 | Test settings: the peak voltage applied to the component, the frequency, and the current range. |
| 6 | Which probe is driven: Probe 1, Probe 2, or both at once. |
| 7 | What the graph plots: the V-I curve, voltage over time, current over time, or both stacked. |
| 8 | The graph. Axes scale themselves to whatever is being measured. |
| 9 | The output switch, and the red emergency stop next to it. |
| 10 | Compare, Board Record and Board Test — press one to open it. |
| 11 | The result: what the device thinks the component is, with its values. |

The emergency stop (next to 9) cuts the output and releases every range
immediately. Use it whenever something does not look right.

---

## 5. Curve Test

This is the main instrument. It applies a small alternating voltage to the
component and plots the current that flows against the voltage that caused it.
Every component family draws a different shape, and that shape is what
identifies it.

### The three settings that matter

**Voltage** — the peak of the test signal. Start low with an unknown component
and raise it only if the curve stays flat. Diodes and transistor junctions need
enough voltage to reach their forward threshold; capacitors and resistors do
not.

**Frequency** — capacitors and inductors behave differently at different
frequencies, so this is what separates them from resistors. A resistor's curve
does not change with frequency; a capacitor's opens into a wider ellipse as the
frequency rises.

**Current range** — how much current the instrument is prepared to see.

| Range | Use it for |
|---|---|
| Fine | Capacitors, large resistors, anything drawing very little current. |
| Medium | A good starting point for most components. |
| Coarse | Small resistors, diodes in conduction, anything drawing a lot. |

If the curve looks clipped, or the app warns that the signal is at the limit,
lower the voltage or move to a coarser range.

### Reading the curve

- **A straight line through the middle** — a resistor. The steeper it is, the
  lower the resistance.
- **A flat line along the horizontal axis** — an open circuit, or nothing
  touching the probes.
- **A vertical line** — a short circuit.
- **An ellipse** — a capacitor. The wider it opens, the larger the value.
- **A knee** — a diode or a junction. Where the knee sits is the forward
  threshold.

The result card under the graph names what it found, gives the value, and shows
how confident it is. **Equivalent Circuit** draws the circuit it settled on.

### Advanced controls

![Advanced panel](images/en/02_advanced.png)

| # | What it is |
|---|---|
| 1 | Waveform. Sine is the standard for curve testing; DC applies a steady voltage. |
| 2 | Peak voltage, as a slider and a number. |
| 3 | Frequency, with quick steps and a slider. |
| 4 | Manual bias — moves the centre of the signal off zero. Off by default, and off is right for almost everything. |
| 5 | Current range per probe, so the two probes can be set differently. |
| 6 | Apply. Appears when changes are waiting to be sent to the device. |

### Auto detect and Auto Optimize

**Automatic** (in the Simple panel) watches the probes. Touch a component and
the instrument recognises what it is and switches to the voltage, frequency and
range that measure it best. It is the quickest way to work through a tray of
unknown parts.

**Auto Optimize** does the same search on demand for the component already on
the probes.

### Sweep

**Sweep mode** walks one axis — voltage, frequency, or current range — step by
step and loops until you stop it. The other two settings stay where they are.
It is useful when you want to see how a component's curve changes rather than
read a single value.

### Two probes

**Probe 1** and **Probe 2** drive one probe at a time. **Synced** drives both
from the same source at the same range, which is how you compare two components
in one pass.

---

## 6. Comparing

![Compare](images/en/03_compare.png)

| # | What it is |
|---|---|
| 1 | Opens the Compare drawer. |
| 2 | Off, Live ↔ Reference, or Probe 1 ↔ Probe 2. |
| 3 | Which probe the reference is captured from. |
| 4 | Capture Reference — stores the curve on screen as the one to match against. |
| 5 | Save the reference to a file, load one back, or delete it. |

**Live ↔ Reference** compares whatever the probes are touching now against a
curve you captured earlier. **Probe 1 ↔ Probe 2** compares the two probes
against each other — put a known-good part on one and the suspect part on the
other.

The verdict is a similarity percentage against a threshold you set. Above the
threshold reads **MATCH**, below it reads **NO MATCH**.

Two things worth knowing:

- **Turn the audible alert on** and you can keep your eyes on the board instead
  of the screen. It beeps when the verdict changes, not continuously.
- If neither probe is drawing measurable current — nothing is touching them, or
  the range is far too coarse for the part — the app says so rather than
  declaring a match. Two pieces of noise are not "the same"; they are simply
  not a measurement.

**Critical-region sensitivity** makes the comparison stricter in the knee
regions of the curve, where a component's identity really lives. Raise it when
you are chasing subtle differences between parts that look alike.

---

## 7. Board Record and Board Test

This is how you test a board you will see again: record every test point once,
then check a suspect board against that record.

![Board Record](images/en/08_board_record.png)

| # | What it is |
|---|---|
| 1 | Switches between recording and testing. |
| 2 | Back to the ordinary measuring screen. |
| 3 | Choose the project folder. Everything about one board — its photo and all its test points — lives in one folder. |

### Recording a board

1. Pick a project folder and give the board a name.
2. Add a photo of the board.
3. Touch the probe to a test point, tap that spot on the photo, name the point,
   and press **Record Point**. The curve at that moment becomes the point's
   reference.
4. Work your way around the board. Marker size and shape can be set per point,
   so dense pin rows stay readable.

**Multi-stage signature** records each point at several voltage and frequency
settings instead of one. It takes longer, but a point recorded this way is much
harder to fool: two components that look identical at one setting rarely look
identical at all of them.

### Testing a board

![Board Test](images/en/09_board_test.png)

Open **Board Test**, press **Start test**, and work through the points in
order. Each one is measured, compared against its reference, and marked passed
or failed. Failing points show up in red on the board photo, so you get a map
of the fault rather than a list.

You can pause, skip a point you cannot reach, or finish early. Skipped points
are counted separately — they are neither passed nor failed, and the summary
says so plainly.

**Auto mode** moves on by itself once a point matches, so you can hold the
probe and watch the board instead of the screen.

When you are done, **Create Excel Report** writes the whole run out — points,
settings, similarities and verdicts.

---

## 8. Oscilloscope

![Oscilloscope](images/en/04_scope.png)

| # | What it is |
|---|---|
| 1 | Run/stop, single shot, and AUTO. |
| 2 | Timebase and the sample rate in use. |
| 3 | Waveform, FFT or XY view. |
| 4 | Export the screen as PNG and the visible data as CSV. |
| 5 | Live or Review, with the buttons to move through the recording. |
| 6 | The display. |
| 7 | Channel settings: vertical scale, position, AC/DC coupling, probe factor, invert. |
| 8 | Trigger: source, edge, mode, level and position. |
| 9 | Measurement cursors. |
| 10 | Live measurements taken from the trace. |

The signal output is **off** in oscilloscope mode — the probes only listen. The
input handles up to 50 V.

**AUTO** is the fastest way to get a signal on screen: it looks at what is
coming in and sets the timebase, the vertical scale and the trigger level for
you.

**Review** stops the stream and lets you move back and forth through the last
twenty seconds and zoom in. The recording keeps running while you are live, so
whatever just happened is still there when you go looking for it.

With one channel switched off, the device puts all its sampling into the other
one and the trace comes out noticeably cleaner. Turn off the channel you are
not using.

---

## 9. Multimeter

![Multimeter](images/en/05_multimeter.png)

| # | What it is |
|---|---|
| 1 | REL, MIN/MAX and HOLD. |
| 2 | Probe 1 reading. |
| 3 | Probe 2 reading. |
| 4 | Where the reading sits within the range. |
| 5 | Which calibration the readings are using. |

Both probes read voltage at once, and DC or AC is chosen automatically — there
is no range switch to get wrong.

- **REL** takes the present reading as zero, so you can measure a difference.
- **MIN/MAX** keeps the lowest and highest reading it has seen.
- **HOLD** freezes the display.

The output is off in this mode as well. Leave the probe you are measuring with
switched on: a switched-off probe with its tip in the air reads noise, not a
voltage.

---

## 10. Settings

![Settings](images/en/06_settings_device.png)

| # | What it is |
|---|---|
| 1 | Language — Turkish or English. It changes immediately and is remembered. |
| 2 | Device and Calibration tabs. |
| 3 | Device identity: firmware version, serial number, calibration state, Wi-Fi module state. |
| 4 | Wi-Fi setup. |
| 5 | Update — checks the application and the device firmware together. |
| 6 | About: which versions you are running. |

The **Wi-Fi module** line is worth a glance. While the device is on USB the
module should read *asleep* — a Wi-Fi radio transmitting next to the analogue
front end disturbs its voltage references, so the device puts it to sleep on
purpose. Over a network connection it is of course awake.

---

## 11. Calibration

![Calibration](images/en/07_settings_cal.png)

| # | What it is |
|---|---|
| 1 | Language. |
| 2 | Calibration status, where it was read from, and how many points it holds. |
| 3 | Start Calibration. |

Calibration is stored **inside the device**, not on the PC, so it travels with
the instrument: move it to another computer and it stays calibrated.

The wizard runs in five stages and takes a few minutes:

1. **Open circuit** — both probes touching nothing. Measures the current-channel
   zeros and the oscilloscope baseline.
2. **Probe 1 shorted** — its two leads joined.
3. **Probe 2 shorted**.
4. **Read calibration** — the device drives a series of DC levels, you measure
   each one with your own multimeter and type the value in. This is what ties
   the instrument's readings to a reference you trust.
5. **Output calibration** — the device sweeps its output from −15 V to +15 V
   and corrects itself using its now-calibrated reading.

An optional sixth stage calibrates the oscilloscope reading against an external
source.

**You will need:** a lead to short the probes, and a multimeter you trust. The
accuracy of that multimeter becomes the accuracy of the instrument, so use a
good one.

Every confirmation screen lets you repeat the stage before it, so a mistake
does not mean starting over. If you cancel or close the wizard part way, the
device keeps the calibration it already had — nothing is written until the run
finishes.

---

## 12. Using it over Wi-Fi

The device can either join your existing network or broadcast its own.

**To set it up**, connect over USB first, open **Settings → Wi-Fi Setup**,
enter the network name and password, and send it. The device joins the network
and the app confirms the setup by finding it there.

**Straight out of the box** the device broadcasts an open network called
**KMY MMD-1**. Connect a phone or a laptop to it and the setup page opens by
itself; if it does not, type `192.168.4.1` into the browser. Advanced settings
such as a static IP address live on that page.

Once the device is on a network, switch the app to **Wi-Fi** and press
**Connect** — devices on the same network are found automatically.

One device serves one connection at a time. A device already in use shows as
**BUSY**.

---

## 13. Updates

**Settings → Update** checks the application and the device firmware together
and installs whatever is out of date. Your calibration is not touched.

- The application update works whether or not the device is plugged in.
- The device firmware needs a USB connection.
- Without an internet connection the check simply says so; nothing breaks.

When there is an update you will be asked once, with the option not to be asked
about that particular version again. A newer version will still ask.

**Do not unplug the USB cable while device firmware is being written.**

---

## 14. Safety and limits

| | |
|---|---|
| Test voltage | ±15 V peak |
| Oscilloscope / voltmeter input | up to 50 V |
| Power | from the USB port |

- **Test the board with its power off** and its capacitors discharged.
- The instrument drives its own signal in Curve Test mode. In Oscilloscope and
  Multimeter modes the output is off and the probes only listen.
- The red emergency stop cuts the output and releases every range at once.
- Nothing here is rated for mains voltage. Do not put the probes on mains.

---

## 15. If something goes wrong

**The device does not appear in the list.**
Check the cable and try a different USB port. Windows needs a USB-serial driver
for the adapter; most systems already have one.

**The controls are locked just after connecting.**
The device is running its start-up self-calibration. It takes about fifteen
seconds and unlocks by itself.

**The output switch will not turn on.**
The device is either still starting up, or it has no calibration stored. Open
Settings → Calibration and check the status.

**The curve is flat.**
Nothing is touching the probes, the component is open, or the voltage is too
low to reach its threshold. Raise the voltage a step, or move to a finer
current range.

**The comparison keeps saying there is no measurement.**
Neither probe is drawing measurable current. Check the probe contact, and move
to a finer current range for a high-impedance part.

**The device shows BUSY.**
Another connection has it — a phone, or another PC. Close that one first.

**The readings look shifted.**
Power the device off and on. If the app reports that the reference baseline has
drifted from where it was at calibration time, run the calibration again.

---

## Support

KMY Electronics — <https://github.com/kmyelectronicseu-png/kmy-mmd1>

When you get in touch, the device serial number helps: **Settings → Device →
Device no.**
