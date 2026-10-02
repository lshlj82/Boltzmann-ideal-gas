# Boltzmann Statistics of an Ideal Gas

An interactive, single-page web demo of the Boltzmann statistics of an ideal gas: the Maxwell speed distribution, the counting of system states for identical particles, the particle-in-a-box partition function, and the resulting thermodynamics (Sackur–Tetrode entropy and chemical potential).

Created by Claude Opus 5.5, based on the lecture notes by Sang Hoon Lee.

## Contents

The page follows Sections 6.4, 6.6, and 6.7 of the lecture notes.

**6.4 The Maxwell speed distribution.** A live plot of 𝒟(v) for several gases. You can change the temperature and drag a shaded band to read off the probability that a molecule's speed is between v₁ and v₂. This probability is computed exactly from the cumulative distribution. The plot marks v_max, v̄, and v_rms. It can also show the distribution split into its degeneracy factor 4πv² and its Boltzmann factor, and overlay other gases for comparison.

**6.4 How the distribution emerges.** A simulation of 1,200 argon atoms that start from a non-Maxwellian state and undergo random binary collisions, each of which conserves energy and momentum. The speed histogram relaxes onto the Maxwell curve for the temperature set by the total energy. Three panels show the box, velocity space, and the speed histogram.

**6.6 Counting system states.** The (s₁, s₂) grid for two particles shows why Z₁Z₂ counts nearly every state of identical particles twice. It compares Mᴺ/N! with the exact boson and fermion counts as the number of single-particle states M grows relative to the number of particles N.

**6.7 Particle in a box.** The energy levels and wavefunctions of a 1D box, and the sum Σ exp(−Eₙ/k_BT) compared with its integral, L/ℓ_Q, across the quantum and classical limits. The two differ by −½, plus a Poisson-summation correction of 2r·exp(−4πr²), where r = L/ℓ_Q.

**6.7 Ideal gas thermodynamics.** For the noble gases, the page computes the following from a chosen T and P:
- ℓ_Q, v_Q, and V/(N v_Q)
- the Sackur–Tetrode entropy, alongside tabulated values for comparison
- μ, U, and C_V

A plot of S/Nk_B against temperature marks where V/N < v_Q, which is where Boltzmann statistics breaks down.

## Running it

The whole demo is one file, `index.html`, with no build step. You can open it directly in a browser. You can also publish it with GitHub Pages: push the repository, then under **Settings → Pages** choose to deploy from the branch root.

The page loads two external resources. A network connection is needed for full rendering, though the interactive plots work without either one:

- [MathJax 3](https://www.mathjax.org/) from jsDelivr, used for the equations.
- [Source Serif 4](https://fonts.google.com/specimen/Source+Serif+4) from Google Fonts. If it can't load, the page falls back to Georgia or the system serif font.

## Notes on the physics

- Physical constants are CODATA 2018 values of k_B, h, and the atomic mass unit.
- The thermodynamics panel treats monatomic gases only, so Z_int = 1. Rotational, vibrational, and electronic contributions are not included.
- Tabulated entropies are standard molar entropies at 298.15 K and 1 bar. At those conditions the Sackur–Tetrode result for argon is 154.8 J/(mol·K), which agrees with the tabulated value.
