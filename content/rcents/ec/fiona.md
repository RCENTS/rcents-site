---  
title:  Fiona
---  


## DATASET :  SRR034841,SRR034842,SRR034843,SRR034844  ORGANISM :  D. melanogaster

          ----

 | --- | ----------- | -------- | --------- | ---------- |
 |     | Stat        | Computed | Reported  | Difference |
 | --- | ----------- | -------- | --------- | ---------- |
 | 1   | Sensitivity | 32.4845  | 67.9      | -35.4155   |
 | 2   | Specificity | 98.1484  | 100       | 1.8516     |
 | 3   | TP          | 90950036 | 3,097,392 | 87852644   |
 | 4   | FP          | 49997483 | 151,321   | 49846162   |
 | 5   | Gain        | 14.6269  | 64.62     | -49.9931   |

 {: #fionaTable1}
----


## DATASET :  SRR000868  ORGANISM :  E. coli K-12 MG1655

          ----

 | --- | ----------- | -------- | -------- | ---------- |
 |     | Stat        | Computed | Reported | Difference |
 | --- | ----------- | -------- | -------- | ---------- |
 | 1   | Sensitivity | 66.0931  | 67.9     | -1.8069    |
 | 2   | Specificity | 99.4821  | 100.0    | -0.5179    |
 | 3   | TP          | 1278102  | 257,697  | 1020405    |
 | 4   | FP          | 307744   | 6379     | 301365     |
 | 5   | Gain        | 50.1791  | 76.88    | -26.7009   |

 {: #fionaTable2}
----


## DATASET :  SRR096469,SRR096470  ORGANISM :  S. cerevisae S288C

          ----

 | --- | ----------- | -------- | -------- | ---------- |
 |     | Stat        | Computed | Reported | Difference |
 | --- | ----------- | -------- | -------- | ---------- |
 | 1   | Sensitivity | 47.0641  | 40.1     | 6.9641     |
 | 2   | Specificity | 92.4307  | 100.0    | -7.5693    |
 | 3   | TP          | 21979851 | 185,299  | 21794552   |
 | 4   | FP          | 19803756 | 18633    | 19785123   |
 | 5   | Gain        | 4.65954  | 36.04    | -31.38046  |

 {: #fionaTable3}
----

## DATASET :  SRR070596  ORGANISM :  S. aureus LGA251

          ----

 | --- | ----------- | -------- | -------- | ---------- |
 |     | Stat        | Computed | Reported | Difference |
 | --- | ----------- | -------- | -------- | ---------- |
 | 1   | Sensitivity | 25.2178  | 35.2     | -9.9822    |
 | 2   | Specificity | 98.2167  | 100.0    | -1.7833    |
 | 3   | TP          | 3359501  | 84       | 3359417    |
 | 4   | FP          | 1622568  | 7        | 1622561    |
 | 5   | Gain        | 13.0381  | 69.87    | -56.8319   |

 {: #fionaTable4}
----
 
<script>
$(document).ready( function () {
    $('#fionaTable1').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            },
            {
                "targets": -2,
                "className": 'dt-body-right'
            }
        ]
    });
    $('#fionaTable2').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            },
            {
                "targets": -2,
                "className": 'dt-body-right'
            }
        ]
    });
    $('#fionaTable3').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            },
            {
                "targets": -2,
                "className": 'dt-body-right'
            }
        ]
    });
    $('#fionaTable4').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            },
            {
                "targets": -2,
                "className": 'dt-body-right'
            }
        ]
    });
} );
</script>

														






