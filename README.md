# Alz-IDProteinExplorer

## Introduction

Welcome to the **Intrinsically Disordered Protein Simulation Tool**! This project is designed to tackle the complex challenge of simulating and understanding the behavior of intrinsically disordered proteins (IDPs). Unlike their well-structured counterparts, IDPs lack a stable, defined conformation under physiological conditions, making them intriguing yet difficult to study. These proteins play crucial roles in various cellular processes and are linked to several diseases. Our tool provides a way to visualize and analyze the dynamic behavior of IDPs, offering insights into their likely structures and residue interactions. By employing advanced computational techniques, we aim to advance our understanding in the field of structural biology and protein chemistry.

## Method and Approach

Our tool employs a Monte Carlo Metropolis algorithm, integrated with the Ising model and Gibbs distribution, to simulate and optimize the structure of IDPs. Here’s a detailed explanation of our methodology:

1. **Monte Carlo Metropolis Algorithm**: This stochastic approach explores the conformational space of the protein by proposing and accepting or rejecting changes based on energy calculations. The algorithm iterates to sample various configurations, driving the system towards an equilibrium state.

2. **Ising Model**: Adapted from statistical physics, the Ising model represents interactions between amino acid residues as "spins" that interact with their neighbors. This model captures hydrophobic and hydrophilic tendencies to reflect residue interactions effectively.

3. **Gibbs Distribution**: To achieve energy optimization, the Gibbs distribution is used. It ensures that the probability of a conformation is proportional to its Boltzmann factor, which incorporates both the configuration's energy and the temperature. This approach allows the system to explore and favor low-energy states.

4. **Energy Calculation**: Energy is computed based on the hydrophobicity and disorderness of neighboring residues. Hydrophobic interactions drive residues to minimize their exposure to water, while disorderness reflects flexibility and conformational entropy. This balance aids in finding a stable, energetically favorable conformation.

This combined approach leverages principles from statistical mechanics and computational optimization to simulate IDP behavior effectively, offering a detailed exploration of their conformational landscape and interaction patterns.

## Functionality

The Intrinsically Disordered Protein Simulation Tool offers several key features:

- **Visualization**: Generates graphical representations of the protein’s shape, showing the arrangement of residues and their interactions. This visual output helps users understand the overall structure and interaction network.

- **Simulation**: Allows users to input parameters and run simulations to explore different protein configurations. The Monte Carlo Metropolis algorithm refines these configurations towards an equilibrium state.

- **Energy Analysis**: Computes and displays the energy associated with residue interactions, based on hydrophobicity and disorderness. This analysis provides insights into protein stability and flexibility.

- **Interaction Map**: Provides a map of interactions between residues, helping identify potential functional sites and interaction domains.

By utilizing these features, researchers can gain valuable insights into the behavior and functional implications of intrinsically disordered proteins.


## Contributing

We welcome contributions to enhance and extend this tool. Please refer to our [CONTRIBUTION.md](CONTRIBUTION.md) file for guidelines on how to get involved.

## License

This project is licensed under the [MIT License](LICENSE).




## Updates

## Getting Started
Instructions:

```bash
python test2.py -pdb Downloads/tau.pdb -t 140 -i 20 -w1 1 -w2 0.1 -ph 7
PDB
```
-replace test2.py with the location of test2.py file in your computer
-replace Downloads/tau.pdb with the location of the target protein pdb file
```bash
python test2.py -h
```
-See help and the list of parameters

```bash
usage: test2.py [-h] [-type INPUT_TYPE] [-fasta FASTA_FILE] [-pdb PDB_FILE]
                [-rt TRIAL] [-d DIRECTORY] [-t TEMPERATURE] [-i ITERATION]
                [-w1 WEIGHT1] [-w2 WEIGHT2] [-ph PH] [-n NUMBER_PROTEIN]
                [-lower LOWER] [-upper UPPER] [-range RANGE]
                [-duplex DUPLEX_LENGTH] [-u UNSTRUCTURE_LENGTH]

cgRNA STS design scanner from introns

optional arguments:
  -h, --help            show this help message and exit
  -type INPUT_TYPE, --input_type INPUT_TYPE
                        input type FASTA or PDB
  -fasta FASTA_FILE, --fasta_file FASTA_FILE
                        FASTA sequence
  -pdb PDB_FILE, --pdb_file PDB_FILE
                        path to the input pdb file
  -rt TRIAL, --trial TRIAL
                        number of different random versions of the protein
                        generated(default 5)
  -d DIRECTORY, --directory DIRECTORY
                        output_directory
  -t TEMPERATURE, --temperature TEMPERATURE
                        Temperature in K
  -i ITERATION, --iteration ITERATION
                        Simulation iterations defaulted 100 (recommand
                        500-5000)
  -w1 WEIGHT1, --weight1 WEIGHT1
                        weight of charge used in energy calculation
  -w2 WEIGHT2, --weight2 WEIGHT2
                        weight of hydrophobicity used in energy calculation
  -ph PH, --ph PH       ph level of the simultation environment
  -n NUMBER_PROTEIN, --number_protein NUMBER_PROTEIN
                        number of protein in the simulation
  -lower LOWER, --lower LOWER
                        minimum window stride size for visualization
  -upper UPPER, --upper UPPER
                        maximum window stride size for visualization
  -range RANGE          The range of the number of sequences in FASTA file to
                        scan (e.g., "0-100")
  -duplex DUPLEX_LENGTH, --duplex_length DUPLEX_LENGTH
                        length of the nucleotides in duplex
  -u UNSTRUCTURE_LENGTH, --unstructure_length UNSTRUCTURE_LENGTH
                        length of the unstructured nucleotides
```

### Prerequisites/requirements

Ensure the following software and libraries are installed on your system:
- Python 3.8 or higher
- pip installed
- Installation Instructions:
```bash
pip install numpy matplotlib biopython pandas seaborn
```
-Download PDB protein files @ https://www.rcsb.org/

