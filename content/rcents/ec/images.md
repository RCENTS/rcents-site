---
title: Images
---

# Short Read Error Correction
----


## rcents/im:blue

| Docker Image   | <%= Octicons::Octicon.new("gear").to_svg %>  [rcents/im:blue](https://hub.docker.com/r/rcents/im) |
| Publication | <%= Octicons::Octicon.new("file").to_svg %>  [doi:10.1093/bioinformatics/btu368](https://doi.org/10.1093/bioinformatics/btu368)  |
| Homepage | <%= Octicons::Octicon.new("home").to_svg %> [CSIRO/blue](http://bioinformatics.csiro.au/blue)                                     |
| Source  | <%= Octicons::Octicon.new("repo").to_svg %> [github/PaulGreenfieldOz](https://github.com/PaulGreenfieldOz/WorkingDogs/tree/master/Blue) |
{: #imageblue}

----


<script>
$(document).ready( function () {
    $('#imageblue').DataTable({
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
