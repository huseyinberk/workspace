# Introduction 

Couchbase db platform iki farklı storage mekanizmasını destekler. Default olarak Couchstore ve Magma. 
- Couchstore belleğe sığabilen veri kümeleriyle çalışması için tasarlanmıştır
- Magma, belleğe sığmayan daha büyük veri kümelerinde yüksek performans gösterecek şekilde tasarlanmıştır

Magma, Couchbase'ın yeni depolama motoru, büyük veri setleri ve yoğun yazma yükleri için optimize edilmiştir. Magma, veri yoğunluğunu ve düğüm başına yazma performansını artırmak, yazma amplifikasyonunu (WA) azaltmak ve SSD'nin ömrünü uzatmak için tasarlanmıştır. Performans testleri, Magma'nın Couchstore ve RocksDB'den daha iyi performans gösterdiğini, özellikle bellekte sığmayan veri setleri için yazma yoğunluğu yüksek YCSB iş yüklerinde üstün olduğunu göstermiştir​[](https://www.couchbase.com/blog/magma-next-gen-document-storage-engine/)​.


| Criteria                     | Couchstore                                                                     | Magma                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum bucket memory quota  | 100MB                                                                          | 1GB                                                                                                      |
| Minimum memory to data ratio | 10%                                                                            | 1%                                                                                                       |
| Maximum data per node        | 3TB                                                                            | 10TB                                                                                                     |
| Data size optimization       | Best when the working dataset can fit into memory                              | Best when the working set is much larger than the available memory and you need disk access speed only   |
| Store and access             | Access data up to ~ 1TB                                                        | Store and access several terabytes of data                                                               |
| Hardware                     | Can run on low-end hardware                                                    | Quality hardware is preferred                                                                            |
| Supported services           | All services including full-text search, eventing, and analytics are available | All services including full-text search, eventing, and analytics are available with the 7.1.2 GA release |
| Data persistence             | Most data is accessed from the memory cache                                    | Applications need large amounts of persistent, durable data                                              |
| Use cases                    | Use case primarily requires memory access                                      | Use case primarily requires disk access                                                                  |
