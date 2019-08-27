---  
title:  Fiona
---  

# Fiona Error Correction

----

| Docker Image   | <%= Octicons::Octicon.new("gear").to_svg %>  [rcents/im:fiona](https://hub.docker.com/r/rcents/im) |
| Publication | <%= Octicons::Octicon.new("file").to_svg %>  [doi:10.1093/bioinformatics/btu368](https://doi.org/10.1093/bioinformatics/btu440)  |
| Homepage | <%= Octicons::Octicon.new("home").to_svg %> [SeqAn](http://www.seqan.de/apps/fiona/)                                     |
| Source  | <%= Octicons::Octicon.new("repo").to_svg %> [github/seqan](https://github.com/seqan/seqan/tree/master/apps/fiona) |
| Reproducibility Scripts | <%= Octicons::Octicon.new("beaker").to_svg %>  [RCENTS/ec/fiona](https://github.com/RCENTS/ec/tree/master/runs/fiona) |
{: #imagefiona1}

----

## Evaluation Metric

----

From the paper:

> For the evaluation of read correction quality, the metric gain
> has been established in (Yang et al., 2010, 2013) as a good 
> summary of both sensitivity and precision. The gain can be computed
> by (b−a)/b where a and b are the sums over the number of errors after 
> and before correction over all reads. When more errors are introduced 
> than corrected over all the reads, the gain takes a negative value. 
> For the evaluation, we developed a tool compute_gain, which is 
> included in the Fiona distribution.

----

## Parameter Selection

----

----

### Datasets

----

#### Illumina Datasets

----

| Organism        | Accession | Avg. Length | Read Count | Coverage |
| --------------- | --------- | ----------- | ---------- | -------- |
| C. elegans      | SRR443373 | 100 bp      | 29 657 035 | 30X      |
| D. melanogaster | SRR492060 | 76 bp       | 51 727 822 | 28X      |
| E. coli K-12    | ERR022075 | 100 bp      | 22 720 100 | 490X     |
| P. syringae     | ERR005143 | 36 bp       | 14 204 532 | 42X      |
| S. cerevisae    | SRR031259 | 36 bp       | 7 485 708  | 22X      |

#### 454 Datasets

----

| Organism        | Accession | Avg. Length | Read Count | Coverage |
| --------------- | --------- | ----------- | ---------- | -------- |
| D. melanogaster | SRX016210 | 544 bp      | 4 692 486  | 18X      |
| E. coli K-12    | SRR000868 | 253 bp      | 230 517    | 13X      |
| S. aureus       | SRR070596 | 514 bp      | 185 384    | 34X      |
| S. cerevisae    | SRX039441 | 274 bp      | 690 237    | 16X      |

#### Ion Torrent Datasets

| Organism      | Accession  | Avg. Length | Read Count  | Coverage |
| ------------- | ---------- | ----------- | ----------- | -------- |
| B.pertussis   | ERR161541  | 142 bp      | 2 464 690   | 85 X     |
| E. coli K-12  | ERR039477  | 92  bp      | 390 976     | 8X       |
| E. coli K-12  | SRR611140  | 162 bp      | 4 669 065   | 163X     |
| E. coli K-12  | SRR620425  | 170 bp      | 4 237 734   | 156X     |
| E. coli K-12  | SRR254209  | 178 bp      | 977 971     | 32X      |
| H. sapiens    | SRR1238539 | 177 bp      | 186 132 134 | 11X      |
| P. falciparum | ERR161543  | 154 bp      | 1 959 564   | 13X      |
| S. aureus     | ERR236069  | 228 bp      | 1 338 465   | 109X     |

----


### Results

----

All the datasets except C.elegans were run for Illumina. 
- C. elgans couldnt complete within the allocated time of 48 hours per task!

All the datasts for 454 were run sucessfully.

H. sapiens, P. falciparum  and S. aureus  failed for Ion Torrent because of out of time failures.

#### Dataset:  SRR034841-4  (D. melanogaster)

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

#### Dataset:  SRR000868  (E. coli K-12 MG1655)

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

#### Dataset:  SRR096469-70  (S. cerevisae S288C)

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

#### Dataset:  SRR070596 (S. aureus LGA251)

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
