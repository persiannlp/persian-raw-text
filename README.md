# Persian Raw Text - متن خام فارسی

The package contains more than 100GBs of free
The texts are collected from the following sources: 

 - [Common Crawl](https://commoncrawl.org/): 65GB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/commoncrawl_fa_merged.txt))
 - [MirasText](https://github.com/miras-tech/MirasText): 12G 
 - [W2C – Web to Corpus](https://lindat.mff.cuni.cz/repository/xmlui/handle/11858/00-097C-0000-0022-6133-9): 1GB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/w2c_merged.txt))
 - Persian Wikipedia (March 2020 dump): 787MB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/fawiki_merged.txt))
 - [Leipzig Corpora](https://corpora.uni-leipzig.de/): 424M ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/LeipzigCorpus.txt))
 - [VOA corpus](https://jon.dehdari.org/corpora/): 66MB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/voa_persian_2003_2008_cleaned.txt))
 - [Persian poems corpus](https://github.com/amnghd/Persian_poems_corpus): 61MB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/poems_merged.txt))
 - [TEP: Tehran English-Persian parallel corpus](http://opus.nlpl.eu/TEP.php): 33MB ([link](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/TEP_fa.txt))

Each resource is modified to exclude non-text content (urls, html, non-utf-8 content, etc). 
I have also dropped the lines that do **not** contain any Persian text. 
I have **not** done any deduplication; so there might be repeated content. 

**The overall data is [here](https://storage.googleapis.com/danielk-files/farsi-text/merged_files/all_text_merged_cleaned.txt) (~70GB, ~13.5million paragraphs).**  


**Note:** since the files are relatively large, you probably shouldn't download in your browser. 
A good way to download the files is to use `gsutil` (see the [here](https://cloud.google.com/storage/docs/gsutil_install) for more). This would give details on the total download size, download progress, etc: 

```bash 
gsutil -m cp -R gs://danielk-files/farsi-text/merged_files/all_text_merged_cleaned.txt  .
Copying gs://danielk-files/farsi-text/merged_files/all_text_merged_cleaned.txt...
/ [0/1 files][600.2 MiB/ 69.8 GiB]   0% Done 
```
You can also use tools like `wget`: 
```bash 
$ wget https://storage.googleapis.com/danielk-files/farsi-text/merged_files/commoncrawl_fa_merged.txt 
--2020-05-17 14:53:08--  https://storage.googleapis.com/danielk-files/farsi-text/merged_files/commoncrawl_fa_merged.txt
Resolving storage.googleapis.com (storage.googleapis.com)... 74.125.195.128
Connecting to storage.googleapis.com (storage.googleapis.com)|74.125.195.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 68720495550 (64G) [text/plain]
Saving to: ‘commoncrawl_fa_merged.txt.1’

commoncrawl_fa_merged.txt.1                    0%[                                                                                              ] 542.30M  55.9MB/s    eta 17m 44s
```


## Credits  
If you find this repo useful, please include a reference to this repository. 
