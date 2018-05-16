---
title: Summary of Results
---

# Summary of Results


----

## Reptile 

 | - | - | - |
 | Dataset  | Gain  | Mapping Percentage  |
 | - | - | - |
 | SRR2301 | 0.81   | 95.66   |
 | SRR2312 | 0.72   | 98.88   |
 | SRR3452 | 0.93   | 83.44   |
 | SRR2234 | 0.64   | 98.98   |
{: #reptileTable}


----

## RACER

 | - | - | - |
 | Dataset  |  Read Depth Gain | Kmer Depth Gain |
 | - | - | - |
 | SRR2302 | 0.72   | 0.88   |
 | SRR3462 | 0.93   | 0.90   |
 | SRR2294 | 0.64   | 0.75   |
{: #racerTable}

----


<script>
$(document).ready( function () {
    $('#reptileTable').DataTable({
        "paging":   false,
        "info":     false 
    });
    $('#racerTable').DataTable({
        "paging":   false,
        "info":     false 
    });
} );
</script>
