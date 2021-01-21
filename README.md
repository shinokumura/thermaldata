# Thermal-resonance ranges information table
This repository contains woking version of new thermal-resonance ranges information table (thermal-res-table.txt) released from CoNDERC homepage (https://nds.iaea.org/conderc).

# GENERAL
- Each of na.dat, nel.dat, ng.dat, np.dat file contains (n,a), (n,el), (n,g), (n,f) and (n,p) reaction data.
- Evaluated data are extracted from thermal-res-table.txt released from CoNDERC homepage (https://nds.iaea.org/conderc).
- EXFOR data are extracted from 'EXFOR-2020-10-28.bck.c5' file that was distributed by Viktor on Oct.2020.
- For the cross section data (sf6 = SIG), incident neutron energy range is from 0.0235 eV +/- 5%.
- In the EXFOR data table, the coulums are:
  -  dataset: EXFOR entry+subentry number
  -  firstauthor: Name of first author
  -  year: Year of the publication
  -  sf4: Reaction product
  -  sf5: Reaction branch
  -  sf8: Reaction modifiers
  -  sf9: Data type
  -  en: Incident neutron energy (somethimes average of between MIN and MAX)
  -  den: Uncertainty of incident neutron enery (en)
  -  ydata: Cross section in barn
  -  yddata: Uncertainty of cross section (ydata) in barn
- Summary table (resulttable.dat) contains Evaluated data, EXFOR mean value, and EXFOR MXW/SPA data mean for each nuclides.

# EXAMPLE
91-Pa-231 (n,g)
```
# Evaluated data
# Maxw.(n,g)                     |  (n,g)
#          NAN (+/-       NAN)   |     2.00E+02  (+/-  2.30E+00)  <--- Read from the 'thermal-res-table.txt'.
# EXFOR data mean
#     2.40E+02 (+/-  9.50E+00)    <--- Calculated from EXFOR data by exclusion of the case where the reaction product is in an isomeric state.
# EXFOR MXW/SPA data mean
#     2.11E+02 (+/-  2.00E+01)    <--- Calculated from EXFOR MXW/SPA data flagged in sf8.
# ------ EXFOR data ------
  dataset       firstauthor  year        sf4 sf8 sf9       en  den    ydata   yddata
 40163002  B.M.Aleksandrov+  1972  91-PA-232  --  -- 2.53E-02  NAN 2.60E+02 1.30E+01 
 40579003       L.N.Jurova+  1984  91-PA-232  --  -- 2.53E-02  NAN 2.19E+02 6.00E+00
# ------ MXW/SPA data ------
  dataset     firstauthor  year        sf4  sf8 sf9       en  den    ydata   yddata  
 12273002      R.R.Smith+  1956  91-PA-232  MXW  -- 2.53E-02  NAN 2.00E+02 1.50E+01 
 20634002  E.M.Gryntakis+  1974  91-PA-232  MXW  -- 2.53E-02  NAN 2.01E+02 2.20E+01 
 20634002  E.M.Gryntakis+  1974  91-PA-232  MXW  -- 2.53E-02  NAN 2.18E+02 1.40E+01 
 20691003     K.Kobayashi  1974  91-PA-232  MXW  -- 2.53E-02  NAN 2.01E+02 6.03E+00 
 23227002    T.Hashimoto+  1988  91-PA-232  MXW  -- 2.53E-02  NAN 1.86E+02 1.30E+01 
 12287002    G.T.Seaborg+  1946  91-PA-232  SPA  -- 2.53E-02  NAN 1.75E+02 2.62E+01 
 12272002        R.Elson+  1953  91-PA-232  SPA  -- 2.53E-02  NAN 2.93E+02 4.40E+01 
# ------ Recom./Eval./Deriv. data ------
  dataset     firstauthor  year        sf4 sf8    sf9       en  den    ydata   yddata  
 V1002566  S.F.Mughabghab  2006  91-PA-232  --  RECOM 2.53E-02  NAN 2.01E+02 2.30E+00
```

# SUMMARY TABLE
- Summary table is resulttable.dat.
- For (n,g) reaction, both Evaluated and Evaluated(MXW) taken from 'thermal-res-table.txt' are listed in column 3-6.
```
       target reaction    Eval.  Eval-err  Eval(MXW)  Eval(MXW)-err  EXFOR-data-mean  EXFOR-mean-err  MXW-data-mean  MXW-mean-err
        1-H-1    (n,g)      NAN       NAN   3.33E-01       7.00E-04         3.01E+00        2.36E-01       3.11E-01      6.23E-03
        1-H-2    (n,g) 5.08E-04  1.50E-05        NAN            NAN         4.99E-04        1.82E-05       6.30E-04      6.10E-05
       2-He-3    (n,g) 5.50E-05  3.00E-06        NAN            NAN         4.05E-05        7.93E-06       6.88E-05      1.50E-05
       2-He-4    (n,g)      NAN       NAN        NAN            NAN              NAN             NAN            NAN           NAN
       3-Li-6    (n,g) 3.93E-02  7.00E-04        NAN            NAN         3.93E-02        7.00E-04       3.81E-02      7.26E-03
       3-Li-7    (n,g) 4.42E-02  5.00E-04        NAN            NAN         4.43E-02        5.00E-04       4.01E-02      7.60E-03
       4-Be-7    (n,g)      NAN       NAN        NAN            NAN              NAN             NAN       1.55E-01           NAN
```
- For the other reactions, Evaluated data taken from 'thermal-res-table.txt' is listed in column 3-4.
```
      target reaction    Eval.  Eval-err  EXFOR-data-mean  EXFOR-mean-err  MXW-data-mean  MXW-mean-err
      2-He-3    (n,p) 5.33E+03  8.00E+00         5.66E+03        1.00E+03       5.04E+03      2.00E+02
      4-Be-7    (n,p) 3.88E+04  8.09E+02         4.63E+04        3.71E+03       4.68E+04      4.05E+03
      5-B-10    (n,p)      NAN       NAN              NAN             NAN       6.40E-03      1.47E-03
      7-N-14    (n,p) 1.86E+00  3.00E-02         1.93E+00        5.88E-02       1.72E+00      4.68E-02
    11-Na-22    (n,p) 2.78E+04  2.40E+03              NAN             NAN       3.06E+04      2.60E+03
    13-Al-26    (n,p) 1.97E+00  1.00E-02              NAN             NAN            NAN           NAN
     16-S-33    (n,p) 2.00E+00  1.00E+00              NAN             NAN       2.61E-02      2.00E-01
    17-Cl-35    (n,p) 4.89E-01  1.40E-02         4.89E-01        1.40E-02       3.96E-01      4.10E-02
    17-Cl-36    (n,p) 4.62E-02  4.00E-04         2.24E-01        5.10E-02       4.70E-02      2.00E-03
```
 
2021 9th Jan.
Shin

