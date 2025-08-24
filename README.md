# ⏱️ Digital Interval Timer (Pomodoro Timer)

A digital Pomodoro-style timer built in **Logisim Evolution**.  
This project allows you to set custom **work** and **rest intervals** using multiplexers and flip-flops. Once the work timer completes, the rest timer automatically begins, making it perfect for focused study or productivity sessions.  

---

## 🔧 Features  
- ✅ Set **work** and **rest** times manually (minutes & seconds) using binary inputs  
- 🔄 Automatic switching between **Work Mode** and **Rest Mode**  
- 🟢 **Comparator logic** detects when the timer reaches `00:00` and switches phases  
- 🔲 **Reset** and **Set** functionality with **SR latch** control  
- ⚡ Built entirely in **Logisim Evolution** using counters, flip-flops, and multiplexers  

---

## 🧩 Components Used  
- ⌛ **4-bit Counters** → Count seconds and minutes downwards  
- 🔀 **Multiplexers (MUX)** → Select between Work and Rest time values for each digit (minutes tens, minutes units, seconds tens, seconds units)  
- 🟪 **SR Latch (Set-Reset)** → Controls whether the timer is active, with inputs for Reset (`R`) and Set (`S`)  
- 🔵 **D Flip-Flop** → Switches between Work mode and Rest mode once Work time reaches zero  
- 🔢 **7-Segment Displays** → Show the countdown in minutes and seconds  

---

## ▶️ How to Use  

1. **Enable Key**  
   - Set the **SR latch Enable = 1** to activate the timer  

2. **Reset Timer**  
   - Press **R** to reset all values to `00:00`  

3. **Set Work/Rest Times**  
   - Enter the **binary values** for Work time and Rest time into the multiplexers (`minTens`, `minUnits`, `secTens`, `secUnits`)  

4. **Load Values**  
   - Press **S** to load the selected values into the timer  

5. **Start the Timer**  
   - Press **Ctrl + K** to start timing  
   - ⚠️ Make sure the timer is **stopped before loading/resetting values**, otherwise errors may occur  

---

## ⚙️ How It Works  
- The **work timer** begins after loading values through the multiplexers  
- The **counters** decrement seconds and minutes, displaying the countdown on the **7-segment displays**  
- A **comparator** continuously checks whether all digits (`minTens`, `minUnits`, `secTens`, `secUnits`) are equal to zero  
- When the comparator detects that the work timer has reached `00:00`, it triggers the **D flip-flop** to switch into **rest mode**  
- The **rest timer** then begins automatically with the values you set in the multiplexers  
- Once the rest timer ends, the cycle can be restarted by setting new values with the SR latch control  

---

## 📂 Project Files  
- `Digital Interval Timer.circ` → The complete Logisim Evolution circuit file  
- Documentation with screenshots and usage instructions  

---

## 💡 Use Case  
This project demonstrates:  
- Sequential circuit design with **counters, latches, and flip-flops**  
- A practical **digital implementation of the Pomodoro technique**  
- The integration of **control logic, multiplexers, and display units** for a functional timer  

--- 

