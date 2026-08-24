
# Activity 4, 5 & 6 – Azure Data Factory

## Objective

To implement an Azure Data Factory data integration pipeline that transfers a file from an on-premises file system to Azure Data Lake Storage Gen2.

## Technologies Used

- Azure Data Factory
- Self-hosted Integration Runtime
- Azure Data Lake Storage Gen2
- Azure Storage
- On-premises Windows VM

## Implementation

The following components were configured:

1. Self-hosted Integration Runtime
2. On-premises File System Linked Service
3. On-premises Source Dataset
4. ADLS Gen2 Linked Service
5. ADLS Gen2 Sink Dataset
6. Azure Data Factory Copy Data Pipeline

## Data Flow

On-Premises File  
↓  
Self-hosted Integration Runtime  
↓  
Azure Data Factory  
↓  
Copy Data Activity  
↓  
ADLS Gen2  
↓  
raw/ingest/sample.csv

## Resources Created

- Linked Service: `LS_Onprem_File195`
- Source Dataset: `DS_Onprem_File195`
- ADLS Linked Service: `LS_adls_ingest_kalyani`
- Sink Dataset: `DS_adls_ingest_195`
- Pipeline: `PL_Onprem_adls_ingest_195`

## Result

The pipeline was successfully debugged and the file was copied to:

`raw/ingest/sample.csv`

The output file was verified successfully in the Azure Storage browser.

## Conclusion

The on-premises file was successfully transferred to Azure Data Lake Storage Gen2 using Azure Data Factory and a Self-hosted Integration Runtime.
