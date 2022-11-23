# Introduction
This is annotation for the RAW-NOD dataset from our paper _GenISP: Neural ISP for Low-Light Machine Cognition_, CPRR NTIRE Workshop 2022
COCO-style annotation. We provide:
* COCO-style annotation for the whole dataset and for each camera subset separately (for RAW and RAWPY JPEG images).

## Subsets

| Dataset | Camera | #classes | #annotated images | #instances | #unannotated images |
|--- |--- |--- |--- |--- |--- |
| Sony | Sony RX100 VII | 3 | 3.2k | 18.7k | 0.9k |
| Nikon | Nikon D750 | 3 | 4.0k | 28.0k | 0 |
| NOD (in total) | Sony+Nikon | 3 | 7.2k | 46.7k | 0.9k |

## Development and test split

| Dataset | Train | Validation | Test | Comment | 
|--- |--- |--- |--- |--- |
| Sony | 80% | 10% | 10% | random split | 
| Nikon | 80% | 10% | 10% | random split |
| NOD (in total) | 80% | 10% | 10% | (Sony and Nikon combined) |


## Notes
* ```area``` is calculated as ```h*w``` of a bbox, 
* image and anno. ```id```s are created by enumeration (from 0 to #img) for each JSON file separately! _I.e._, image and anno. 
```id```s don't correspond to each other between annotation files. _E.g._, image with an ```"id":250``` in ```NOD_Sony_RX100m7_test.json``` is NOT the same as the image with the same ```"id":250``` in ```NOD_Sony_Nikon_test.json```.
