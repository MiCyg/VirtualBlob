# Virtual Blob
![Work in Progress](https://img.shields.io/badge/status-in--progress-orange)

Welcome to **VirtualBlob** – a small interactive creature brought to life on an LED matrix. The device contains an LED matrix, a light sensor, and an accelerometer. Its purpose is to display a small creature that reacts to external motion. The project aims to realistically simulate the creature's behavior both physically and in terms of interactivity.

This project is an natural consequence of [Adafriend](https://learn.adafruit.com/adafriend/overview), which I also built, with some minor modifications, but not well documented. Learning from that experience, I have now tried to document the project thoroughly so that it can be reproduced without issues. If you notice any inconsistencies or have questions, feel free to contact me.

<p align="center">
	<img src="images/VB_dark.jpg" alt="PoVirtualBlob Demo" width="75%" />
</p>

---

## What is VirtualBlob?

VirtualBlob is a playful, educational project. It contains:
- **8x8 LED matrix** displaying the creature
- **Light sensors** to detect surroundings
- **Accelerometer** to sense movement and tilting
- **Touch sensor** to user communicate
- **Buzzer** to user communicate

The blob is a soft solid simulation with boundaries on all edges. It reacts to motion: if tilted, it will crawl toward the nearest edge. The goal is to simulate both physical and behavioral responses realistically.

<p align="center">
	<img src="images/VB_wee.gif" alt="Pomodoro test" width="45%" />
	<img src="images/VB_rotating.gif" alt="Break test" width="45%" />
</p>

---

## Project Structure

The project is organized into three modules, each as a **Git submodule**:

- `Mechanical` – Enclosure and structural design  
- `Hardware` – PCBs, sensors, and electronics  
- `Software` – Blob simulation, LED control, and sensor management  

Clone everything at once:
```bash
git clone --recursive https://github.com/MiCyg/VirtualBlob.git
```

If already cloned without --recursive, initialize submodules:
```bash
git submodule update --init --recursive
```

# Contributing

Make changes in the respective module repository. Update the submodule pointer in the main repo after changes:

```bash
git add software hardware mechanical
git commit -m "Update submodules"
git push
```
