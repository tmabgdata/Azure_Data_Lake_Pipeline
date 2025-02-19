# Azure Data Lake: Creating an Ingestion Pipeline

This repository contains the project **Azure Data Lake: Creating an Ingestion Pipeline**, where a pipeline was developed for the ingestion, organization, and preparation of data in Azure Data Lake. The project uses non-emergency (311) service request data submitted by Boston residents between 2015 and 2020.

## Work Scenario

In recent years, the city of Boston has seen a significant increase in non-emergency service requests through the 311 system. Each request highlights an area of the city that needs improvement. To make more informed decisions, the Boston government requested the creation of an efficient Data Lake to process and store this data in a structured manner.

### Objective

The project's mission is to create an ingestion pipeline that ensures the extraction, compression, organization, and ingestion of data into **Azure Data Lake**, utilizing the **bronze**, **silver**, and **gold** layers to structure the data and prepare it for future analysis.

## Project Structure

### Project Steps

1. **Set up resources in Azure**

   - Create an Azure account.
   - Configure spending alerts and a resource group to manage the project's services.

2. **Create a storage account**

   - Configure **Blob Storage** as the primary repository for compressed data.

3. **Extract and compress data**

   - Use Python to extract data from Boston's official website:
     - [311 Service Requests - Official Website](https://data.boston.gov/dataset/311-service-requests)
   - Compress the extracted data to optimize storage.

4. **Upload data to Blob Storage**

   - Upload the compressed data to **Blob Storage** using Python.

5. **Create and structure the Data Lake**

   - Implement **Azure Data Lake Storage Gen 2**.
   - Adopt a layered approach:
     - **Bronze**: Raw and uncompressed data.
     - **Silver**: Transformed and validated data.
     - **Gold**: Data ready for analysis.

6. **Create a pipeline to copy data from Blob to the Data Lake**

   - Build a pipeline that transfers data from **Blob Storage** to the Data Lake.
   - Ensure the data is decompressed during the transfer to the **bronze** layer.

### Technologies Used

- **Microsoft Azure**
  - Blob Storage
  - Data Lake Storage Gen 2
- **Python**
  - Libraries: `os`, `zipfile`, `azure-storage-blob`, among others.
- **Planning and Management**
  - [Trello Board](https://trello.com/b/fOZD6D4K/azure-data-lake-criando-um-pipeline-de-ingestao-de-dados)

## Data Used

The 311 service requests represent non-emergency calls made by Boston citizens between 2015 and 2020.

- [311 Service Requests - Official Website](https://data.boston.gov/dataset/311-service-requests)
- Alternative links (in case the original site is unavailable):
  - [2015 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/c9509ab4-6f6d-4b97-979a-0cf2a10c922b/download/311_service_requests_2015.csv)
  - [2016 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/b7ea6b1b-3ca4-4c5b-9713-6dc1db52379a/download/311_service_requests_2016.csv)
  - [2017 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/30022137-709d-465e-baae-ca155b51927d/download/311_service_requests_2017.csv)
  - [2018 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/2be28d90-3a90-4af1-a3f6-f28c1e25880a/download/311_service_requests_2018.csv)
  - [2019 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/ea2e4696-4a2d-429c-9807-d02eb92e0222/download/311_service_requests_2019.csv)
  - [2020 Data](https://data.boston.gov/dataset/8048697b-ad64-4bfc-b090-ee00169f2323/resource/6ff6a6fd-3141-4440-a880-6f60a37fe789/download/script_105774672_20210108153400_combine.csv)

## Repository Organization

- `scripts/`: Python scripts used for data extraction, compression, and upload.
- `notebooks/`: Notebooks containing the pipeline's documentation and implementation.
- `resources/`: Additional documentation and useful links.
- `README.md`: This file.

## Trello Board

Task management was organized using [Trello](https://trello.com/b/fOZD6D4K/azure-data-lake-criando-um-pipeline-de-ingestao-de-dados).

## Contribution

Contributions are welcome! Feel free to open an *issue* or submit a *pull request*.

## Contact

Thiago Alves\
[GitHub](https://github.com/tmabgdata) | [LinkedIn](https://www.linkedin.com/in/thiago-bigdata/)

---

This project was developed as a case study to consolidate skills in data engineering and the use of the Azure platform.