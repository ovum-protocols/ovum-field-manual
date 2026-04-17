# ŌVUM — Field Manual 01

Gemini_Generated_Image_tbz16ftbz16ftbz1.png

### Tesla P4 Compute Recovery Protocol
**Verified protocols for constrained systems.**

---

## What this is
Cloud providers charge 10x to run AI on hardware
identical to decommissioned workstations sitting
in server rooms right now.

Field Manual 01 is a 50-page production-grade deployment
protocol for the NVIDIA Tesla P4 — covering 7 verified
workstation platforms, zero PSU modification required.
Every command tested. Every BIOS setting verified.
Every failure boundary documented.

---

## What's inside
- ✅ Full hardware install guide for 7 supported systems
- ✅ Per-chassis BIOS/UEFI settings — exact steps
- ✅ NVIDIA Driver 570.x + CUDA 12.8 install protocol
- ✅ Ollama systemd configuration + environment variables
- ✅ CPU governor + GPU power tuning for max tokens/sec
- ✅ Model recommendations + real benchmark table
- ✅ Full debug + recovery decision tree
- ✅ Docker + Open WebUI advanced setup
- ✅ Complete automation script (Automator tier)

---

## Supported Hardware Matrix
| System | CPU | Stock PSU | PCIe Slot | P4 Compatible |
|---|---|---|---|---|
| Dell OptiPlex 9020 MT | Intel 4th Gen Haswell | 290W | 1x PCIe 3.0 x16 | ✅ YES |
| Dell OptiPlex 7050 MT | Intel 7th Gen Kaby Lake | 260W | 1x PCIe 3.0 x16 | ✅ YES |
| Dell OptiPlex 7060 MT | Intel 8th Gen Coffee Lake | 260W | 1x PCIe 3.0 x16 | ✅ YES |
| Dell Precision T3610 | Intel Xeon E5 Ivy Bridge | 425W | 2x PCIe 3.0 x16 | ✅ YES |
| HP Z640 Workstation | Intel Xeon E5 v3/v4 | 925W | 3x PCIe 3.0 x16 | ✅ YES |
| HP Z440 Workstation | Intel Xeon E5 v3/v4 | 700W | 2x PCIe 3.0 x16 | ✅ YES |
| Lenovo ThinkStation P310 | Intel 6th/7th Gen Xeon | 400W | 1x PCIe 3.0 x16 | ✅ YES |

> No PSU upgrade required. Tesla P4 draws max 75W from PCIe slot only.

---

## Real Performance Numbers
| Model | Quant | VRAM | Tokens/sec |
|---|---|---|---|
| Llama3-8B-instruct | Q4KM | 6.2 GB | 28–34 |
| Mistral 7B | Q4KM | 4.9 GB | 30–38 |
| Phi-3.5-mini | Q4KM | 2.9 GB | 45–55 |
| Qwen2-7B | Q4KM | 5.2 GB | 30–36 |

---

## Get the protocol
| Tier | Includes | Price |
|---|---|---|
| 📄 Blueprint | 50-page PDF deployment protocol | $49 |
| ⚙️ Automator | PDF + verified .sh automation scripts | $149 |

**[→ Download Field Manual 01](YOUR_GUMROAD_LINK)**

---
