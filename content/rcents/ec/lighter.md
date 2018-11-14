---
title: Lighter
---

# Lighter bases

 | - | - | - | - |
 | Organism  |  Dataset | Pct Increase (Computed) | Pct Increase (Reported) | Difference |
 | - | - | - | - |
 | H. sapiens Chr 14 | GAGE | 1.67 | | |
 | C. elegans WS222 | SRR065390 | 0.62 | | |
 | E. coli K12 MG1655 | ERR022075 | 1.14 | | |
{: #lighterTableBases}


# Lighter reads

 | - | - | - | - |
 | Organism  |  Dataset | Pct Increase (Computed) | Pct Increase (Reported) | Difference |
 | - | - | - | - |
 | H. sapiens Chr 14 | GAGE | 0.00933647082028 | | |
 | C. elegans WS222 | SRR065390 | 0.00209288799347 | | |
 | E. coli K12 MG1655 | ERR022075 | 0.00516073872914 | | |
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
