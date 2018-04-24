# mecab
```
version : mecab-0.996
```
- **install**
  - **mecab**
    ```
    tar -xzvf mecab-0.996.tar.gz
    cd mecab-0.996
    ./configure --with-charset=utf8 --prefix=$HOME/tools/bin
    make
    make install
    ```
  - **dict**
    ```
    tar -xzvf mecab-ipadic-2.7.0-20070801.tar.gz 
    cd mecab-ipadic-2.7.0-20070801
    ./configure --with-charset=utf8 --prefix=$HOME/tools/bin
    make
    make install
    ```
  - **python**
    ```
    pip install mecab-python
    ```
- **test**
  ```
  # -*- coding: utf-8 -*-
  import MeCab
  mecab = MeCab.Tagger('-Ochasen')
  print mecab.parse('祇園精舎の鐘の声諸行無常の響あり')  #utf-8
  ```
  - **output**
    ```
      祇園	ギオン	祇園	名詞-固有名詞-地域-一般		
      精舎	ショウジャ	精舎	名詞-一般		
      の	ノ	の	助詞-連体化		
      鐘	カネ	鐘	名詞-一般		
      の	ノ	の	助詞-連体化		
      声	コエ	声	名詞-一般		
      諸行無常	ショギョウムジョウ	諸行無常	名詞-一般		
      の	ノ	の	助詞-連体化		
      響	ヒビキ	響	名詞-一般		
      あり	アリ	ある	動詞-自立	五段・ラ行	連用形
      EOS
    ```
