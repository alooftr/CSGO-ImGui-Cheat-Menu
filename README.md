# CSGO-Aimbot-Console
if it flags antivirus it's bcus it injects xd

# Build
1. Make sure it's in Release / x86.
2. Project > Properties > General > C++ Language Standard = ISO C++ 20 Standard (/std:c++20)
3. Project > Properties > Advanced > Character Set = Use Multi-Byte Character Set.
4. Project > Properties > Advanced > Target File Extension = .exe.
5. Project > Properties > Linker > System > SubSystem = Windows (/SUBSYSTEM:WINDOWS).
6. If you dont have Direct X 9 installed, download it. If you do,
7. Project > Properties > Linker > Input > Additional Dependencies > Add "d3d9.lib".
8. Build > Build Solution.

# Configuration
1. To change the name of the window go into "main.cpp", on line 30; change "pulsive.cc" to whatever you want.
2. To add hacks, go into "hacks.cpp" in the void "void hacks::VisualsThread" and inside the while loop, add what you want.
3. To initiate the hack, go into "globals.h" and in the globals namespace, add the hack you want. If it's a toggle "inline bool hack = false;".
4. Then go into "gui.cpp" and the end you'll see "gui::Render()" you'll see "ImGui::Checkbox("Glow",  &globals::glow);", the &globals means we passed that  namespace throw. and we can toggle that global.
5. Then add what you want with &globals::hack_name and you're done.
