
## Preamble

The source code provided in this repository is available under the [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/) license.

It is part of the submitted paper in the Metabolomics Journal, entitled : 

"Optimizing 1D 1H-NMR profiling of plant samples from extract preparation to spectra processing : standardisation, automation and high-throughput"

Authors: Catherine Deborde^1,2%^, Jean-Xavier Fontaine^3%^, Daniel Jacob^1,2^, Adolfo Botana^4^, Valérie Nicaise^5^, Florence Forget^5^, Sylvain Lecomte^3^, Cédric Decourtil^3^, Amar Hamadeh^3^, François Mesnard^3^, Annick Moing^1,2^, Roland Molinié^3^ 

* 1 UMR1332 Biologie du Fruit et Pathologie, INRA, Univ. Bordeaux, Centre INRA de Nouvelle Aquitaine Bordeaux, av Edouard Bourlaux, F-33140 Villenave d’Ornon, France
* 2 Plateforme Métabolome du Centre de Génomique Fonctionnelle Bordeaux, MetaboHUB, IBVM, Centre INRA de Nouvelle Aquitaine Bordeaux, av Edouard Bourlaux, F-33140 Villenave d’Ornon, France
* 3  BIOPI - EA 3900, Univ. Picardie Jules Verne, 33 rue Saint Leu, F-80039 Amiens, France
* 4  JEOL UK, Silver Court, Watchmead Road, Welwyn Garden City, AL7 1LT, UK
* 5  UR MycSA,INRA, Centre INRA de Nouvelle Aquitaine Bordeaux, av Edouard Bourlaux,  F-33140 Villenave d’Ornon, France
* % These two authors have contributed equally to this work 

# au_metabo
## AU program for metabolomic data acquisition
For each sample:
* 1 - MeOD signal (from the extraction solution) is used for the field/frequency lock
* 2 - Shims are optimized using the TopShim program for gradient shimming (Z1 to Z6) followed by trimming of (Z1, Z2, X, Y) shims.
* 3 - The 90°pulse length is determined with pulsecal module.

To use this AU program, the file “au_metabo” must be loaded in the folder  /opt/topspin(version)/exp/stan/nmr/au/src/user/.

It’s also necessary to registered the matrix of shim after 3D shim with name : “bestMeOD”. 

You must also load the “tunemetabo” file in the folder /opt/topspin(version)/exp/stan/nmr/lists/group/


# au_TMSPMeOH
## AU program for full width at half maximum (FWHM) 

The determination of the two selected spectra quality criteria full width at half maximum (FWHM) for TMSP and MeOD resonances are obtained with the au_TMSPMeOH  program


