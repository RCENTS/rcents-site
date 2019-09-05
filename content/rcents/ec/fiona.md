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

## Summary

All the Illumina datasets except __C.elegans__ were successfully run. __C. elgans__ dataset couldnt complete within the allocated time of 48 hours per run. All the datasts for 454 were sucessfully run. Among the Ion Torrent datasets, __H. sapiens__, __P. falciparum 3D7__  and __S. aureus__ datasets failed to complete within the allocated time.

In case of Illumina datasets, all the datasets that successfully ran show performance closer to the reported performance.
In case of 454 datasets, there is a siginficant deviation (more than 10 points for *Gain*) from the reported performance.
In case of Ion Torrent datasets, except for the __SRR620425  (E. coli K-12 MG1655)__ dataset, all other show significant (more than 10 points) difference between the claimed performance and the computed performance.


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

Paramters were selected as given in the __Supplementary Details__ document (Page 6):

> We used paramter -t 8 for eight threads, and pass teh genome length using
> -g GLEN. ... Fiona uses a default error rate of 0.05 and Fiona-H for Illumina
> uses a default of 0.01


----

### Datasets

----

#### Illumina Datasets

----

| Organism        | Accession | Avg. Length | Read Count | Coverage | Read Count (Obs.) |
| --------------- | --------- | ----------- | ---------- | -------- | ----------------- |
| C. elegans      | SRR443373 | 100 bp      | 29 657 035 | 30X      | 166,079,398       |
| D. melanogaster | SRR492060 | 76 bp       | 51 727 822 | 28X      | 51,727,822        |
| E. coli K-12    | ERR022075 | 100 bp      | 22 720 100 | 490X     | 45,440,200        |
| P. syringae     | ERR005143 | 36 bp       | 14 204 532 | 42X      | 7,102,266         |
| S. cerevisae    | SRR031259 | 36 bp       | 7 485 708  | 22X      | 7,485,708         |
 {: #fionaDatasetTable1}
----

#### 454 Datasets

----

| Organism        | Accession | Avg. Length | Read Count | Coverage | Read Count (Obs.) |
| --------------- | --------- | ----------- | ---------- | -------- | ----------------- |
| D. melanogaster | SRX016210 | 544 bp      | 4 692 486  | 18X      | 4,930,981         |
| E. coli K-12    | SRR000868 | 253 bp      | 230 517    | 13X      | 230,517           |
| S. aureus       | SRR070596 | 514 bp      | 185 384    | 34X      | 185,384           |
| S. cerevisae    | SRX039441 | 274 bp      | 690 237    | 16X      | 690,237           |
 {: #fionaDatasetTable2}
----

#### Ion Torrent Datasets

| Organism      | Accession  | Avg. Length | Read Count  | Coverage | Read Count (Obs.) |
| ------------- | ---------- | ----------- | ----------- | -------- | ----------------- |
| B.pertussis   | ERR161541  | 142 bp      | 2 464 690   | 85X      |                   |
| E. coli K-12  | ERR039477  | 92  bp      | 390 976     | 8X       | 390,976           |
| E. coli K-12  | SRR611140  | 162 bp      | 4 669 065   | 163X     | 4,669,065         |
| E. coli K-12  | SRR620425  | 170 bp      | 4 237 734   | 156X     | 4,237,734         |
| E. coli K-12  | SRR254209  | 178 bp      | 977 971     | 32X      | 977,971           |
| H. sapiens    | SRR1238539 | 177 bp      | 186 132 134 | 11X      | 186,132,134       |
| P. falciparum | ERR161543  | 154 bp      | 1 959 564   | 13X      |                   |
| S. aureus     | ERR236069  | 228 bp      | 1 338 465   | 109X     | 1,338,465         |
 {: #fionaDatasetTable3}

----


### Results

----

All the Illumina datasets except __C.elegans__ were successfully run. __C. elgans__ dataset couldnt complete within the allocated time of 48 hours per run. All the datasts for 454 were sucessfully run. Among the Ion Torrent datasets, __H. sapiens__, __P. falciparum 3D7__  and __S. aureus__ datasets failed to complete within the allocated time.

#### Dataset:  ERR005143  (P. syringae)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 95.67    | 91.36    | 4.31       |
| 2 | Sensitivity | 97.58    | 95.50    | 2.08       |
| 3 | Specificity | 99.99    | 100.00   | -0.01      |
 {: #fionaTable1}
----

#### Dataset:  SRR492060  (D. melanogaster)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 28.02    | 31.39    | -3.37      |
| 2 | Sensitivity | 34.01    | 34.30    | -0.29      |
| 3 | Specificity | 99.88    | 100.00   | -0.12      |
 {: #fionaTable2}
----


#### Dataset:  SRR031259  (S. cerevisae S288C)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 53.30    | 58.89    | -5.59      |
| 2 | Sensitivity | 77.41    | 78.00    | -0.59      |
| 3 | Specificity | 99.91    | 99.90    |  0.01      |
 {: #fionaTable3}
----


#### Dataset:  ERR022075  (E. coli K-12 MG1655)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 92.64    | 98.66    | -6.02      |
| 2 | Sensitivity | 93.91    | 99.20    | -5.29      |
| 3 | Specificity | 99.99    | 100.00   | -0.01      |
 {: #fionaTable4}
----

#### Dataset:  SRR034841-4  (D. melanogaster)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 14.63    | 64.62    | -49.09     |
| 2 | Sensitivity | 32.48    | 9.5      | 21.98      |
| 3 | Specificity | 98.15    | 100.00   | -1.85      |
 {: #fionaTable5}
----


#### Dataset:  SRR000868  (E. coli K-12 MG1655)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 50.18    | 76.88    | -26.70     |
| 2 | Sensitivity | 66.09    | 56.2     | 9.89       |
| 3 | Specificity | 99.48    | 100.00   | -0.52      |
 {: #fionaTable6}
----


#### Dataset:  SRR096469-70  (S. cerevisae S288C)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 4.66     | 36.04    | -32.62     |
| 2 | Sensitivity | 47.06    | 40.01    | 7.05       |
| 3 | Specificity | 92.43    | 100.00   | -7.57      |
 {: #fionaTable7}
----

#### Dataset:  SRR070596  (S. aureus LGA251)

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 13.04    | 69.87    | -56.83     |
| 2 | Sensitivity | 25.22    | 27.20    | -2.02      |
| 3 | Specificity | 98.22    | 99.90    | -1.72      |
 {: #fionaTable8}
----

#### Dataset:  ERR039477  (E. coli K-12 MG1655)

The paper doesn't report Sensitivity and Specificity for this dataset.

|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 59.83    | 90.52    | -40.69     |
| 2 | Sensitivity | 71.61    |   NA     |    NA      |
| 3 | Specificity | 99.84    |   NA     |    NA      |
 {: #fionaTable9}
----

#### Dataset:  SRR611140  (E. coli K-12 MG1655)


|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 72.19    | 81.24    | -9.05      |
| 2 | Sensitivity | 76.83    | 84.60    | -7.77      |
| 3 | Specificity | 99.92    | 100.0    | -0.08      |
 {: #fionaTable10}
----

#### Dataset:  SRR254209  (E. coli O104:H4)


|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 11.31    | 69.33    | -58.02     |
| 2 | Sensitivity | 31.00    | 76.10    | -45.10     |
| 3 | Specificity | 95.89    | 99.70    | -3.91      |
 {: #fionaTable11}
----

#### Dataset:  ERR161541  (B. pertussis 18323)


|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 20.58    | 72.83    | -51.15     |
| 2 | Sensitivity | 51.87    | 77.80    | -25.93     |
| 3 | Specificity | 95.76    | 99.80    | -4.04      |
 {: #fionaTable12}
----


#### Dataset:  SRR620425  (E. coli K-12 MG1655)


|   | Stat        | Computed | Reported | Difference |
| - | ----------- | -------- | -------- | ---------- |
| 1 | Gain        | 70.36    | 74.06    | -3.70      |
| 2 | Sensitivity | 73.53    | 76.60    | -3.07      |
| 3 | Specificity | 99.96    | 100.0    | -0.04      |
 {: #fionaTable13}
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
    $('#fionaTable5').DataTable({
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
    $('#fionaTable6').DataTable({
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
    $('#fionaTable7').DataTable({
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
    $('#fionaTable8').DataTable({
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
    $('#fionaTable9').DataTable({
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
    $('#fionaTable10').DataTable({
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
    $('#fionaTable11').DataTable({
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
    $('#fionaTable12').DataTable({
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
    $('#fionaTable13').DataTable({
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
    $('#fionaDatasetTable1').DataTable({
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
    $('#fionaDatasetTable2').DataTable({
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
    $('#fionaDatasetTable3').DataTable({
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
