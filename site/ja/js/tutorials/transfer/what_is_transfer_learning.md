# 転移学習とは？

Note: これらのドキュメントは私たちTensorFlowコミュニティが翻訳したものです。コミュニティによる
翻訳は**ベストエフォート**であるため、この翻訳が正確であることや[英語の公式ドキュメント](https://www.tensorflow.org/?hl=en)の
最新の状態を反映したものであることを保証することはできません。
この翻訳の品質を向上させるためのご意見をお持ちの方は、GitHubリポジトリ[tensorflow/docs](https://github.com/tensorflow/docs)にプルリクエストをお送りください。
\
コミュニティによる翻訳やレビューに参加していただける方は、
[docs-ja@tensorflow.org メーリングリスト](https://groups.google.com/a/tensorflow.org/forum/#!forum/docs-ja)にご連絡ください。

高度な深層学習モデルには大量のパラメータ（重み）があり、それらをなにもないところから訓練するには大量の計算資源のデータが必要です。転移学習は関連するタスクについてすでに学習済みのモデルの一部を取り出して、新しいモデルの中で再利用することでそのような資源の大部分を省略するテクニックです。

例えば、このセクションの次のチュートリアルではすでに画像の中の数千種類の物体を認識できるように訓練されたモデルを利用して、独自の画像認識器を構築する方法を紹介します。学習済みモデルの既存の知識を適用すると、元のモデルで必要としたものよりもずっと少ない訓練データで独自の画像クラスを検出できます。

この手法はブラウザやモバイルデバイスのような資源が限られた環境でモデルをカスタマイズする際だけでなく、新しいモデルを高速に開発する際にも有効です。

転移学習を行う際、元のモデルの重みを調節しないこともよくあります。そのかわりに最終レイヤを取り除き、切り詰められたモデルの出力で新しい（通常は非常に浅い）モデルを訓練します。このセクションのチュートリアルで、このテクニックを紹介します。

- [画像分類器を元にした転移学習](image_classification)
- [音声認識を元にした転移学習](audio_recognizer)
