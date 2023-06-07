---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Alissa Trujillo
---

## 1.2 

### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     |
| 1024x768 PNG image                         | 0.79-4.72 MB  |
| 1024x768 RAW image                         | 1.18-1.38 MB  | 
| HD (1080p) HEVC Video (15 minutes)         | ? MB          |
| HD (1080p) Uncompressed Video (15 minutes) | ? MB          |
| 4K UHD HEVC Video (15 minutes)             | ? MB          |
| 4k UHD Uncompressed Video (15 minutes)     | ? MB          |
| Human Genome (Uncompressed)                | ? GB          |

#### Explanation:

 - Characters: each character is one byte
 - PNG: Can be stored from 8-48 bits per pixel, range is multiplied
        by the resolution
 - RAW: Can be stored from 12-14 bits per pixel, range is multiplied
        by the resolution
 - HEVC

### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | ??       |      |
| Daily Twitter Tweets (Snappy Compressed)  | ??       |      |
| Daily Instagram Photos                    | ??       |      |
| Daily YouTube Videos                      | ??       |      |
| Yearly Twitter Tweets (Uncompressed)      | ??       |      |
| Yearly Twitter Tweets (Snappy Compressed) | ??       |      |
| Yearly Instagram Photos                   | ??       |      |
| Yearly YouTube Videos                     | ??       |      |

### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | ??   |            |
| Twitter Tweets (Snappy Compressed) | ??   |            |
| Instagram Photos                   | ??   |            |
| YouTube Videos                     | ??   |            |

### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | ? ms                 |
| Low Earth Orbit Satellite | ? ms                 |
| Geostationary Satellite   | ? ms                 |
| Earth to the Moon         | ? ms                 |
| Earth to Mars             | ? minutes            | 


### References

https://docs.oracle.com/cd/E19253-01/817-6223/chp-typeopexpr-2/index.html
https://learn.microsoft.com/en-us/windows/win32/gdiplus/-gdiplus-types-of-bitmaps-about
https://en.wikipedia.org/wiki/Raw_image_format