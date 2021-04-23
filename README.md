# one-spe
**One Solid-Phase Extraction for ~~-all-~~ most Proteomics Workflows**

Ever since I encountered my first samples where a polymer or detergent, unbeknown to me, was present and had to suffer through column and instrument cleanup I've wanted a simple, unified and robust method of sample cleanup following every Trypsin digestion so that my system would never have to suffer contamination again.  

Various methods abound in the literature for removing detergents which may also work for polymers, some are more effective than others but tended to lack the simplicity and robustness I required.  Almost 8 years ago when I started using sodium deoxycholate (SDC) to improve Trypsin digest workflows my quest for an easy method amenable to scale up in either volume or sample number began.

My goal was to use a solid phase support which would bind Tryptic peptides but not neutral or negatively charged molecules and have good recovery of the applied peptides.  The obvious choice was a cation exchange material.  This support also must not contaminate the sample with leachables and be able to withstand the very high pH of the elution solvent. This last requirement rules out the use of silica based cation exchangers.  

And finally the solvent for eluting the peptides needed to be completely volatile; easily evaporated in a centrifugal vacuum lyophilizer such as a speed-vac.  I prefer not to use a trap column but rather directly inject the sample onto the capillary column for LC/MS/MS.  Therefore, at the end of the workflow the sample must be completely MS compatible.

This required some tweaks to the Trypsin digestion buffer.  Typically TRIS-HCl pH 8 - 8.5 is used as the buffer.  One reason is that since it contains a reactive amine group it should act as a scavenger for amine reactive species that may be generated during the sample workup e.g. during reduction and alkylation steps or if Urea is present.  However, I discovered that even in the presence of 100mM TRIS-HCl if the buffer also contained 8M Urea a small percentage of peptides would contain carbamylated modifications.  That is when I stoped using Urea and now I use SDC as the denaturing agent because Trypsin retains a high percentage of its proteoltic activity even at high concentrations of SDC up to 10%. See [Lin et. al.](http://dx.doi.org/10.1016/j.ab.2008.03.009) This compatibility is not unexpected since deoxycholate is a bile acid that is present along with Trypsin in the small intestine. See [Wikipedia - Deoxycholate](https://en.wikipedia.org/wiki/Deoxycholic_acid).

The other problem with Tris-HCL is that it is cationic.  So it along with Tryptic peptides will bind to a cation exchanger.  HEPES on the other hand is anionic so will not be retained by a cation exchange support.  And happily there are recent reports of HEPES used with good success for Tryptic digests.  See [Goodman et.al.](http://dx.doi.org/10.1002/pmic.201800236).

SDC is anionic so will not be retained by a cation exchanger.  However, SDC has a few idiosyncracies.  The main one is that it precipitates in acid conditions.  Acid was originally used to remove SDC from the digest, sometimes combined with solvent extraction using ethyl acetate then final cleanup using a reversed phase support e.g C18 tips.  This is nasty laborious and prone to increase variability in recovery of the peptides. It also doesn't remove other detergents that may be lurking from upstream protein based workflows e.g. affinity pull-down etc. Totally not a good nor comprehensive workflow to make the sample MS compatible.  Also SDC doesn't play well with calcium.  Those who add calcium to stabilize Trypsin be warned. 

A problem for single step cation exchange SPE is created because of this acid insolubility property of SDC.  You have to acidify the Trypsin digest so that the peptides become protonated on the basic sites and subsequently this positive charge will allow the peptides to be retained by the cation exchanger. The negatively charged and neutral molecules will pass through but SDC is insoluble in acidic conditions so it will just plug up the SPE device.  Since acidified SDC is soluble in ethyl acetate, I hypothesized that by adding a water miscible organic solvent like acetonitrile to the digest along with an acid such as formic or trifluoroacetic acid the acidified solvent should keep SDC soluble allowing the diluted digest to easily pass through the solid phase cation exchange support. That is the case and has been published by other labs.  See: [Humphrey et. al.] (https://doi.org/10.1038/s41596-018-0014-9).

The result of all this is a highly efficient and reproducible sample cleanup that can be directly injected onto a capillary column for LC/MS/MS analysis.  
