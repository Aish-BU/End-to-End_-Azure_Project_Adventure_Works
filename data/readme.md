Here are clear questions and corresponding answers about creating a Data Lake and handling data redundancy in Azure:

### Q1: By default, does Azure create a Data Lake Storage Gen2 account when creating storage?
**Answer:**  
No. By default, Azure creates a **Blob storage account**, not a Data Lake Storage account.

### Q2: How do you explicitly create a Data Lake Storage Gen2 account instead of regular Blob storage?
**Answer:**  
When creating the storage account in Azure, ensure you **enable the hierarchical namespace**. Enabling this option creates a **Data Lake Storage Gen2 account**. If this is not enabled, Azure creates a standard Blob storage account instead.

### Q3: Which option must be enabled to create a Data Lake instead of Blob storage?
**Answer:**  
You must enable the **"Hierarchical namespace"** feature when creating the storage account.

### Q4: What type of data redundancy is recommended for this Data Lake scenario?
**Answer:**  
Use **Locally Redundant Storage (LRS)** for data redundancy. LRS replicates your data synchronously three times within the same data center, providing local redundancy without incurring the higher costs associated with geo-redundancy (GRS).

### Q5: Why select Locally Redundant Storage (LRS) instead of Geo-Redundant Storage (GRS)?
**Answer:**  
Selecting **LRS** reduces costs by replicating data only within the same Azure region, suitable for non-critical data scenarios or scenarios where cost management is important. **GRS**, on the other hand, is more expensive and suitable for highly critical applications requiring data replication across different geographic locations.
