<div align="center">
<img src="https://img.shields.io/badge/ŌVUM-Field%20Manual%2001-000000?style=for-the-badge&labelColor=000000&color=ffffff" alt="ŌVUM Field Manual 01"/>
Tesla P4 Compute Recovery Protocol

Turn a retired workstation into a working local AI box — without PSU mods, blind BIOS guessing, or wasted weekends.

Show Image
Show Image


50 pages · 7 verified chassis · Driver 570.x · CUDA 12.8 · Ollama · Open WebUI

</div>

What This Is

Cloud providers charge premium rates to run workloads that can often fit on older enterprise hardware — when the workload, GPU, and system are matched correctly.

Field Manual 01 is a 50-page, production-grade deployment protocol for the NVIDIA Tesla P4. Built around seven verified workstation platforms and a no-PSU-upgrade approach centered on the card's 75 W slot-powered design.

This is not a generic homelab PDF. It is a chassis-by-chassis deployment manual covering:


Physical install
BIOS and UEFI configuration
NVIDIA driver and CUDA setup
Ollama service configuration
Open WebUI integration
Performance tuning
Recovery paths when something breaks



The Tesla P4 is a low-profile, single-slot PCIe Gen3 card with 8 GB GDDR5 memory and a 75 W maximum power limit — purpose-built for constrained, stock-PSU systems.




Screenshots


Add your own screenshots in the assets/ folder and update the paths below. The four highest-trust images for conversion are: a BIOS slot configuration screen, nvidia-smi output, the Ollama or Open WebUI chat interface, and a sample PDF page.



BIOS / UEFI — PCIe Slot Configuration

<!--
  REPLACE THIS BLOCK:
  Capture your BIOS screen showing PCIe x16 slot enabled, then drop the image into assets/bios-screenshot.png
-->
[ Add your BIOS screenshot here: assets/bios-screenshot.png ]

Recommended: Dell OptiPlex or HP Z-series BIOS, PCIe configuration page.
Shows the slot is recognised before the OS boots — eliminates the #1 buyer concern.

nvidia-smi — GPU Recognised at Boot

<!--
  REPLACE THIS BLOCK:
  Run `nvidia-smi` after driver install and screenshot the terminal output.
  Drop into assets/nvidia-smi.png
-->
[ Add your nvidia-smi screenshot here: assets/nvidia-smi.png ]

Should show: Tesla P4 · 8192 MiB · Driver 570.x · CUDA 12.8 · P8 power state

Ollama + Open WebUI — Running Locally

<!--
  REPLACE THIS BLOCK:
  Screenshot the Open WebUI chat interface with a model loaded and a token/sec
  counter visible. Drop into assets/openwebui-screenshot.png
-->
[ Add your Open WebUI screenshot here: assets/openwebui-screenshot.png ]

Recommended: Show model selector + live generation + GPU memory readout side-by-side.

Sample PDF Page — Field Manual Interior

<!--
  REPLACE THIS BLOCK:
  Export one non-sensitive interior page as a PNG and drop into assets/pdf-sample.png
  Good candidates: the debug decision tree, the BIOS step table, or the benchmark table page.
-->
[ Add your PDF sample page here: assets/pdf-sample.png ]

Recommended: The debug/recovery decision tree page — shows depth and production quality.


Who This Is For

✅ Built for❌ Not forOperators building a low-cost local LLM box from decommissioned business hardwareBuyers looking for a gaming GPU guideBuyers who want exact steps, not theoryUsers who want multi-GPU or high-end 13B+ focused buildsUsers who want Ollama + Open WebUI on a workstation instead of renting cloud inferencePeople who only want a cloud workflowPeople who care more about verified compatibility than maximum GPU performanceBuyers expecting a beginner-friendly consumer PC tutorial


Supported Hardware Matrix


No PSU upgrade required. The Tesla P4 draws a maximum of 75 W through the PCIe slot — no external power connectors needed.



SystemCPUStock PSUPCIe SlotP4 CompatibleDell OptiPlex 9020 MTIntel 4th Gen Haswell290 W1× PCIe 3.0 x16✅ YESDell OptiPlex 7050 MTIntel 7th Gen Kaby Lake260 W1× PCIe 3.0 x16✅ YESDell OptiPlex 7060 MTIntel 8th Gen Coffee Lake260 W1× PCIe 3.0 x16✅ YESDell Precision T3610Intel Xeon E5 Ivy Bridge425 W2× PCIe 3.0 x16✅ YESHP Z640 WorkstationIntel Xeon E5 v3/v4925 W3× PCIe 3.0 x16✅ YESHP Z440 WorkstationIntel Xeon E5 v3/v4700 W2× PCIe 3.0 x16✅ YESLenovo ThinkStation P310Intel 6th/7th Gen Xeon400 W1× PCIe 3.0 x16✅ YES


Real Performance Numbers

ModelQuantVRAMTokens/secLlama 3 8B InstructQ4_K_M6.2 GB28–34Mistral 7BQ4_K_M4.9 GB30–38Phi-3.5-miniQ4_K_M2.9 GB45–55Qwen2-7BQ4_K_M5.2 GB30–36


Benchmark methodology: Ubuntu 22.04 LTS · NVIDIA Driver 570.x · CUDA 12.8 · Ollama 0.1.x · prompt length ~128 tokens · figures represent generation throughput (tokens/sec post-prompt), averaged over 3 runs at idle system load. CPU governor set to performance. GPU power limit at 75 W (stock slot max).




What's Inside

Field Manual 01 — Contents
├── Hardware Install Guide        Full physical install for all 7 supported systems
├── BIOS / UEFI Configuration     Per-chassis settings with exact steps
├── NVIDIA Driver + CUDA Setup    Driver 570.x + CUDA 12.8 install protocol
├── Ollama Configuration          systemd service + environment variable reference
├── Performance Tuning            CPU governor + GPU power limit optimisation
├── Model Recommendations         Tested models + benchmark table with methodology
├── Debug + Recovery Tree         Full decision tree for when something breaks
├── Docker + Open WebUI Setup     Advanced container deployment walkthrough
└── [Automator tier only]
    └── Automation Scripts        Verified .sh scripts for faster, error-free deploy


Pricing Tiers

TierIncludesBest forPrice📄 Blueprint50-page PDF deployment protocolBuyers who want the full manual and will run steps manually$49⚙️ AutomatorPDF + verified .sh automation scriptsBuyers who want faster deployment and fewer setup mistakes$149

<div align="center">
Show Image

</div>

Why This Is Different

Most homelab AI content is either too generic, too expensive, or built around newer consumer GPUs.

This product is narrower on purpose: Tesla P4 · stock enterprise hardware · verified chassis support · repeatable deployment path into Ollama and Open WebUI.

That specificity is the advantage.


Quick Compatibility Check

Before you buy, confirm your system meets these three criteria:


 Your chassis is one of the 7 listed above or has a PCIe 3.0 x16 slot with clearance for a low-profile single-slot card
 Your stock PSU is ≥ 260 W (the P4 draws 75 W max through the slot — no external connector needed)
 You are running or planning to run Ubuntu 22.04 LTS (other distros possible but not covered in the manual)


If all three are checked — you're good to go.


License & Usage

This repository is a public landing page for a commercial product. The PDF and scripts are delivered via Gumroad after purchase and are not distributed here.


<div align="center">
ŌVUM · Field Manual 01
Verified deployment protocols for constrained systems.

Show Image

</div>
