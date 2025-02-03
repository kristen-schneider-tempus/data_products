# Working with the creation and editing of tempus data_products

[Link to Jira Ticket](https://tempuslabs.atlassian.net/browse/BFXA-5513?atlOrigin=eyJpIjoiZGI4YWUxZmIyZDIyNGM3NmE0NDVkMzc0NDBkYTZlNTMiLCJwIjoiaiJ9)


1. Navigate to [Tempus Core Platform (TCP)](https://core-platform-console.securetempus.com/data-product-types/) and find the [`bfx-bed`](https://core-platform-console.securetempus.com/data-product-types/bfx-bed/) data product.

2. Navigate to [bioinf-rna-analysis/bedfile_workflow_RNAv2](`https://github.com/tempuslabs/bioinf-rna-analysis/tree/master/bedfile_workflow_RNAv2`) to find the bed file locations.
```
aws s3 ls s3://pipeline-refdata/bed/rs_v2_raw/

mkdir bed_files
aws s3 cp s3://pipeline-refdata/bed/rs_v2_raw/ ./bed_files 
    --recursive 
    --exclude "*"
    --include "*.bed"
```

