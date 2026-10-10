# 🤖 jev-robot-control - Watch AI Robots Move Real Objects

## 🚀 What Is This?

This program lets you watch three different artificial intelligence (AI) systems compete to move a small robot arm. The robot must pick up an apple and place it on a plate. You can see each AI think, move, and react — just like watching a game show for robots!

The whole thing runs on your computer using a physics simulator called MuJoCo. That means the robot moves in a virtual 3D world that behaves like the real world. You don't need any robot hardware or special equipment.

## 🎬 See It In Action

Before you download anything, watch this short video to see what the comparison looks like:

[▶️ Watch the comparison video](media/jev-vs-gpt6-vs-mini-xyz.mp4)

This video shows all three AI systems side by side, moving the same robot to complete the same task.

![Final comparison screenshot](media/final.png)

## 🏆 How Did They Perform?

Here is the result from one complete test run. Each AI had the same starting conditions and the same task: pick up the apple and place it on the plate.

| Controller | Outcome | Cycles | API calls | API cost | Wall time | Simulation time |
|---|---|---:|---:|---:|---:|---:|
| Jev 1.13 | ✅ Placed the apple | 113 | 226 | $0.018825 | 181.847 seconds | 36.16 seconds |
| GPT-6 Astra (low reasoning) | ✅ Placed the apple | 106 | 212 | $5.933624 | 707.274 seconds | 33.92 seconds |
| GPT-4.1 mini | ❌ Hit 160-cycle limit | 160 | 320 | $0.288512 | 704.253 seconds | 51.20 seconds |

**What do these numbers mean?**

- **Cycles:** How many times the AI made a decision to move the robot.
- **API calls:** How many times the AI asked its "brain" (a cloud service) for help.
- **API cost:** How much money those cloud requests cost (Jev is very cheap!).
- **Wall time:** Real-world time the test took on the computer.
- **Simulation time:** Virtual time inside the simulated world.

This was one test per AI, not a statistical average. It shows what happened in that single trial.

## 🖥️ System Requirements

Your computer needs to meet these minimum requirements to run the program smoothly:

- **Operating System:** Windows 10 or Windows 11 (64-bit)
- **Processor:** Intel Core i3 or AMD equivalent or better
- **Memory (RAM):** At least 8 GB
- **Storage:** At least 2 GB of free disk space
- **Graphics:** Any GPU from the last 10 years (integrated graphics are fine)
- **Internet:** Required only for the GPT-6 Astra and GPT-4.1 mini controllers to make API calls

No special hardware, robot, or sensors are needed. Everything runs virtually.

## 📥 Download and Install

[![Download Now](https://img.shields.io/badge/Download-jev--robot--control-blue?style=for-the-badge&logo=github)](https://github.com/Drykeeightyeight427/jev-robot-control)

Visit this link to download the application.

After you click the link, you will land on the project page. Look for the green **"Code"** button or a **"Releases"** section. Choose the download option that gives you a folder with all the files.

Once the download finishes, you will have a folder named `jev-robot-control` (or similar). Inside that folder, you will find everything you need.

## 🛠️ How to Run the Program

Follow these steps carefully:

1. **Extract the files** (if they came in a ZIP file). Right-click the downloaded file and choose **"Extract All..."**. Choose a folder you can easily find, like your Desktop.

2. **Open the main folder.** Look inside for a file named `jev-robot-control.exe` or a file called `run.bat` or `start.bat`. If you see an `.exe` file, double-click it. If you see a `.bat` file, double-click that instead.

3. **Wait for the program to start.** A window will open showing the robot simulation. The three AI systems will begin their tasks automatically.

4. **Watch the comparison.** The program shows all three controllers working in synchronized columns. You will see Jev, GPT-6 Astra, and GPT-4.1 mini each trying to place the apple.

5. **When it finishes,** the program will display the final results. You can close the window when you are done.

**First-time setup note:** The program may need to download some small supporting files on its first run. This is normal and only happens once. Make sure you are connected to the internet for that initial step.

## 🔍 What You Will See

When the program runs, you will see three separate panels. Each panel shows the same virtual robot arm. The task is simple:

1. The robot arm starts in a home position.
2. An apple sits on a table.
3. A plate sits nearby.
4. Each AI must figure out how to grab the apple and put it on the plate.

Each AI works differently:

- **Jev 1.13:** A fast, local controller that makes decisions directly on your computer. It does not need cloud access. It is very fast and very cheap.
- **GPT-6 Astra (low reasoning):** A cloud-based AI that "thinks" more slowly. It uses internet requests and costs more money per action.
- **GPT-4.1 mini:** Another cloud AI, but with less capability. In this test, it could not finish the task in the allowed time.

The program records everything: every movement, every decision, and the final outcome. You can replay any portion of the test.

## 📁 Files in the Repository

Here is what you will find inside the project folder:

- **`media/`** — Contains the comparison video and final screenshot.
- **`source/`** — The main program code (you do not need to touch this).
- **`results/`** — Recorded responses and trajectories from the test run.
- **`verifier/`** — A tool that checks whether the robot's movements were valid.
- **`README.md`** — This documentation.

## ❓ Frequently Asked Questions

**Q: Do I need to know programming to use this?**
A: No. This program runs as a standalone application. You just double-click to start it.

**Q: Do I need a real robot arm?**
A: No. Everything happens in a virtual simulator on your screen.

**Q: Will this cost me money?**
A: Running Jev costs nothing. The GPT controllers require API keys and may incur charges if you use them. The default test runs all three, but you can watch without setting up any API keys.

**Q: Why did GPT-4.1 mini fail?**
A: It reached the maximum allowed number of decision cycles (160) without completing the task. That is a built-in time limit, not a crash.

**Q: Can I change the task or the robot?**
A: The included program is fixed for this comparison. Changing it requires modifying the code, which is possible but not necessary for viewing.

**Q: What if the program does not start?**
A: Make sure you extracted all files completely. Try right-clicking the executable and selecting **"Run as administrator"**. Check that your antivirus is not blocking the program — sometimes security software flags new applications.

## 🧪 The Offline Verifier

The repository includes a special tool called the **offline verifier**. This tool lets you check whether a recorded robot trajectory actually accomplished the task — without running the full simulation again.

You can use this if you want to validate results or explore how the verification works. Simply open the `verifier` folder and run the included script (instructions are inside that folder).

## 🤝 Need Help?

If you run into any problems, here is what you can do:

- Re-read the steps above carefully.
- Make sure you have extracted all files from the download.
- Check your internet connection for the first run.
- Look at the project's Issues page on GitHub (if available) for known problems.

## 🧠 About the Controllers

This project is not just a game — it is a serious technical comparison. The three AI systems represent different approaches to robot control:

- **Jev 1.13** is a purpose-built controller designed for this task. It uses direct Cartesian control (moving in X, Y, Z directions) and makes efficient decisions locally.
- **GPT-6 Astra** is a large language model that generates movement intents through a cloud API. It works but is slower and more expensive.
- **GPT-4.1 mini** is a smaller model that struggles with the multi-step reasoning required for this task.

By watching all three side by side, you can see the trade-offs between speed, cost, and capability.

## 📄 License and Credits

This project is provided for educational and research purposes. The code is available for you to inspect and learn from. If you use any part of it in your own work, please reference this repository.

## 🏁 Final Words

You now have everything you need to download, run, and enjoy this robot comparison. It is a fascinating look at how different AI systems approach a simple physical task. Whether you are a robotics enthusiast, an AI curious user, or just someone who likes watching robots, this program has something for you.

Download it today and see the future of robot control with your own eyes.

[![Get Started Now](https://img.shields.io/badge/Download-jev--robot--control-green?style=for-the-badge&logo=github)](https://github.com/Drykeeightyeight427/jev-robot-control)

Keywords: robot control, xArm7, MuJoCo, AI comparison, GPT-6 Astra, GPT-4.1 mini, Jev, Cartesian control, robotics simulator, virtual robot, apple placement task, offline verifier, synchronized replay, Windows application, API cost comparison, trajectory recording