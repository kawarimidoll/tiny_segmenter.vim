# tiny_segmenter.vim

`tiny_segmenter.vim` は、日本語分かち書きソフトウェア TinySegmenter の Vim script 版です。

オリジナル版ではシングルファイルにモデルを同梱していますが、本スクリプトではJSONに分割しているため、異なるモデルに基づいて分かち書きを行うことも可能です。

## Getting Started

```vim
" オリジナル版のモデルを使う場合
let m = tiny_segmenter#load_model("ORIGINAL")

" ローカルのモデルを使用することも可能
" let m = tiny_segmenter#load_model('/path/to/model.json')

echo m.parse('Vim はオープンソースであり自由に配布可能です')
" => ['Vim', ' ', 'は', 'オープンソース', 'で', 'あり', '自由', 'に', '配布', '可能', 'です']
```

## Original

[TinySegmenter: Javascriptだけで実装されたコンパクトな分かち書きソフトウェア](http://chasen.org/~taku/software/TinySegmenter/)

## Prior art

https://github.com/shogo82148/TinySegmenterMaker
