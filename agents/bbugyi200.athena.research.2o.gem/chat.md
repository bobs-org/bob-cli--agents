# Chat History - ace-run (research.2o.gem)

- **TIMESTAMP:** 2026-09-26 17:15:53 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.2o.gem
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260926_170810.md`

## Prompt

%id(gem, clan=research.2o)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.2o.cdx`, `research.2o.grk`, `research.2o.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I have a UPS
attached to this machine that is probably not actually connected to this machine but is
powering it. I don't know what the make or model of the UPS is but I do remember that I
used to control it from this machine back when it was connected with a USB cord via the
`pwrstat` command (I think). That UPS is alerting me that the battery is no longer
functional and needs to be replaced so I need to figure that out. Also in the case of
power outages, I need a way to remotely turn this machine on.

Can you do some research with the goal of helping me decide the best way to implement
this? End your analysis with a recommended solution and a guess as to what UPS is
powering this machine. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: UPS Identification, Battery Replacement, and Remote Power-On Strategy for Athena

The complete research report has been written to:
`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202609/ups_battery_replacement_and_remote_power_on__gem.md`

And registered into durable SASE artifact storage:
- **Artifact Label:** `research:202609/ups_battery_replacement_and_remote_power_on__gem.md`
- **Artifact Ref:** `file:explicit:11a7e0a09e9bcef7a0d8d471`

---

## 1. Identification of the UPS

### Conclusion: **CyberPower CP1500PFCLCD** (1500VA / 900W, Pure Sine Wave)

**Direct Evidence Uncovered on System:**
1. **Workstation Hardware Build Sheet (`~/Sync/var/notes/Journal/computer.txt`)**:
   Under the hardware manifest for this exact machine (AMD Ryzen Threadripper 3970X, ASUS PRIME TRX40-PRO motherboard, RTX 3080 Ti GPU), the UPS is explicitly documented:
   ```text
   ===== UPS =====
   [X] CyberPower CP1500PFCLCD
       - https://www.amazon.com/gp/product/B00429N19W/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1
   ```
2. **Package Manager (`dpkg -l`)**: Residual configuration for CyberPower's native Linux management suite:
   ```text
   rc  powerpanel  1.3.3  amd64  PowerPanel for Linux is a software program that monitors the status of your CyberPower Systems UPS.
   ```
3. **Shell Aliases (`~/.config/aliases.sh`, line 461)**:
   `alias pwrstat='sudo pwrstat'`
4. **Shell History (`~/.zsh_history`)**: Multiple invocations of `pwrstat` and `pwrstat -status` during past reboot and provisioning sequences.
5. **Obsidian GTD Vault (`~/bob/cash.md` & `~/bob/dev.md`)**:
   - `cash.md`: Tasks scheduled from late August 2026: `Buy new battery for UPS!`.
   - `dev.md`: `Figure out why UPS doesn't protect athena! -> OBSOLETE: See [[cash#^buy-ups-battery]]!`.

---

## 2. Battery Replacement Guide

### Root Cause & Urgency
Sealed Lead-Acid (SLA) AGM batteries have an expected service life of **3 to 5 years**. Purchased around 2020–2021, the original internal cells are ~5–6 years old. High internal resistance now prevents them from sustaining nominal float voltage under load, triggering the audible alarm and replacement warning. In this state, the unit cannot provide backup runtime during a power drop.

### Battery Specifications
- **Configuration:** **Two 12V 9Ah** (or 8.5Ah) AGM SLA batteries connected in series (producing a **24V DC** bus).
- **Physical Dimensions (per cell):** ~5.94" L × 2.56" W × 3.70" H (151 × 65 × 94 mm).
- **Terminal Type:** **F2** (0.250" / 6.35 mm wide spade tabs). *Do not purchase F1 (0.187") terminals.*

### Replacement Options
1. **CyberPower Official Replacement Cartridge (RB1290X2 / RB1290X2B)** — *~$75 – $85*
   - Pre-assembled with the correct series bridge harness, heavy-gauge wiring, fuse, and connector.
   - Plug-and-play installation; includes prepaid recycling return packaging.
   - *Tip:* Verify your unit's serial number at [CyberPower Battery Replacement Tool](https://www.cyberpowersystems.com/tools/battery-replacement/) to confirm whether `RB1290X2` or `RB1290X2B` is designated.
2. **Third-Party Bare SLA Batteries (Pair)** — *~$35 – $45*
   - Examples: **Mighty Max ML9-12 F2 (2-pack)** or **ExpertPower EXP1290 F2 (2-pack)**.
   - Requires peeling off the outer tape and reusing the original center bridge wire/inline fuse between the two new batteries.

### Replacement Steps
1. Power down `athena`, switch off the UPS, and disconnect the UPS from the wall.
2. Remove the screw on the bottom/front battery door and slide off the faceplate.
3. Slide out the battery pack and disconnect the main **red (+)** and **black (-)** leads.
4. Replace with the OEM cartridge or transfer the center fuse/bridge wire to the new bare cells (maintaining series polarity).
5. Slide back into the chassis, reconnect red and black leads, and replace the cover.
6. Connect to wall power and allow to charge undisturbed for **8 to 12 hours** before placing under full load. Hold the power button to run a self-test and clear the alert.

---

## 3. Remote Power-On Strategy for Athena

`athena` runs on an **ASUS PRIME TRX40-PRO** motherboard with an **Intel I211 Gigabit NIC** (`enp67s0`, MAC: `a8:5e:45:d0:74:53`). With a 280W Threadripper 3970X and 350W RTX 3080 Ti, system load can reach 600W–800W+.

### The Challenge with Standard UPS Shutdowns
If a UPS daemon cleanly shuts down Linux before battery depletion, the machine enters ACPI **S5 (Soft Off)** while standby power remains. If utility power returns:
- If the UPS never dropped output power, the PSU never experienced a true AC loss (**G3 state**); standard BIOS "Restore AC Power Loss" will **not** turn the PC back on.
- A method is needed to either signal a power-on or cycle AC power to the PSU.

### Evaluated Options & Comparative Analysis

| Method | Additional Cost | Hardware Needed | Works After Clean S5 Shutdown? | Remote Access Mechanism | Handles OS Freeze / Hang? |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. BIOS AC Restore Only** | $0 | None | Only if UPS fully cuts output | Autonomous on power return | No |
| **2. Heavy-Duty Smart Plug + BIOS** | ~$15 – $25 | 15A Smart Plug | **Yes** (Remote power cycle) | Smartphone App / Cloud / HA | **Yes** (Hard reboot) |
| **3. Wake-on-LAN (WoL)** | $0 | None | **Yes** (If standby power present) | Router App / Tailscale peer | No |
| **4. SwitchBot Bot / Smart Relay** | ~$30 – $40 | SwitchBot / Relay | **Yes** (Direct button press) | BLE Hub / Cloud App | **Yes** (5s long press) |
| **5. Hardware KVM (PiKVM / NanoKVM)**| ~$40 – $180 | KVM-over-IP unit | **Yes** (ATX header control) | Web UI / Tailscale / SSH | **Yes** + Full BIOS / Console |

---

## 4. Recommended Solution

A tiered solution provides the highest reliability, lowest operational friction, and immediate zero-cost wins:

### 1. Zero-Cost Foundation (Configure Immediately)
- **BIOS Settings (`ASUS PRIME TRX40-PRO`):**
  - Enter UEFI BIOS (`<Del>` on startup) > **Advanced Mode (`F7`)** > **Advanced** > **APM Configuration**.
  - Set **Restore AC Power Loss** = **`[Power On]`**.
  - Set **Power On By PCI-E** = **`[Enabled]`** (activates Intel I211 onboard LAN wake).
  - Set **ErP Ready** = **`[Disabled]`** (ensures standby power to PCIe/NIC in S5).
- **Linux Wake-on-LAN Setting:**
  - Persist magic packet wake on `athena`:
    ```bash
    sudo nmcli connection modify "Wired connection 1" 802-3-ethernet.wake-on-lan magic
    ```
  - Send WoL packets to MAC `a8:5e:45:d0:74:53` via the **TP-Link AX11000 Tether App**, router web portal, or another local device on Tailscale.

### 2. Reliable Remote On-Demand Control (Recommended Production Setup)
- Install a **15A / 1800W rated Smart Plug** (e.g. **Kasa KP125M / Tapo P125M** or **Shelly Plus 1PM Gen3**) into one of the **Battery + Surge** outlets of the CyberPower CP1500PFCLCD. Plug `athena` into this smart plug.
- **How to Power On Remotely from Anywhere:**
  1. Open the smart plug app (or Home Assistant).
  2. Toggle the smart plug **OFF**.
  3. Wait **20 to 30 seconds** (allows PSU capacitors to discharge so the motherboard detects the transition to G3).
  4. Toggle the smart plug **ON**.
  5. The ASUS motherboard detects AC mains restoration and automatically boots up.
  - *Bonus:* This doubles as an emergency hard-power-cycle mechanism if the OS ever kernel panics or freezes while you are away.

### 3. Reconnect the UPS USB Cable
- Connect a standard **USB Type-A to Type-B** cable from the UPS to `athena`.
- Reinstall CyberPower's native utility (`powerpanel`) to restore the `pwrstat` command, or install Network UPS Tools (`nut`) to broadcast power state to other machines across the local network.
