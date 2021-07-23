# MESA single star models suite for binary models from "Detailed evolutionary models of massive contact binaries: I. Model grids and synthetic populations for the Magellanic Clouds"
## Author: Athira Menon, email: athira.menon89@gmail.com
### **MESA version: 10398**. Feel free to edit the files/ src code for future versions. 

There are two directories here corresponding to the single star models used in the evolution of a binary model with the following initial parameters: **P= 1.0 day, q= 0.9, M1+M2= Mtotal= 26 M☉**, located in:
https://github.com/athira11/massive_contact_binaries.git. It contains the initialization files, src  and make directories. To edit and create new single star models, please follow the steps below: 

1. To change the mass of the star:
In inlist1
```
save_model_filename = '12.3M_LMC.mod'

initial_mass = 12.3
``` 
2. To change the composition of the star: 

I have by entered by hand the individual elemental mass fraction corresponding to the LMC from Brott et al. 2011. These lines maybe edited as needed for the composition you
wish to relax your star to. 

In inlist1:
```
 ! BROTT+ 2011 LMC mixture, Z=0.0047
  num_accretion_species = 19

  accretion_species_id(1) = 'h1'
  accretion_species_xa(1) = 0.7391

  accretion_species_id(2) = 'he3'
  accretion_species_xa(2) = 1.651d-5

  accretion_species_id(3) = 'he4'
  accretion_species_xa(3) = 0.2562

  accretion_species_id(4) = 'c12'
  accretion_species_xa(4) = 4.988d-4

  accretion_species_id(5) = 'n14'
  accretion_species_xa(5) = 8.219d-5

  accretion_species_id(6) = 'o16'
  accretion_species_xa(6) = 2.64d-3

  accretion_species_id(7) = 'ne20'
  accretion_species_xa(7) = 6.405d-5

  accretion_species_id(8) = 'mg24'
  accretion_species_xa(8) = 1.990d-4

  accretion_species_id(9) = 'si28'
  accretion_species_xa(9) = 3.28d-4

  accretion_species_id(10) = 's32'
  accretion_species_xa(10) = 1.119d-06

  accretion_species_id(11) = 'ar36'
  accretion_species_xa(11) = 2.855d-7

  accretion_species_id(12) = 'ca40'
  accretion_species_xa(12) = 2.117d-6

  accretion_species_id(13) = 'ti44'
  accretion_species_xa(13) = 0.0

  accretion_species_id(14) = 'cr48'
  accretion_species_xa(14) = 0.0

  accretion_species_id(15) = 'cr56'
  accretion_species_xa(15) = 0.0

  accretion_species_id(16) = 'fe52'
  accretion_species_xa(16) = 0.0

  accretion_species_id(17) = 'fe54'
  accretion_species_xa(17) = 2.379d-6

  accretion_species_id(18) = 'fe56'
  accretion_species_xa(18) = 1.309d-3

  accretion_species_id(19) = 'ni56'
  accretion_species_xa(19) = 0.0

```
```
    Zbase = 0.0047d0
```

3. Finally, cd make and edit the directory path in makefile. Compile and run the model. 
```
./clean && ./mk
./rn
```

4. Once the .mod files are ready for your single stars, copy them to the binary model directory and follow the next steps to begin your binary evolution. 
