# PIC18 Pipeline Lab

### 👉 [Open the live lab](https://mohammed2345353.github.io/pic18-pipeline-simulator/)

![HTML](https://img.shields.io/badge/built%20with-HTML%20%2B%20SVG%20%2B%20JS-orange)
![Offline](https://img.shields.io/badge/runs-offline-brightgreen)
![Dependencies](https://img.shields.io/badge/dependencies-0-brightgreen)

An interactive teaching model of the PIC18 Harvard architecture. The signal map shows how the CPU can fetch an instruction from Flash and access RAM in the same instruction cycle.

## Run the lab

Open `index.html` in a browser or choose **Open in Integrated Browser** from its editor tab in VS Code. The lab uses HTML, CSS, SVG and JavaScript and runs offline.

Choose **Next cycle** to step through the instructions or **Play** to run the sequence. Select a circle to inspect its role and current value. Use the timeline to revisit any cycle.

| Cycle | Fetch | Execute |
| --- | --- | --- |
| 1 | `MOVLW 0x25` | — |
| 2 | `MOVWF 0x40, ACCESS` | Load `0x25` into WREG |
| 3 | `INCF 0x40, F, ACCESS` | Write `0x25` from WREG to RAM address `0x40` |
| 4 | — | Read and increment RAM at `0x40` to `0x26` |

The lab models three sequential, single-word instructions and displays register values after each instruction cycle. The diagram and timing are simplified for teaching.

Reference: [Microchip PIC18FXX2 data sheet](https://ww1.microchip.com/downloads/en/devicedoc/39564c.pdf), section 4.2 and the instruction set summary.

## Who it's for

- Students learning microcontrollers and computer architecture (fetch/execute overlap, Harvard vs. von Neumann).
- Teachers who want a visual to project in class: step forward and back through each instruction cycle.

## Contributing

Ideas for more instructions (branches, `CALL`/`RETURN`, flushing the pipeline) are welcome. Open an issue or a pull request.
