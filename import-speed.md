## Partial dataset 330k records

papaparse events - 4.61, 4.92, 4.58
csv-parse events - 5.61, 5.58, 5.5
csv-parse cast values function - 13.74
node-gtfs version of csv-parse events @9_000 variables - 5.15, 5.10, 5.06
papaparse pipeline - 13.36, 13.47

## Complete dataset GTFS_ALL.ZIP

- papa-parse - 815.59 seconds ( 13.59 minutes )
- papa-parse wrap w/ transaction - 779.55, 809 seconds
- papa-parse wrap w/ pragma - 296.86, 302.57 seconds ( 5.05 minutes )
- papa-parse wrap w/ pragma & transactions - 277.438, 297.76 seconds
- node-gtfs insert at 800 record default - 1087.14 seconds ( 18.11 minutes )
- node-gtfs insert at 8_000 records - 519.09 seconds, 501 ( 8.65 minutes )
- node-gtfs insert at 20_000 records - 382.40 seconds, 411 ( 6.37 minutes )
- node-gtfs insert at 30_000 records - 402 seconds, 411 ( 6.37 minutes )

## Complete dataset, skip database insert

- papa-parse - 67.92 seconds
- papa-parse w/ prepared values - 79.24 seconds
- papa-parse pipeline for await loop - 370.66 seconds :(
- node-gtfs 800 records - 213.34 seconds
- node-gtfs 8_000 records - 170.78 seconds
- node-gtfs 20_000 records - 161.99 seconds

## 330k record dataset

- papa-parse - 4.73, 4.78, 4.66 seconds
- papa-parse w/ pragma & transaction - 4.43, 4.789, 4.713 seconds
- papa-parse w/ transaction queries - 4.66, 4.91, 4.8 seconds
- papa-parse w/ global transaction - 4.76, 4.699, 4.695 seconds
- papa-parse w/ prepared values but skip insert - 1.553 seconds
