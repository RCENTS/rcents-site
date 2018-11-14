---
title: RACER
---

# RACER

## RACER evaluation using Read Search
----

 | - | - | - | - |
 | Organism  |  Dataset | Gain (Computed) | Gain (Reported) | Difference |
 | - | - | - | - |
 |B. subtilis subtilis 168  | DRR000852  | 83.64   | 82.12 | 1.52 |
 |C. elegans WS222  | SRR065390  | 58.54   | 56.54 | 2.00 |
 |D. melanogaster R6.18  | SRR018292,SRR018293,SRR018294,SRR060098  | 38.85   | 42.95 | -4.10 |
 |E. coli K 12 MG1655  | SRR001665  | 90.78   | 86.32 | 4.46 |
 |E. coli K 12 MG1655  | SRR022918  | 39.26   |  56.50| -17.24 |
 |E. coli K 12 MG1655  | SRR396532  | 80.29   |  76.32| 3.97 |
 |E. coli K 12 MG1655  | SRR396536  | 86.78   |  83.58| 3.20 |
 |H. influenzae Rd KW20  | SRR065202  | 76.77   | 78.35| -1.58 |
 |L. interrogans str. 56601  | SRR353563  | 90.97   | 53.91 | 37.06 |
 |L. interrogans str. Fiocruz L1 130  | SRR397962  | 88.14   | 59.87 | 28.27 |
 |L. lactis  | SRR088759  | 97.63   | 80.49 | 17.14 |
 |P. aeruginosa PAO1  | SRR396641  | 86.73   | 85.32 | 1.41 |
 |S. aureus MW2  | SRR022866  | 26.89   | 25.96 | 0.93 |
 |S. cerevisiae S288C  | SRR352384  | 13.59   | 12.25 | 1.34 |
 |T. pallidum  | SRR361468  | 78.77   | 85.75 | -6.98 |
{: #racerTableSS}

---

## RACER evaluation with BWA
----

 | - | - | - | - |
 | Organism  |  Dataset | Gain (Computed) | Gain (Reported) | Difference 
 | - | - | - | - |
 |  B. subtilis subtilis 168 | DRR000852 | 26.26  | 93.55 | -67.29 |
 |  C. elegans WS222 | SRR065390 |  9.29  | 65.96 | -56.67 |
 |  D. melanogaster R6.18 | SRR018292,SRR018293,SRR018294,SRR060098 |  28.15  | 57.04 | -28.89 |
 |  E. coli K 12 MG1655 | SRR001665 |  78.44  | 82.67 | -4.23 |
 |  E. coli K 12 MG1655 | SRR022918 |  31.18  | 90.80 | -59.62 |
 |  E. coli K 12 MG1655 | SRR396532 |  56.99  | 83.91 | -26.92 |
 |  E. coli K 12 MG1655 | SRR396536 |  85.23  | 77.80 | 7.43 |
 |  H. influenzae Rd KW20 | SRR065202 |  50.85  | 84.33 | -33.48 |
 |  L. interrogans str. 56601 | SRR353563 |  34.88  | 89.27 | -54.39 |
 |  L. interrogans str. Fiocruz L1 130 | SRR397962 |  29.09  |  90.81 | -61.72 |
 |  L. lactis | SRR088759 |  95.93  | 92.02 | 3.91 |
 |  P. aeruginosa PAO1 | SRR396641 | 48.34 | 89.31 | -40.97 |
 |  S. aureus MW2 | SRR022866 |  12.25  | 47.00 | -34.75 |
 |  S. cerevisiae S288C | SRR352384 |  8.35  | 14.68 | -6.33 |
 |  T. pallidum | SRR361468 |  77.42  | 92.35 | -14.93 |
{: #racerTableBWA}

----


<script>
$(document).ready( function () {
    $('#racerTableSS').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            }
        ]
    });
    $('#racerTableBWA').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            }
        ]
    });
} );
</script>
