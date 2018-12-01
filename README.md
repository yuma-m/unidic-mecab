# mecab-unidic

Docker container with mecab, unidic-mecab, python-mecab.

```bash
$ docker run -it yumam/unidic-mecab:latest
root@2a20c9080f43:/# mecab
あいうえお
あ	ア	アー	あー	感動詞-フィラー		
いう	ユー	イウ	言う	動詞-一般	五段-ワア行	連体形-一般
え	エ	エー	えー	感動詞-フィラー		
お	オ	オー	おー	感動詞-フィラー		
EOS
すもももももももものうち
すもも	スモモ	スモモ	李	名詞-普通名詞-一般		
も	モ	モ	も	助詞-係助詞		
もも	モモ	モモ	桃	名詞-普通名詞-一般		
も	モ	モ	も	助詞-係助詞		
もも	モモ	モモ	桃	名詞-普通名詞-一般		
の	ノ	ノ	の	助詞-格助詞		
うち	ウチ	ウチ	内	名詞-普通名詞-副詞可能		
EOS

root@287d3d27ab94:/# python
Python 2.7.13 (default, Sep 26 2018, 18:42:22) 
[GCC 6.3.0 20170516] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import MeCab
>>> mecab = MeCab.Tagger("-Ounidic")
>>> print(mecab.parse("Hello World"))
Hello	Hello	Hello	Hello	名詞-普通名詞-一般		
World	World	World	World	名詞-普通名詞-一般		
EOS
```

## Tags

- `stretch` (`latest`): Debian Stretch based container
- `buster`: Debian Buster based container
