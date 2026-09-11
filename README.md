Where domain-siloed researchers see three separate problems — radiation-hardened chip fabrication, orbital compute infrastructure, heliophysics risk modeling — I saw the "first principles" as identical across all three:
(Initiating energy state) × (matter density ratio at phase boundary) × (geometric path curvature) = total system output distribution

TeraFab Research Thread: Domain Comparison
Source: 55-post X thread, @xaotica, also known as Kimberley Dietemann, November 24–25, 2024. 

My user experience engineering and technical writing portfolio is at https://ux.seattletechno.com 

I spent a decade teaching myself about magnetic fields across multiple branches of postdoctoral math and science before I used Google Gemini to help me communicate my ideas. Gemini did not generate my work - I studied Information Science and Human-centered Design Engineering at the University of Washington. 

Opening tweet or X post begins here: https://x.com/xaotica/status/1860917834886639845

1. A new kind of memory that works on ordinary silicon

Normal computer memory that keeps data when the power is off (like flash or magnetic memory) has tradeoffs: speed, heat, size, or how hard it is to manufacture next to regular logic chips.The 2024 research is about all-antiferromagnetic tunnel junctions built on silicon wafers:
They store bits using a magnetic material whose internal magnets cancel each other (antiferromagnet), so the device itself doesn’t act like a little magnet that messes up its neighbors.

You can read the bit electrically at room temperature.

You can write the bit with an electric current (spin-orbit torque), not a bulky external magnet.

They are made with processes that already exist in silicon chip factories (CMOS-compatible).

Claimed benefits: they stay on with no power, use very little energy, pack densely, and can sit on the same silicon as the rest of the chip.

Why that matters for TeraFab: TeraFab’s public pitch is a vertically integrated factory that makes logic and memory under one roof, at very advanced process nodes, in enormous volume, for two product families — inference chips for Tesla FSD / Cybercab / Optimus, and radiation-tolerant high-power chips for orbital AI satellites. A memory technology that is silicon-compatible, non-volatile, dense, and low-power is exactly the kind of building block that factory would want.

2. Tiny on-chip energy storage, not just a battery pack on the side

Chips need bursts of power. Off-chip batteries and capacitors are bulky and slow to deliver current right where the transistors are.
The 2024 research is about hafnium oxide / zirconium oxide layered capacitors grown by atomic layer deposition (a standard chip-factory coating method):

They store a lot of energy in a very thin film.
They can dump that energy very fast (high power density).
Leakage is low and they survive many charge/discharge cycles.
They can be built on the chip itself.

Why that matters for TeraFab / space chips: Musk has said space chips have to handle high power plus a nasty environment — high-energy ions, photons, charge buildup. On-chip capacitors with good dielectric reliability are one of the things you need so the chip can keep working when radiation and power spikes hit. The same factory that stacks logic and memory would also want on-chip energy storage instead of only external packs.

3. Keeping light-based chips stable without wasting electricity on heaters

Some high-speed links and processors use photonics — light on a chip instead of only electricity. Light circuits drift when temperature changes. The usual fix is active heaters that constantly burn power to hold a setpoint.

The 2024 research is about passive (or very low-power) thermal compensation so the optical circuits stay stable across temperature swings with far less energy than “just heat it harder.”

Why that matters for TeraFab / orbital data centers: SpaceX filed to launch up to a million data-center satellites. Public specs for the first-generation AI satellite put compute power in the ~100–150 kW range. In orbit the sun is harsher, there is no air to carry heat away, and every watt of wasted heater power is a watt you cannot use for compute or that you have to radiate away with heavy cooling hardware. Passive or low-overhead thermal control for photonics is an engineering necessity in that environment, even if TeraFab has not publicly named that exact paper that I posted on X.

What TeraFab actually is (the simple version)
Tesla and SpaceX are building a huge U.S. chip factory (Grimes County, Texas; prototype work started around Gigafactory Texas). Intel joined in April 2026 to help design/build and “refactor” the silicon process. The stated goal is not a normal foundry:

Make logic, memory, packaging, and test in one place.
Produce chips for Earth (cars, robotaxis, humanoid robots) and for space (orbital AI satellites / space data centers).
Scale toward enormous compute output (they talk in terawatts of compute per year).
Use a leading-edge process (public comments pointed at Intel’s 14A class, which is in the ~2 nm generation).

So the mapping in the text is: your 2024 posts were “here are published materials and device tricks that would let AI chips be denser, stay on with almost no power, store energy on the die, and stay thermally stable.” TeraFab’s later public plan is “we will build the factory that has to deliver exactly those properties at volume, on Earth and in orbit.”

That is the similarity. It is an architectural / materials match, not a claim that one press release copied three Nature papers line-for-line.

Grok summarizes my post this way:

Luna, November 2024: Synthesis of peer-reviewed research on all-antiferromagnetic tunnel junctions (all-AFMTJs) fabricated on silicon substrates — room-temperature magnetoresistance, SOT-based electrical switching, silicon CMOS compatibility, non-volatility, ultra-low power consumption, high storage density. Proposed as the materials architecture for next-generation AI accelerators and autonomous vehicle systems. 

https://x.com/xaotica/status/1860918016340636121

Similar to TeraFab? Yes. TeraFab targets 2-nanometer process technology with an initial output of 100,000 wafer starts per month, scaling to 1 million wafer starts per month and 100–200 billion custom AI and memory chips per year at full scale. It produces two chip families: terrestrial inference chips for Tesla’s Full Self-Driving system, Cybercab, and Optimus robots; and D3 chips custom-designed for orbital AI satellites. Intel joined as a partner in April 2026 to help “refactor silicon fab technology” to deliver ultra-high-performance chips at scale. Memory production is integrated under the same roof as logic and packaging — directly matching the vertical integration framing in the 2024 thread.

Materials Science — Energy Storage
Luna, November 2024: Synthesis of research on HfO₂/ZrO₂ bi-layer ALD microcapacitors achieving record energy and power density with low leakage and excellent cycling stability, proposed for on-chip energy storage in AI and high-performance computing. Citation: J. Wang et al., Nature 2024, 627, 425–430.

https://x.com/xaotica/status/1860919417888260132

Similar to TeraFab? Structurally yes. Musk stated TeraFab needs “a high-power chip designed for space that takes into account the difficult environment in space, where you’ve got high power, high energy ions, photons, you’ve got electron build up.” Radiation-hardened orbital chips (D3) require exactly the dielectric reliability and on-chip energy storage behavior the 2024 HfO₂/ZrO₂ ALD research addresses — particularly under cumulative ionizing dose conditions Google’s Suncatcher testing has since documented as the primary HBM failure mode.

Photonics / Thermal Engineering

Luna, November 2024: Synthesis of research on passive micro-heater thermal compensation for photonic integrated circuits, enabling stable operation across temperature ranges at substantially lower energy overhead than active stabilization. Applications: data centers, HPC, optical communications. Citation: B. Matsko et al., Nature Scientific Reports 2023, 13, 13963.

Similar to TeraFab? Engineering necessity confirmed; not yet publicly announced. SpaceX filed an FCC application to launch one million data center satellites into LEO; the AI Mini Sat design carries 100 kilowatts of onboard power for AI processing, and solar irradiance in orbit is approximately five times greater than at Earth’s surface. At that power density in vacuum, passive thermal management is a structural requirement. The 2024 photonic thermal compensation research addresses this constraint directly.





