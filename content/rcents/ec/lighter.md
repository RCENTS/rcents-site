---
title: Lighter
---

# Lighter bases

 | - | - | - | - |
 | Organism  |  Dataset | Pct Increase (Computed) | Pct Increase (Reported) | Difference |
 | - | - | - | - |
 | H. sapiens Chr 14 | GAGE | 1.67 | 0.74 | 0.93 |
 | C. elegans WS222 | SRR065390 | 0.62 | 0.43 | 0.19 |
 | E. coli K12 MG1655 | ERR022075 | 1.14 | 0.61 | 0.53 |
{: #lighterTableBases}


# Lighter reads

 | - | - | - | - |
 | Organism  |  Dataset | Pct Increase (Computed) | Pct Increase (Reported) | Difference |
 | - | - | - | - |
 | H. sapiens Chr 14 | GAGE | 0.93 | 0.91 | 0.02 |
 | C. elegans WS222 | SRR065390 | 0.21 | 0.10 | 0.11 |
 | E. coli K12 MG1655 | ERR022075 | 0.52 | 0.42 | 0.10 |
{: #lighterTableReads}


<script>
$(document).ready( function () {
    $('#lighterTableBases').DataTable({
        "paging":false,
        "columnDefs": [
            {
                "targets": -1,
                "className": 'dt-body-right'
            }
        ]
    });
    $('#lighterTableReads').DataTable({
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
