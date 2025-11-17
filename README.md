# AclR Conformations - Interactive 3D PDB Viewer

**🔗 [View Interactive Visualization](https://jadenshirkey.github.io/Visualizing-AclR-Conformations-via-HTML-/AclR_PDB_with_Centers_v8.html)**

An interactive HTML-based widget for visualizing AclR protein conformations in 3D using the 3Dmol.js library. This tool allows researchers to explore different conformational states of the AclR protein, including apo and ligand-bound forms.

## Features

- **Interactive 3D Visualization**: Rotate, zoom, and pan to explore protein structures from any angle
- **Multiple Conformational States**: Switch between four different AclR conformations:
  - APO (AA') - Unbound conformation variant 1
  - APO (BC) - Unbound conformation variant 2
  - +LIG, OFF - Ligand-bound, inactive state
  - +LIG, ON - Ligand-bound, active state

- **Customizable Display Options**:
  - Toggle protein structure visibility
  - Fast mode (C-alpha trace) for performance
  - Show/hide geometric centers with distance measurements
  - Display/hide amino acid sidechains
  - Add/remove residue labels
  - Automatic rotation (spin mode)

- **Distance Measurements**: Automatically calculates and displays distances between DNA-binding domains (DBD) and ligand-binding domains (LBD)

- **Dark Theme UI**: Modern, easy-on-the-eyes interface optimized for extended viewing sessions

## Quick Start

### Online Usage

Simply open `AclR_PDB_with_Centers_v8.html` in any modern web browser. The widget will automatically load the 3Dmol.js library from a CDN.

### Offline Usage

For offline use or better performance:

1. Download the 3Dmol.js library:
   ```bash
   wget https://unpkg.com/3dmol@2.0.4/build/3Dmol-min.js
   ```

2. Place `3Dmol-min.js` in the same directory as `AclR_PDB_with_Centers_v8.html`

3. Open `AclR_PDB_with_Centers_v8.html` in your browser

The widget will automatically use the local copy if available.

## How to Use

### Basic Controls

1. **Mouse Controls**:
   - **Left-click + drag**: Rotate the structure
   - **Scroll**: Zoom in/out
   - **Right-click + drag**: Pan/translate the view

2. **State Selection**:
   - Use the "State" dropdown to switch between different AclR conformations
   - The structure will automatically update when a new state is selected

3. **Display Options**:
   - **Show PDB**: Toggle the protein structure on/off
   - **Fast mode (trace)**: Switch to C-alpha trace for better performance with large structures
   - **Show centers**: Display geometric centers of binding domains with distance measurements
   - **Sidechains**: Show/hide amino acid sidechains
   - **Labels**: Toggle residue labels
   - **Spin**: Enable automatic rotation

4. **Reset View**: Click the "Reset view" button to return to the default camera position

### Understanding the Visualization

- **Protein Structure**: Displayed in cartoon representation with rainbow coloring (N-terminus = blue, C-terminus = red)
- **Sidechains**: Important residues shown in stick representation
- **Centers**: Geometric centers of functional domains displayed as colored spheres:
  - LBD_A (Ligand-binding domain A)
  - LBD_B (Ligand-binding domain B)
  - DBD_A (DNA-binding domain A)
  - DBD_B (DNA-binding domain B)
- **Distance Measurements**: Dashed lines connecting domain centers with distances in Ångströms (Å)

## PDB Files Included

The repository includes four PDB files representing different AclR conformational states:

- `AclR_APO_AA'.pdb` (300 KB) - Apo state, AA' conformation
- `AclR_APO_BC.pdb` (297 KB) - Apo state, BC conformation
- `AclR_LIGAND_OFF.pdb` (335 KB) - Ligand-bound, inactive state
- `AclR_LIGAND_ON.pdb` (328 KB) - Ligand-bound, active state

These files are embedded directly in the HTML viewer for convenience, but are also available as separate files for use in other molecular visualization tools.

## Technical Details

### Dependencies

- **3Dmol.js** (v2.0.4): Modern, object-oriented library for molecular visualization
  - Automatically loaded from CDN: `https://unpkg.com/3dmol@2.0.4/build/3Dmol-min.js`
  - Falls back to local copy if placed in the same directory

### Browser Compatibility

The widget works in all modern browsers that support:
- HTML5
- CSS3
- WebGL (for 3D rendering)
- ES6 JavaScript

Tested browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari

### File Structure

```
.
├── AclR_PDB_with_Centers_v8.html   # Main HTML viewer (self-contained)
├── AclR_APO_AA'.pdb                # PDB file - Apo AA' state
├── AclR_APO_BC.pdb                 # PDB file - Apo BC state
├── AclR_LIGAND_OFF.pdb             # PDB file - Ligand OFF state
├── AclR_LIGAND_ON.pdb              # PDB file - Ligand ON state
├── 3Dmol-min.js                    # (Optional) Local copy of 3Dmol.js
└── README.md                       # This file
```

## Use Cases

This widget is ideal for:

- **Research presentations**: Interactive demonstrations of protein conformational changes
- **Educational purposes**: Teaching protein structure and dynamics
- **Publication supplements**: Providing reviewers and readers with interactive 3D structures
- **Structural analysis**: Comparing different conformational states and measuring domain distances
- **Remote collaboration**: Sharing a single HTML file for structural discussions

## Customization

The HTML file can be easily modified to:

- Add more PDB structures (edit the `PDBS` object)
- Change color schemes (modify the styling and 3Dmol.js color parameters)
- Add custom labels or measurements
- Highlight specific residues or regions
- Adjust the UI theme and layout

## License

See the [LICENSE](LICENSE) file for details.

## Credits

Visualization powered by [3Dmol.js](https://3dmol.csb.pitt.edu/), an object-oriented, WebGL-based JavaScript library for online molecular visualization.

## Contact & Contributing

Issues, suggestions, and contributions are welcome! Please feel free to open an issue or submit a pull request.

---

**Pro Tip**: For the best experience, use a computer with a dedicated GPU and view in fullscreen mode (F11 in most browsers).
