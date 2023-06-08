---
title: Assignment 1
subtitle: Computer Performance, Reliability, and Scalability Calculation
author: Alissa Trujillo
---

## 1.2 

### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Bytes     |
| 1024x768 PNG image                         | 0.79-4.72 MB  |
| 1024x768 RAW image                         | 1.18-1.38 MB  | 
| HD (1080p) HEVC Video (15 minutes)         | 300 MB        |
| HD (1080p) Uncompressed Video (15 minutes) | 135000 MB     |
| 4K UHD HEVC Video (15 minutes)             | 1200 MB       |
| 4k UHD Uncompressed Video (15 minutes)     | 540000 MB     |
| Human Genome (Uncompressed)                | 1.5 GB        |

#### Explanation:

 - Characters: each character is one byte
 - PNG: Can be stored from 8-48 bits per pixel, range is multiplied
        by the resolution
 - RAW: Can be stored from 12-14 bits per pixel, range is multiplied
        by the resolution
 - HD HEVC: An HD video is ~20MB per minute compressed. 20 x 15 = 300
 - HD Raw: 1 Frame = 5MB x 30 FPS = 150MB per second. For 15 minutes:
        150 x 60 (seconds in a minute) x 15 (minutes) = 135000
 - 4K HEVC: A 4K video is ~80MB per minute compressed. 84 x 15 = 1260
 - 4K Raw: 4K resolution has 4x as many pixels as an HD video, making
        135000 x 4 = 540000
 - Human Genome:
         - Haploid: 3 Billion base pairs x 2 bits = 750MB
         - Diploid: 750MB x 2 = 1.5GB

### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64GB     |  01  |
| Daily Twitter Tweets (Snappy Compressed)  | 43GB     |  01  |
| Daily Instagram Photos                    | 275.5GB  |  01  |
| Daily YouTube Videos                      | 14.4TB   |  05  |
| Yearly Twitter Tweets (Uncompressed)      | 23.3TB   |  08  |
| Yearly Twitter Tweets (Snappy Compressed) | 15.7TB   |  05  |
| Yearly Instagram Photos                   | 100.6TB  |  31  |
| Yearly YouTube Videos                     | 5256TB   | 1577 |

#### Explanation

- Tweets Uncomporessed: 500,000,000 (tweets) x 128 (characters) x 1 byte
       = 64GB
- Tweets Compressed: According to Github, Snappy has a 1.5x compression
       rate for text. 64/1.5 = ~43GB
- Daily Instagram Photos: 100,000 (photos per day) x 
       2.755MB (avg size of 1024x768 PNG image) = 275.5GB
- Daily Youtube Videos: 20MB per minute x 500 hours per minute = 10000MB
       10000MB (per minute) x 60 (minutes per hr) x 24 (hrs per day) =
       14.4TB
- Yearly Tweets Uncompressed: 64GB (daily) x 365 = 23.3TB
- Yearly Tweets Compressed: 43GB (daily) x 365 = 15.7TB
- Yearly Instagram Photos: 275.5GB (daily) x 365 = 100.6TB
- Yearly Youtube Videos: 14.4TB (daily) x 365 = 5256TB
       

### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | 08   |    0.12    |
| Twitter Tweets (Snappy Compressed) | 05   |    0.08    |
| Instagram Photos                   | 31   |    0.47    |
| YouTube Videos                     | 1577 |    23.7    |

#### Explanation

- Annual Hard Drive Failure Rate: 1.5% x # of Hard Drives

### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 47.6ms               |
| Low Earth Orbit Satellite | 6-12.5ms             |
| Geostationary Satellite   | 182.6ms              |
| Earth to the Moon         | 1929.1ms             |
| Earth to Mars             | 30.2 minutes         | 

#### Explanation

- Latency: Distance (mi) + 100 / 124(m/msec) + 2ms
- LA to Amsterdam: 5551mi + 100 / 124 + 2 = 47.6ms
- Low Orbit Satellite: 400-1200mi + 100 / 124 + 2 = 6ms-12.5ms
- Geostationary Satellite: 22300mi + 100 / 124 + 2 = 182.6ms
- Earth to Moon: 238855mi + 100 / 124 + 2 = 1929.1ms
- Earth to Mars: 225,000,000mi (avg dist.) + 100 / 124 + 2 = 30.2min

### References

https://docs.oracle.com/cd/E19253-01/817-6223/chp-typeopexpr-2/index.html
https://learn.microsoft.com/en-us/windows/win32/gdiplus/-gdiplus-types-of-bitmaps-about
https://en.wikipedia.org/wiki/Raw_image_format
https://www.circlehd.com/blog/how-to-calculate-video-file-size#:~:text=Shutter%20speed%20is%20an%20in,150MB%20storage%20space%20per%20second.
https://en.wikipedia.org/wiki/Human_genome#Information_content
https://www.omnicoreagency.com/instagram-statistics/
https://www.omnicoreagency.com/youtube-statistics/
https://www.backblaze.com/b2/hard-drive-test-data.html
https://en.wikipedia.org/wiki/Low_Earth_orbit
https://www.techtarget.com/searchmobilecomputing/definition/geostationary-satellite#:~:text=A%20geostationary%20satellite%20is%20an,rotates%20(west%20to%20east).
https://www.rmg.co.uk/stories/topics/how-far-away-moon