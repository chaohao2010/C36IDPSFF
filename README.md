## CHARMM36IDPSFF force field for GROMACS

### Introduction
This is the description of the concept and the usage of **CHARMM36IDPSFF** force field

Recently, we developed a residue-specific force field based on CHARMM36m force field with  
modified dihedral energy correlation map (CMAP) to simulate intrinsically disordered proteins (IDPs).  
You can use this force field in your research according to the following information.

### Usage
1. Decompress the file `c36IDPSFF.tar.bz2`    
  
	*$ tar -jxvf c36IDPSFF.tar.bz2*

2. Enter the `c36IDPSFF` directory and you will find the force field files  
  
    *$ cd c36IDPSFF/*  
    *$ ls*  
	**charmm36IDPSFF.ff**  **README.md**  **test**  
 
3. Copy the force field `charmm36IDPSFF.ff` to your Gromacs force field directory  
  
	*$ cp -r charmm36IDPSFF.ff/ $GROMACS/share/gromacs/top*  
  
	[Note： $GROMACS is the directory where you install the Gromacs software.]  
	If you are neither a root user nor sudoer, and you have no permission to copy this folder  
	to $GROMACS/share/gromacs/top, you can put them into the place where you prepare  
	the .top and .gro files for simulation instead.  
  
	Example:  
    *$ cp -r charmm36IDPSFF.ff/ test/*  
    *$ cd test/*  
	  *$ gmx pdb2gmx -f test.pdb -o test.gro -water tip3p -p test.top -i test.itp -ignh*  
    ...  
    Select the Force Field:  
    From current directory:  
	1: CHARMM36IDPSFF all-atom force field (April 2018)  
    From $GROMACS/share/gromacs/top  
    2: AMBER03 force field (Duan et al., J. Comp. Chem. 24, 1999-2012, 2003)  
    3: AMBER03 protein, nucleic AMBER94 (Duan et al., J. Comp. Chem. 24, 1999-2012, 2003)  
    ...  
    [You can choose our force field by inputting "1" and then click "Enter"]  

### Reference  
When you publish or report results using CHARMM36IDPSFF force field, please cite this paper  

- H. Liu, D. Song, H. Lu, R. Luo and H. F. Chen. Intrinsically Disordered Protein Specific  
  Force Field CHARMM36IDPSFF, Chemical Biology & Drug Design, 2018, 92, 1722-1735.
  
