<script src="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/list.js/2.3.1/list.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tify@0.27.0/dist/tify.css">

# waterperiodの図書館
こんにちは。
こちらはCode4Lib JAPAN カンファレンス 2022のチュートリアル「GitHub Pagesで作るWebサイト」で作成したページです。

## お知らせ
- 新着図書を追加しました。(2022年9月3日)
- [ブクログのページ](https://waterperiod.github.io/booklog.html)を追加しました。(2022年9月3日)
- [イベントのページ](https://waterperiod.github.io/event.html)を追加しました。(2022年9月3日)
- 「waterperiodの図書館」のページを開設しました。(2022年9月3日)

## 新着図書
<div id="books">
  <input class="search" placeholder="検索" />
  <button class="sort" data-sort="title">
    タイトルで並べ替え
  </button>
  <ul class="list">
    <!-- _data フォルダの books.csv からデータを取り出す -->
    {% for book in site.data.books %}
      <li>
        <!-- books.csv の title 列、 url 列をリンク先に設定 -->
        <p class="title"><a href="{{ book.url }}">{{ book.title }}</a> <i>{{ book.author }}</i></p>
      </li>
    {% endfor %}
  </ul>
</div>

<script>
var options = {
    valueNames: [ 'title' ]
};

var userList = new List('books', options);
</script>
