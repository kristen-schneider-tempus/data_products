# Working with the creation and editing of tempus data_products

[Link to Jira Ticket](https://tempuslabs.atlassian.net/browse/BFXA-5513?atlOrigin=eyJpIjoiZGI4YWUxZmIyZDIyNGM3NmE0NDVkMzc0NDBkYTZlNTMiLCJwIjoiaiJ9)

### Important Data and Git Repositories
[Tempus Core Platform (TCP)](https://core-platform-console.securetempus.com/data-product-types/) [`bfx-bed`](https://core-platform-console.securetempus.com/data-product-types/bfx-bed/) data product.

[REPO: bioinf-rna-analysis/bedfile_workflow_RNAv2](`https://github.com/tempuslabs/bioinf-rna-analysis/tree/master/bedfile_workflow_RNAv2`) to find the bed file locations.
This bucket contiains input bed files (coordinates of probes); which are mostly 120nt in length.
```
aws s3 ls s3://pipeline-refdata/bed/rs_v2_raw/

mkdir bed_files
aws s3 cp s3://pipeline-refdata/bed/rs_v2_raw/ ./bed_files 
    --recursive 
    --exclude "*"
    --include "*.bed"
```

[REPO: bioinf-rna](https://github.com/tempuslabs/bioinf-rna)



### Helful Resources
- [Tempus Data Model Molecular Handbook](https://docs.google.com/document/d/1Bb1G79CtwttkIjOtEiCh3RNXg6DU3A0XpK6WltEKezM/edit?tab=t.0#heading=h.pfbkcxyt3abb)

- [Tempus Tech Handbook--Data Products](https://tech-handbook.opstempus.com/tempus-os/data-products/)

- [Tempus Core Platform (TCP)](https://core-platform-console.securetempus.com/data-product-types/)

- [Jerod Parsons--Producer of Bioinformatics Data Products SOP](https://docs.google.com/document/d/1YjxD_dP4rBSDdYbeSCY9-fT9x0ZDHSBGHtf66Cw-11E/edit?tab=t.0#heading=h.e0xzlmtjocrs)

- [Genelle Harrison--How to update a data product](https://docs.google.com/document/d/1nnU6M1y6tzgQKvDMVY007ssLAuuvJBmeMWvY6eWCWm4/edit?tab=t.0)

- [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/s3/ls.html)