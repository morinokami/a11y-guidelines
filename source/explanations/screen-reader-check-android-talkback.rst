.. _exp-screen-reader-check-android-talkback:

##########################################
Android TalkBackを用いたチェックの実施方法
##########################################

Android用スクリーン・リーダーのTalkBackの推奨設定の方法、基本的な使い方と基本的なチェックの実施方法について記します。

なお、本稿の記述は、以下の環境に基づいたものです。
機種、AndroidのバージョンやTalkBackのバージョンによって細部が異なる可能性があります。

端末
   Pixel 6
Androidバージョン
   12
TalkBackバージョン
   12.1

本稿ではごく一部の機能や設定について紹介しています。
より詳しくは、Googleが提供する `Androidのユーザー補助機能に関するヘルプ <https://support.google.com/accessibility/android/>`_ 内、「スクリーン リーダーを使用する」にあるTalkBackに関する情報を参照してください。

**********
起動と終了
**********

TalkBackの起動と終了の方法はいくつかありますが、一時的に有効にしたり、有効/無効を切り替えながら使うような場合は、以下の設定をすると便利です。

1. 「設定」アプリ、 :menuselection:`ユーザー補助 --> TalkBack` の順にタップ
2. :menuselection:`TalkBackショートカット` をオンにする
3. :menuselection:`TalkBackショートカット` が「音量大と音量小の両方のボタンを長押し」になっていない場合は、 :menuselection:`TalkBackショートカット` をタップし、 :menuselection:`音量キーを長押し` をチェック

この設定を行うことで、音量大と音量小のボタンを同時に長押しして、TalkBackの有効/無効を切り替えることができるようになります。

********
推奨設定
********

以下、アクセシビリティー・チェック実施の観点で推奨される設定を記します。

読み上げの詳細設定
==================

オブジェクトの選択時などに読み上げられる情報量を制御する設定です。

設定の場所
   「設定」アプリ、 :menuselection:`ユーザー補助 --> TalkBack --> 設定 --> 読み上げの詳細設定`
推奨設定
   *  「プリセットの選択」で「高」を選択、または
   *  「プリセットの選択」で「カスタム」を選択肢、以下の項目が有効になっていることを確認する

      -  使用に関するヒントの読み上げ
      -  リストやグリッドの情報の読み上げ
      -  画面に表示されるリスト項目の数を読み上げる → 常に読み上げる
      -  要素タイプの読み上げ

読み上げコントロール
====================

後述する読み上げコントロールによって選択できる設定項目を設定します。

設定の場所
   「設定」アプリ、 :menuselection:`ユーザー補助 --> TalkBack --> 設定 --> メニューのカスタマイズ --> 読み上げコントロールをカスタマイズ`
推奨設定
   *  「見出し」を選択
   *  その他、必要に応じてよく使う項目を選択し、使うことがないものの選択を解除

TalkBackの読み上げ内容の表示
============================

TalkBackが読み上げる内容を、画面に表示する設定です。

設定の場所
   「設定」アプリ、 :menuselection:`ユーザー補助 --> TalkBack --> 設定 --> 詳細設定 --> デベロッパー向けの設定`
推奨設定
   「音声出力の表示」をチェック

**************
基本的な使い方
**************

TalkBack有効時に使われることが多い、基本的なゼスチャーを以下に示します。
なお、これらのゼスチャーはデフォルトの設定で有効なもので、ほとんどのゼスチャーは好みに応じて変更することが可能です。

.. _exp-sr-androidtb-one-finger-horizontal-flick:

1本指による右および左方向へのフリック
=====================================

フォーカスを次（右フリック）または前（左フリック）のオブジェクトに移して、そのオブジェクトを読み上げます。

画面の先頭のオブジェクトが選択されているときに左フリック、または画面の末尾のオブジェクトが選択されているときに右フリックすると、「ポン」という効果音が再生されます。
さらに同じ方向にフリックすると、画面末尾で右フリックの場合は画面先頭の、画面先頭で左フリックの場合は画面末尾のオブジェクトが選択され読み上げられます。

この方法で画面の内容を読み上げさせることでチェックを実施する場合、以下が基本的な手順です：

1. 画面の先頭（普通は左上）のオブジェクトにタッチして選択された状態にする
2. 左フリックをしてそれ以上前にオブジェクトが存在しないことを確認（フリック時に「ポン」という効果音が再生される。再度左フリックすると、画面末尾のオブジェクトが選択され読み上げられる。）
3. 左方向にフリックして別の内容が読み上げられる場合は、先頭のオブジェクトに到達するまで左フリック
4. そこから画面の末尾に到達するまで、読み上げられる内容を確認しながら右フリックを繰り返す

1本指によるダブルタップ
=======================

上述の1本指による左右方向へのフリックを行うことで、画面上のオブジェクトのいずれかが選択された状態になります。
また、画面上の任意のオブジェクトを1本指でタップすることでも、そのオブジェクトが選択された状態になります。

画面上のオブジェクトが選択された状態のとき、画面上の任意の場所を1本指で素早く2度タップ（ダブルタップ）すると、そのオブジェクトがアクティベートされます。すなわち、TalkBackが有効になっているときのダブルタップは、TalkBackが無効になっているときのタップ操作に相当します。

.. _exp-sr-androidtb-one-finger-vertical-flick:

1本指による上および下方向へのフリック
=====================================

後述する読み上げコントロールの変更のゼスチャーで選択された内容に基づいて、読み上げ、フォーカスの移動、設定の変更などの操作をすることができます。

例えば、読み上げコントロールで「文字」が選択されているときは、1本指の下方向ーのフリックで次の文字、上方向ーのフリックで前の文字に移動して、その文字を読み上げます。
読み上げコントロールで「単語」や「行」を選択すると、移動の単位がそれぞれ単語や行に変わります。

また、読み上げコントロールの選択が、「見出し」、「コントロール」、「リンク」などの場合は、1本指の下/上方向へのフリックで、次/前の当該オブジェクトに移動して読み上げます。
「読み上げ速度」、「原語」などの場合は、1本指の上下方向へのフリックで、当該の設定値を変更します。

読み上げコントロールの変更（3本指による上および下方向へのフリックなど）
=======================================================================

読み上げコントロールの設定変更には、デフォルトで以下のゼスチャーが割り当てられています。
いずれのゼスチャーも同じ操作に割り当てられていますので、使いやすいものを使用します。

*  3本指による上および下方向へのフリック
*  3本指による左および右方向へのフリック
*  1本指による上方向へのフリックに続けて下方向にフリック、および下方向へのフリックに続けて上方向にフリック

読み上げコントロールの設定に関しては、前述の推奨設定も参照してください。

スクロール
==========

スクロールは、2本指で画面に触れ、ゆっくりと動かすような操作で行います。
同じ距離をフリックよりも時間をかけて移動するようなイメージです。
この動きを、本稿では以下「スライド」と記します。

縦長の画面でのスクロールは2本指による上または下方向へのスライドで縦方向にスクロールすることができます。
また、例えばホーム画面で画面を切り替えるような場合は、2本指による右または左方向へのスライドで実行することができます。

その他の2本指による操作
=======================

TalkBackが有効でない場合に1本指のフリックで行う操作は、TalkBack有効時には2本指によるフリック操作で実行できます。

例えば、画面下端から上方向に1本指でフリックすることでホーム画面に移動する設定がされている場合、TalkBack有効時には画面下端に2本指で触れてそのまま上方向にフリックすることで同様の操作をすることができます。

****************************************
戸惑わないために知っておきたいゼスチャー
****************************************

以下に挙げる操作は、意図せずに実行して戸惑うことが多い操作です。
チェックの際に使うことはあまりありませんが、事前に知っておくことでうっかりこれらの操作を実行してしまっても適切に対応することができるはずです。

音楽の再生
==========

2本指でダブルタップすると、音楽が再生されることがあります。

再度2本指でダブルタップすることで、再生を停止することができます。

**********************************************************
一般的に用いられるコンポーネントの操作方法と期待される挙動
**********************************************************

ここでは、用いられることが多い標準のUIコンポーネントについて、TalkBack使用時の挙動と操作方法を記します。
UIコンポーネントを独自に実装する場合は、これらを参考にしてTalkBack使用時の挙動を定めると良いでしょう。

ボタン
======

UIコンポーネント
   *  button
   *  floating action button
参考
   *  `Buttons - Material Design <https://material.io/components/buttons>`_
   *  `MaterialButton  |  Android Developers <https://developer.android.com/reference/com/google/android/material/button/MaterialButton>`_
   *  `Buttons: floating action button - Material Design <https://material.io/components/buttons-floating-action-button>`_
   *  `FloatingActionButton  |  Android Developers <https://developer.android.com/reference/com/google/android/material/floatingactionbutton/FloatingActionButton>`_

使用されている箇所の例
----------------------

button
   「電話」アプリ、 :menuselection:`キーパッド` の「発信」ボタン
floating action button
   「Gmail」アプリ、右下の :menuselection:`作成` ボタン

TalkBack利用時の挙動
--------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  そのボタンの役割が分かるテキストが読み上げられる
   *  ボタンであることが分かる読み上げがされる
1本指によるダブルタップ
   *  ボタンがアクティベートされる

checkbox
========

UIコンポーネント
   checkbox
参考
   *  `Checkboxes - Material Design <https://material.io/components/checkboxes>`_
   *  `MaterialCheckBox  |  Android Developers <https://developer.android.com/reference/com/google/android/material/checkbox/MaterialCheckBox>`_

使用されている箇所の例
----------------------

「カレンダー」アプリ、左上のボタン（TalkBackでは「カレンダーリストと設定ドロワーを表示する」と読み上げられるボタン）をタップして表示される画面の、カレンダーのリスト

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  なにを変更するためのコントロールかが分かる読み上げがされる
   *  現在の選択状態（オン/オフ）が読み上げられる
1本指によるダブルタップ
   選択状態が切り替わる

switch
======

UIコンポーネント
   switch
参考
   *  `Switches - Material Design <https://material.io/components/switches>`_
   *  `SwitchMaterial  |  Android Developers <https://developer.android.com/reference/com/google/android/material/switchmaterial/SwitchMaterial>`_

使用されている箇所の例
----------------------

「設定」アプリ、 :menuselection:`ネットワークとインターネット` の「機内モード」の切り替え

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  スイッチであることが読み上げられる
   *  なにを変更するためのコントロールかが分かる読み上げがされる
   *  現在の選択状態（オン/オフ）が読み上げられる
1本指によるダブルタップ
   選択状態が切り替わり、変更後の状態が読み上げられる

radio button
============

UIコンポーネント
   radio button
参考
   *  `Radio buttons - Material Design <https://material.io/components/radio-buttons>`_
   *  `MaterialRadioButton  |  Android Developers <https://developer.android.com/reference/com/google/android/material/radiobutton/MaterialRadioButton>`_

使用されている箇所の例
----------------------

「設定」アプリ、 :menuselection:`ネットワークとインターネット --> プライベート DNS` の「OFF】、「自動」、「プライベート DNS プロバイダのホスト名」の選択

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  ラジオボタンであることが分かる読み上げがされる
   *  現在選択されている項目が読み上げられる
   *  現在選択されている項目が、全部でいくつある項目のうちのいくつ目かが分かる読み上げがされる
1本指によるダブルタップ
   *  選択状態が変更され、変更後の状態を読み上げる

スピナー
========

UIコンポーネント
   menu
参考
   *  `Menus - Material Design <https://material.io/components/menus>`_
   *  `AppCompatSpinner  |  Android Developers <https://developer.android.com/reference/androidx/appcompat/widget/AppCompatSpinner>`_

使用されている箇所の例
----------------------

「時計」アプリ、 :menuselection:`その他のオプション --> 設定` のアラームの「週の始まり」の設定

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  変更対象が分かる読み上げがされる
   *  現在選択されている項目が読み上げられる
1本指によるダブルタップ
   選択肢が表示される
選択肢が表示された状態で
   1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
      選択肢が読み上げられる
   1本指によるダブルタップ
      その項目が選択されて元の画面に戻る

time picker
===========

UIコンポーネント
   time picker
参考
   *  `Time pickers - Material Design <https://material.io/components/time-pickers>`_
   *  `MaterialTimePicker  |  Android Developers <https://developer.android.com/reference/com/google/android/material/timepicker/MaterialTimePicker>`_

使用されている箇所の例
----------------------

「時計」アプリ、「アラーム」タブ、 :menuselection:`アラームを追加` で表示される画面

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  フォーカスされている項目が読み上げられる
   *  現在選択されている項目の場合は、そのことが分かる読み上げがされる
1本指によるダブルタップ
   その項目が選択された状態になる

ポップアップ
============

UIコンポーネント
   snackbar
参考
   *  `Snackbars - Material Design <https://material.io/components/snackbars>`_
   *  `Snackbar  |  Android Developers <https://developer.android.com/reference/com/google/android/material/snackbar/Snackbar>`_

使用されている箇所の例
----------------------

「Gmail」アプリ、メール一覧でメールを長押し後、 :menuselection:`既読にする` をタップすると表示される

TalkBack利用時の挙動
---------------------

表示内容が自動的に読み上げられる

dialog
======

UIコンポーネント
   dialog
参考
   *  `Dialogs - Material Design <https://material.io/components/dialogs>`_
   *  `DialogFragment  |  Android Developers <https://developer.android.com/reference/androidx/fragment/app/DialogFragment>`_

使用されている箇所の例
----------------------

「設定」アプリ、 :menuselection:`ネットワークとインターネット --> プライベート DNS` で表示される画面

TalkBack利用時の挙動
---------------------

1本指による右/左方向へのフリック
   *  ダイアログ内の要素間でフォーカスが移動し、選択される
   *  フォーカスされている要素が読み上げられる
1本指で触れる
   *  触れた箇所にある要素がフォーカスされる
   *  フォーカスされている要素が読み上げられる
1本指によるダブルタップ
   フォーカスされている要素がアクティベートされる

ハンバーガー・メニュー
======================

UIコンポーネント
   navigation drawer
参考
   *  `Navigation drawer - Material Design <https://material.io/components/navigation-drawer>`_
   *  `Toolbar  |  Android Developers <https://developer.android.com/reference/androidx/appcompat/widget/Toolbar>`_

使用されている箇所の例
----------------------

「Gmail」アプリ、画面左上に表示されている3本線

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   ナビゲーション・ドロワーであることが分かる読み上げがされる
1本指によるダブルタップ
   メニューが開いて選択肢が表示される
メニューが開いている状態で
   1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
      選択肢が読み上げられる
   1本指によるダブルタップ
      その項目が選択されて当該画面に遷移する

画面右上のメニュー
==================

UIコンポーネント
   toolbar
参考
   `Toolbar  |  Android Developers <https://developer.android.com/reference/androidx/appcompat/widget/Toolbar>`_

使用されている箇所の例
----------------------

「Chrome」アプリ、右上に表示されているメニュー

TalkBack利用時の挙動
---------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   タップできることが分かる読み上げがされる
1本指によるダブルタップ
   メニューが開いて選択肢が表示される
メニューが開いている状態で
   1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
      選択肢が読み上げられる
   1本指によるダブルタップ
      その項目が選択されて当該画面に遷移する

tab
===

UIコンポーネント
   tab
参考
   *  `Tabs - Material Design <https://material.io/components/tabs>`_
   *  `TabLayout.TabView  |  Android Developers <https://developer.android.com/reference/com/google/android/material/tabs/TabLayout.TabView>`_

使用されている箇所の例
----------------------

「Play ストア」アプリ、「おすすめ」、「ランキング」、「子供」などのタブ

TalkBack利用時の挙動
--------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  タブの名称（タイトル）が読み上げられる
   *  現在選択、表示されているタブの場合は、選択されていることが分かる読み上げがされる
1本指によるダブルタップ
   そのタブが選択状態になり、選択されたことが分かる読み上げがされる

縦スクロール
============

UIコンポーネント
   LinearLayoutManager
参考
   *  `LinearLayoutManager  |  Android Developers <https://developer.android.com/reference/androidx/recyclerview/widget/LinearLayoutManager>`_

使用されている箇所の例
----------------------

「Play ストア」アプリ、コンテンツの一覧

TalkBack利用時の挙動
--------------------

2本指を上/下方向へスライド
   *  効果音が再生され、表示がスクロールする
   *  指を離すと、全何項目中の何項目目から何項目目までが表示されているかが分かる読み上げがされる

text field
==========

UIコンポーネント
   text field
参考
   *  `Text fields - Material Design <https://material.io/components/text-fields>`_
   *  `TextInputEditText  |  Android Developers <https://developer.android.com/reference/com/google/android/material/textfield/TextInputEditText>`_

使用されている箇所の例
----------------------

「Gmail」アプリ、 :menuselection:`作成` の、件名や本文を入力するフィールド

TalkBack利用時の挙動
--------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   *  なにを変更するためのコントロールかが分かる読み上げがされる
   *  text fieldであることが分かる読み上げがされる
   *  現在入力されている値、またはプレイスホルダーとして表示されている値が読み上げられる
1本指によるダブルタップ
   *  編集可能な状態に切り替わる
   *  画面上に表示されたキーボードから入力ができる
   *  外付けのキーボードが接続されている場合は、そのキーボードからも入力ができる
編集可能な状態での1本指による上または下方向へのフリック
   *  読み上げコントロールの設定※に応じてカーソルが移動し、移動した範囲の入力内容が読み上げられる

※読み上げコントロールの設定が、「文字」の場合は1文字ずつ、「単語」の場合は1単語ずつ、「行」の場合は1行ずつ移動します。

検索ボックス
============

UIコンポーネント
   SearchView
参考
   *  `SearchView  |  Android Developers <https://developer.android.com/reference/androidx/appcompat/widget/SearchView>`_

使用されている箇所の例
----------------------

「設定」アプリ画面内の「設定を検索」

TalkBack利用時の挙動
--------------------

1本指で触れる、または1本指による右/左方向へのフリックでフォーカス
   検索ボックスであることが分かる読み上げがされる
1本指によるダブルタップ
   *  編集可能な状態に切り替わる
   *  画面上に表示されたキーボードから入力ができる
   *  外付けのキーボードが接続されている場合は、そのキーボードからも入力ができる
編集可能な状態での1本指による上または下方向へのフリック
   *  読み上げコントロールの設定※に応じてカーソルが移動し、移動した範囲の入力内容が読み上げられる
検索語入力ご
   *  1本指による右/左方向へのフリックで検索候補間を移動
   *  検索候補を1本指でダブルタップすると検索を実行など

※読み上げコントロールの設定が、「文字」の場合は1文字ずつ、「単語」の場合は1単語ずつ、「行」の場合は1行ずつ移動します。
