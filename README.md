<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ICT From Heshan | Premium A/L LMS</title>
    <!-- Tailwind CSS CDN (Free Styling) -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-gray-900 text-white font-sans antialiased">

    <!-- 1. NAVIGATION BAR -->
    <nav class="bg-gray-800 border-b border-gray-700 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center">
                    <span class="text-2xl font-extrabold tracking-wider text-cyan-400">
                        <i class="fa-solid fa-code-branch mr-2"></i>ICT FROM HESHAN
                    </span>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#home" class="hover:bg-gray-700 px-3 py-2 rounded-md text-sm font-medium transition">Home</a>
                        <a href="#courses" class="hover:bg-gray-700 px-3 py-2 rounded-md text-sm font-medium transition">Courses</a>
                        <a href="#simulator" class="bg-cyan-600 hover:bg-cyan-500 px-3 py-2 rounded-md text-sm font-medium transition text-gray-900 font-bold">Logic Simulator</a>
                        <a href="#lms" class="hover:bg-gray-700 px-3 py-2 rounded-md text-sm font-medium transition">LMS Portal</a>
                    </div>
                </div>
                <div class="md:hidden">
                    <button class="text-gray-400 hover:text-white"><i class="fa-solid fa-bars text-xl"></i></button>
                </div>
            </div>
        </div>
    </nav>

    <!-- 2. HERO SECTION -->
    <section id="home" class="relative overflow-hidden py-20 px-4 sm:px-6 lg:px-8 bg-gradient-to-b from-gray-800 to-gray-900">
        <div class="max-w-5xl mx-auto text-center relative z-10">
            <span class="bg-cyan-900/50 text-cyan-400 border border-cyan-700 text-xs px-3 py-1 rounded-full font-bold uppercase tracking-wider">Sri Lanka's Next-Gen A/L ICT Platform</span>
            <h1 class="mt-6 text-4xl sm:text-6xl font-black tracking-tight">
                A/L ICT සරලව, ප්‍රායෝගිකව <br>
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">සුපිරිම A සාමාර්ථයකට!</span>
            </h1>
            <p class="mt-6 text-lg text-gray-400 max-w-2xl mx-auto">
                ක মুখපාඩම් කරන්නේ නැතුව Logic Gates, Python, Networking සහ Systems සිද්ධාන්ත ප්‍රායෝගිකව ඉගෙන ගන්න ලංකාවේ දියුණුම තාක්ෂණික පන්තියට අදම එකතු වන්න.
            </p>
            <div class="mt-10 flex justify-center space-x-4">
                <a href="#simulator" class="bg-cyan-500 hover:bg-cyan-400 text-gray-900 font-bold px-6 py-3 rounded-lg shadow-lg shadow-cyan-500/20 transition transform hover:-translate-y-0.5">Try Free Simulator</a>
                <a href="#courses" class="bg-gray-800 hover:bg-gray-700 border border-gray-700 font-medium px-6 py-3 rounded-lg transition">Explore Courses</a>
            </div>
        </div>
    </section>

    <!-- 3. INTERACTIVE LOGIC GATE SIMULATOR (A/L Spec) -->
    <section id="simulator" class="py-16 px-4 sm:px-6 lg:px-8 border-t border-gray-800 bg-gray-950">
        <div class="max-w-4xl mx-auto">
            <div class="text-center mb-10">
                <h2 class="text-3xl font-bold text-cyan-400"><i class="fa-solid fa-toggle-on mr-2"></i>Interactive Logic Gate Simulator</h2>
                <p class="text-gray-400 mt-2">Inputs (A සහ B) වෙනස් කරමින් Logic Gate එකෙන් Output එක ලැබෙන විදිහ Live අත්හදා බලන්න.</p>
            </div>

            <!-- Simulator Card Container -->
            <div class="bg-gray-900 rounded-2xl border border-gray-800 p-6 md:p-8 shadow-2xl">
                <!-- Selector Tabs -->
                <div class="flex flex-wrap gap-2 justify-center mb-8 border-b border-gray-800 pb-6">
                    <button onclick="changeGate('AND')" id="btn-AND" class="gate-btn bg-cyan-600 text-gray-900 font-bold px-4 py-2 rounded-lg transition">AND Gate</button>
                    <button onclick="changeGate('OR')" id="btn-OR" class="gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition">OR Gate</button>
                    <button onclick="changeGate('NOT')" id="btn-NOT" class="gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition">NOT Gate</button>
                    <button onclick="changeGate('NAND')" id="btn-NAND" class="gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition">NAND Gate</button>
                    <button onclick="changeGate('NOR')" id="btn-NOR" class="gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition">NOR Gate</button>
                    <button onclick="changeGate('XOR')" id="btn-XOR" class="gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition">XOR Gate</button>
                </div>

                <!-- Simulation Interactive Area -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-center justify-center p-6 bg-gray-950 rounded-xl border border-gray-800">
                    
                    <!-- Inputs Panel -->
                    <div class="flex flex-col items-center space-y-4">
                        <span class="text-xs uppercase tracking-widest text-gray-500 font-bold">Inputs</span>
                        
                        <!-- Input A -->
                        <div class="flex items-center space-x-4 bg-gray-900 p-3 rounded-lg w-full justify-between border border-gray-800">
                            <span class="font-bold text-lg text-cyan-400">Input A</span>
                            <button onclick="toggleInput('A')" id="btn-inputA" class="bg-gray-800 px-4 py-1.5 rounded font-mono text-xl text-red-500 border border-red-900/50">0</button>
                        </div>
                        
                        <!-- Input B (Hidden for NOT gate) -->
                        <div id="inputB-container" class="flex items-center space-x-4 bg-gray-900 p-3 rounded-lg w-full justify-between border border-gray-800">
                            <span class="font-bold text-lg text-cyan-400">Input B</span>
                            <button onclick="toggleInput('B')" id="btn-inputB" class="bg-gray-800 px-4 py-1.5 rounded font-mono text-xl text-red-500 border border-red-900/50">0</button>
                        </div>
                    </div>

                    <!-- Gate Icon Display -->
                    <div class="text-center py-6 md:py-0 border-y md:border-y-0 md:border-x border-gray-800 flex flex-col items-center justify-center">
                        <span id="gate-title" class="text-2xl font-black text-white tracking-widest mb-2">AND</span>
                        <div class="w-24 h-24 bg-cyan-950/40 border-2 border-cyan-500/50 rounded-full flex items-center justify-center shadow-lg shadow-cyan-500/10">
                            <i id="gate-icon" class="fa-solid fa-microchip text-4xl text-cyan-400"></i>
                        </div>
                    </div>

                    <!-- Output Panel -->
                    <div class="flex flex-col items-center justify-center space-y-2">
                        <span class="text-xs uppercase tracking-widest text-gray-500 font-bold">Output (Y)</span>
                        <div id="output-box" class="w-24 h-24 bg-gray-950 rounded-xl flex items-center justify-center border-2 border-red-500 shadow-lg transition duration-300">
                            <span id="txt-output" class="text-4xl font-mono font-bold text-red-500">0</span>
                        </div>
                        <span id="gate-logic-desc" class="text-xs text-gray-400 text-center mt-2 font-mono">Y = A . B</span>
                    </div>

                </div>
            </div>
        </div>
    </section>

    <!-- 4. COURSE SECTION -->
    <section id="courses" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
        <div class="text-center mb-12">
            <h2 class="text-3xl font-bold">Available A/L Courses</h2>
            <p class="text-gray-400 mt-2">ඔබට ගැළපෙනම පාඨමාලාව තෝරාගෙන අදම වැඩ අරඹන්න.</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Card 1 -->
            <div class="bg-gray-800 rounded-xl p-6 border border-gray-700 flex flex-col justify-between">
                <div>
                    <span class="bg-blue-900/60 text-blue-400 text-xs px-2.5 py-1 rounded font-bold uppercase">Theory</span>
                    <h3 class="text-xl font-bold mt-3">2027 A/L Theory</h3>
                    <p class="text-gray-400 mt-2 text-sm">ICT මුල සිට සරලව. දත්ත සන්නිවේදනය, දත්ත සමුදාය සහ ප්‍රכලනය (Python) ඇතුළු සියලුම විෂය නිර්දේශය ආවරණය කෙරේ.</p>
                </div>
                <button class="w-full mt-6 bg-gray-700 hover:bg-gray-600 text-white font-bold py-2 rounded-lg transition">Enrol Now</button>
            </div>
            <!-- Card 2 -->
            <div class="bg-gray-800 rounded-xl p-6 border border-cyan-500/30 shadow-lg shadow-cyan-500/5 flex flex-col justify-between">
                <div>
                    <span class="bg-cyan-900/60 text-cyan-400 text-xs px-2.5 py-1 rounded font-bold uppercase">Revision</span>
                    <h3 class="text-xl font-bold mt-3">2026 A/L Revision</h3>
                    <p class="text-gray-400 mt-2 text-sm">පූර්ණ විෂය පුනරීක්ෂණය, පසුගිය විභාග ප්‍රශ්න පත්‍ර සාකච්ඡාව සහ වැදගත් සිද්ධාන්ත කෙටි ක්‍රම මඟින් මතක තබා ගැනීම.</p>
                </div>
                <button class="w-full mt-6 bg-cyan-500 hover:bg-cyan-400 text-gray-900 font-bold py-2 rounded-lg transition">Enrol Now</button>
            </div>
            <!-- Card 3 -->
            <div class="bg-gray-800 rounded-xl p-6 border border-gray-700 flex flex-col justify-between">
                <div>
                    <span class="bg-purple-900/60 text-purple-400 text-xs px-2.5 py-1 rounded font-bold uppercase">Paper Class</span>
                    <h3 class="text-xl font-bold mt-3">2026 Paper Class</h3>
                    <p class="text-gray-400 mt-2 text-sm">සතිපතා කාලයට අනුව MCQ සහ Structural/Essay පත්‍ර ලබා දීම සහ Live Marking/Ranking පද්ධතිය.</p>
                </div>
                <button class="w-full mt-6 bg-gray-700 hover:bg-gray-600 text-white font-bold py-2 rounded-lg transition">Enrol Now</button>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-gray-950 border-t border-gray-800 py-8 text-center text-sm text-gray-500">
        <p>&copy; 2026 ICT From Heshan. All Rights Reserved. Designed for Next-Gen Tech Students.</p>
    </footer>

    <!-- INTERACTIVE SIMULATOR LOGIC (JAVASCRIPT) -->
    <script>
        // State variables
        let currentGate = 'AND';
        let inputA = 0;
        let inputB = 0;

        // Change Logic Gate Function
        function changeGate(gate) {
            currentGate = gate;
            
            // UI Button Highlighting Logic
            document.querySelectorAll('.gate-btn').forEach(btn => {
                btn.className = "gate-btn bg-gray-800 hover:bg-gray-700 px-4 py-2 rounded-lg transition";
            });
            document.getElementById(`btn-${gate}`).className = "gate-btn bg-cyan-600 text-gray-900 font-bold px-4 py-2 rounded-lg transition";

            // Update Titles & Equations
            document.getElementById('gate-title').innerText = gate;
            
            const inputBContainer = document.getElementById('inputB-container');
            if(gate === 'NOT') {
                inputBContainer.style.display = 'none'; // Hide input B for NOT gate
                document.getElementById('gate-logic-desc').innerText = "Y = A'";
            } else {
                inputBContainer.style.display = 'flex';
                if(gate === 'AND') document.getElementById('gate-logic-desc').innerText = "Y = A . B";
                if(gate === 'OR') document.getElementById('gate-logic-desc').innerText = "Y = A + B";
                if(gate === 'NAND') document.getElementById('gate-logic-desc').innerText = "Y = (A . B)'";
                if(gate === 'NOR') document.getElementById('gate-logic-desc').innerText = "Y = (A + B)'";
                if(gate === 'XOR') document.getElementById('gate-logic-desc').innerText = "Y = A ⊕ B";
            }

            calculateOutput();
        }

        // Toggle Inputs (0 to 1 / 1 to 0)
        function toggleInput(type) {
            const btn = document.getElementById(`btn-input${type}`);
            if(type === 'A') {
                inputA = inputA === 0 ? 1 : 0;
                btn.innerText = inputA;
                updateInputStyle(btn, inputA);
            } else {
                inputB = inputB === 0 ? 1 : 0;
                btn.innerText = inputB;
                updateInputStyle(btn, inputB);
            }
            calculateOutput();
        }

        function updateInputStyle(element, value) {
            if(value === 1) {
                element.className = "bg-cyan-950 px-4 py-1.5 rounded font-mono text-xl text-cyan-400 border border-cyan-500 shadow-sm shadow-cyan-500/30";
            } else {
                element.className = "bg-gray-800 px-4 py-1.5 rounded font-mono text-xl text-red-500 border border-red-900/50";
            }
        }

        // Main Core Logic for Gates
        function calculateOutput() {
            let output = 0;

            switch(currentGate) {
                case 'AND': output = inputA && inputB; break;
                case 'OR':  output = inputA || inputB; break;
                case 'NOT': output = !inputA ? 1 : 0; break;
                case 'NAND': output = !(inputA && inputB) ? 1 : 0; break;
                case 'NOR':  output = !(inputA || inputB) ? 1 : 0; break;
                case 'XOR':  output = inputA !== inputB ? 1 : 0; break;
            }

            // Convert boolean to numeric binary
            output = output ? 1 : 0;

            // Update Output UI
            const outputBox = document.getElementById('output-box');
            const txtOutput = document.getElementById('txt-output');
            
            txtOutput.innerText = output;

            if(output === 1) {
                outputBox.className = "w-24 h-24 bg-cyan-950 rounded-xl flex items-center justify-center border-2 border-cyan-400 shadow-lg shadow-cyan-500/30 transition duration-300";
                txtOutput.className = "text-4xl font-mono font-bold text-cyan-400 animate-pulse";
            } else {
                outputBox.className = "w-24 h-24 bg-gray-950 rounded-xl flex items-center justify-center border-2 border-red-500 transition duration-300";
                txtOutput.className = "text-4xl font-mono font-bold text-red-500";
            }
        }
    </script>
</body>
</html>
