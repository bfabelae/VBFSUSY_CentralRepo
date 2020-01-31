## Description of the contents of each folder above (Pileup studies with 2017 MC).

The contents on each folder (MC_NanoAODvX, X=5,6) above are:

  ### Tarballs:
  - `2017pileuphistos_nanoAODvX.tar.gz`: Tarball with all Pileup_nTrueInt histograms in PDF format for each MC sample.
  - `2017pileupratiocomparisons_nanoAODvX.tar.gz`: Tarball with all ratio plots (Pileup_nTrueInt / mc2017_pileup_Dec2018reReco) in PDF format for each MC sample.
  ### ROOT files:
  - `rawHistos_pucomp_<samples>NanoAODvX.root`: Pileup_nTrueInt distributions for each MC sample.
  - `pucomp_<samples>NanoAODvX.root`: Ratio histograms(Pileup_nTrueInt / mc2017_pileup_Dec2018reReco) for each MC sample. 
  - `discrepancy_pucomp_<samples>_NanoAODvX.root`: Ratio plots (Pileup_nTrueInt / mc2017_pileup_Dec2018reReco) for the samples that were classified under the category of "discrepancy"[1].
  - `nodiscrepancy_pucomp_<samples>_NanoAODvX.root`: Ratio plots (Pileup_nTrueInt / mc2017_pileup_Dec2018reReco) for the samples that were classified under the category of "no discrepancy" [1].

[1] **MC samples classification**.

  To classify the level of disagreement between the Pileup_nTrueInt distribution in each MC sample and the mc2017_pileup_Dec2018reReco used to apply pileup weights:
  1. Take the ratio plot and normal fit to a "flat-line" f(x) = 1 (ROOT), since we expect no differences between these distributions (therefore, the ratio should be equal to one).
  2. Calculate the chi2 / ndof value for each sample.
  3. Those samples whose fit results in:
      - a chi2 / ndof < 1.5 (1.5 s.d. \~ 90%) are categorized as having "_no discrepancy_",
      - a chi2 / ndof > 1.5, are classified as having a "_discrepancy_".
