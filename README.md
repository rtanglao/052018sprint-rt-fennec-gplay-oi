# 052018sprint-rt-fennec-gplay-oi
* Post End of May 2018 Firefox for Android aka Fennec Google Play Store Review Replying Sprint
* a clone of https://github.com/rtanglao/rt-open-innovation-fennec-gplay

## 30June2018

### 30June2018-3 Add november 2017 - april 2018 reviews
* november2017 to april2018 reviews are here: november2017-april-2018-fennec-gplay-reviews.zip

### 30June2018-2 find the reviews replied during experiment 2 which was roughly May 26 - June 16, 2018

* generate a CSV file using a mongodb query using NoSQL Manager for MongoDB Professional 30 day free trial (or any other tool free or otherwise that will generate CSV files; you can also write code in ruby other languages to do this which i've done in the past but i'm lazy so I'm using NoSQL Manager :-) 

```js
// The following query shows all reviews that have non NULL reply text! 
// This only shows 322, bug in my program or all reviews not uploaded? We know over 2000 reviews were updated.
{"Developer Reply Text": {$ne: null} }
```

### 30June2018-1 read the CSVs from google play into the database

```bash
 . setupDatabase
 ./read-reviews-replies.rb utf8-downloaded-29june2018-may2018-fennec-gplay-reviews.csv 2>30june2018-may2018-stderr.txt
 ./read-reviews-replies.rb utf8-downloaded-29june2018-june2018-fennec-gplay-reviews.csv 2>30june2018-june2018-stderr.txt
 ```

## 28June2018

```bash
zip -e downloaded-29june2018-may-2018-reviews.zip utf8-downloaded-29june2018-may2018-fennec-gplay-reviews.csv
zip -e downloaded-29june2018-june-2018-reviews.zip utf8-downloaded-29june2018-june2018-fennec-gplay-reviews.csv
```
