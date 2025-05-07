# 名前: 木村 浩一(きむら こういち)

- [GitHub](https://github.com/kupuma-ru21)
- [Portfolio](https://kupuma-ru21.com/)
  - [Repository](https://github.com/kupuma-ru21/portfolio)

## 職務経歴

### フルスタックエンジニア

#### 株式会社Sorajima | 2024 年 5 月 - 現在 | 東京, 日本 (リモート)
##### [ソラジマTOON](https://sorajimatoon.com/) / ソラジマTOONの管理画面のフロント・バックエンド開発 / 作家さんと編集者の方が連絡を取るためのwebアプリのフロント開発

- パフォーマンス改善
  - Lighthouseによるパフォーマンススコアを35% → 75%に改善
    - Network request数を削減

    - 画像読み込みの最適化(`<img>`の`fetchPriority`,`loading`属性を活用)

    - Promise.allを使った非同期処理の並列化

    - レイアウトシフトの解消

    - 不要なレンダリングの削減(controlled componentをuncontrolled componentに置き換え)

  - 楽観的UIを使用しUXの改善

- DX改善
  - 共通コンポーネントを [CompoundComponentパターン](https://kentcdodds.com/blog/compound-components-with-react-hooks) で再設計し、柔軟かつ拡張しやすいUI構成に改善。
従来のprops制御による複雑化を解消し、責務を分離することで保守性と拡張性を向上。


  - Eslintのルール追加<br />
    RemixからLink(画面遷移時に使用される)コンポーネントが提供されてる。
    該当のコンポーネント拡張したコンポーネントをプロジェクト全体で使用することを想定。
    Remixから提供されてるLinkでなく、拡張したコンポーネントが必ず使われるようEslintに"no-restricted-imports"のルールを追加。
    ルールの追加により、全ての画面遷移の挙動が必ず一致するよう担保。

  - [不要なuseEffect](https://react.dev/learn/you-might-not-need-an-effect#resetting-all-state-when-a-prop-changes)の削除

- APIの新規追加、改修、バグ修正(バックエンドエンドエンジニアとのコミニュケーションコスト削減に貢献)

- プロジェクトの新規立ち上げ対応<br />
  立ち上げの経験はなかったが、もともと興味があった分野だったため、機会を活かして自らフロントエンドの立ち上げを担当。
  当初はインフラ周りの知識が浅く不明点も多かったが、GCPのドキュメントを参考に、実際に業務で使用している技術（React, Go, GCP）で[Webアプリ](https://github.com/kupuma-ru21/portfolio)を個人開発。
  事前に構成や技術的な理解を深めたことで、実プロジェクトの立ち上げをスムーズに進行することができた。

- クリティカルなバグの原因調査、解消
  ログインができなくなるという、クリティカルなバグが発生
  他のdeveloperが原因調査をしてたが、調査に時間がかかってた
  原因調査の依頼が自分に来てたわけでは無いが、自分の方でも調査をし、修正(https://github.com/chakra-ui/chakra-ui/issues/7449#issuecomment-1474890718)


##### 使用技術

React.js, Next.js, Remix, Chakra-UI, Storybook, GraphQL-Codegen, Apollo Client, URQL, React-Hook-Form, Zod, ESLint, Prettier, PNPM, Git, Slack, Figma, Go, Ent, Gqlgen

---

### フルスタックエンジニア

#### Buysell Technologies | 2023 年 2 月 - 2023 年 12 月 | 東京, 日本 (リモート)

##### 買取店舗で使用する業務システムのフロント・バックエンド開発

- 日付ライブラリの再選定とリプレイス<br />
  既存プロジェクトではday.jsが使用されていたが、[day.js に起因するパフォーマンス問題](https://github.com/iamkun/dayjs/issues/1236)が発生。<br />
  根本的な解決の見込みがなかったため、day.js から date-fns へリプレイス。<br />
  date-fnsを選定した理由は以下
  - 日付ライブラリの中で[install数が多い](https://npmtrends.com/date-fns-vs-dayjs-vs-luxon)
    - date-fnsに関連する情報が豊富であるため、date-fns起因の問題に直面した場合、問題解決しやすいと判断

    - TypeScript製であり、型安全に扱える

    - 他のライブラリと比較してメンテナンスが活発

- DX・設計改善<br />
  複数の異なる責務を持つ処理が一つのコンポーネントに集約されている「[論理的凝集](https://speakerdeck.com/sonatard/coheision-coupling?slide=29)」の状態だったため、責務ごとにコンポーネントを分離。
  凝集度を適切に保つことで、可読性・メンテナンス性が向上し、機能追加や修正の影響範囲を限定できるようになった。

- APIの新規追加・ER図の更新<br />
  バックエンドの経験はなかったが、もともと興味があった分野だったため、機会を活かして API の新規追加を担当。<br />
  バックエンドのテックリードの方にアドバイスを求めたところ、SQLBoiler を重点的に学ぶことを勧められ、6:2:2 の比率（SQLBoiler : Go : SQL）で学習を実施。
  その結果、API の新規追加およびテストの作成を期日内に完了することができた。
  また、APIの実装に伴い既存テーブルへのカラム追加が必要となり、ER図の更新も併せて実施した。

- Frontend developer全員のPRレビュー
  - バグ検知によって、品質低下を防止
  - よりsimpleなcodeを提案し、DX改善
  - コードの複雑性軽減

- Sentryで検知されたerrorの修正、修正が難しい場合はチーム巻き込んで相談

- Junior developerをサポート


##### 使用技術

React.js, Next.js, Storybook, GraphQL-Codegen, Apollo Client, Material-UI, React-Hook-Form, Zod, Vitest, ESLint, Prettier, PNPM, Git, Slack, Jira, Figma, Go, SQLBoiler, Gqlgen

---

### フロントエンド エンジニア

#### Visits Technologies | 2021 年 5 月 - 2023 年 2 月 | 東京, 日本 (リモート)

##### [Visits Forms](https://visitsforms.com/)のフロントエンド開発

- DX改善
  - コードフォーマットを手動で整える必要があり、非効率だと感じたためPrettierを導入。<br />
    チーム全体で統一されたフォーマットが維持されるようになり、レビュー負荷の軽減や生産性向上に貢献。<br />
    導入後、テックリードの方から「非常に開発しやすくなった」とのフィードバックをいただいた。

  - コーディング規約の策定と ESLint設定の整備<br />
    コードスタイルの揺らぎを防ぐためにコーディング規約を作成し、ESLint によりルールが自動的に適用されるよう設定を構築。<br />
    書き方の統一により、エンジニアがコーディング時に迷う時間を削減し、開発効率の向上に貢献。

  - UIコンポーネントの責務分離による設計改善
    共通UIコンポーネントが親コンポーネントのドメイン知識に依存しないよう設計を見直し、疎結合な構造を実現。<br />
    再利用性・保守性の向上に加え、ドメイン変更時の影響範囲を最小限に抑えることに貢献。

- パフォーマンス改善<br />
  アルゴリズムの見直しにより、特定の処理の計算量を O(2n) から O(n) に削減。<br />

- Jest・React Testing Library を用いたテストコードの作成<br />
  単体テストおよびコンポーネントテストを実装し、品質向上と不具合の早期発見に貢献。<br />
  Sentryを導入していたが、テスト導入後の実運用では月に1件あるかないか程度のエラー通知に抑えられており、テストによる品質の担保が実現できた。
  また、通知されたエラーについては都度テストコードを追加し、再発防止の体制を整えた。

- アジャイル開発における自身の課題発見と改善<br />
  プロジェクト初期、自身の生産性の低さを感じていたが、原因が明確でなかったため、フロントエンド・バックエンドのメンバーにフィードバックを依頼。<br />
  その結果、コミュニケーション不足が要因ではないかと指摘を受け、ウォーターフォール型の開発に慣れていた影響で、PM やデザイナーとの認識合わせを行わずに実装を進めていたことに気づいた。<br />
  不明点が出てから都度質問し、回答待ちの状態で開発が停滞するケースが多発していたため、改善策として、実装前に仕様・デザインに関する不明点を洗い出し、PM・デザイナーと事前に確認する習慣を意識。<br />
  以降は開発をスムーズに進行できるようになり、生産性向上つながった。



##### 使用技術

React.js, React-Router, React-Datepicker, React-DND, React-i18next, React-Hook-Form, React-Testing-Library, Yup, GraphQL-Codegen, Apollo Client, Styled-Components, Jest, ECharts, ESLint, Prettier, Yarn, Git, Slack, Jira, Figma

---

### フロントエンド エンジニア

#### Gizmo inc. | 2019 年 9 月 - 2021 年 5 月 | 東京, 日本

##### インターネットバンキングのフロントエンド開発

- React.js・TypeScript を用いた UI / ビジネスロジックの実装<br />
  当初はReactの経験がなかったため、業務外の時間を活用して学習を実施。<br />
  学習開始から約1カ月で基本的な記述スタイルや設計思想に慣れ、業務内でも滞りなくReactを活用できるようになった。

- Hooksを用いたロジックの共通化とリファクタリング<br />
  複数のコンポーネントに分散していたReactに依存する同様の処理をカスタムフックに抽出。<br />
  処理の共通化により、メンテナンス性・再利用性を向上させ、ロジックの重複や変更漏れのリスクを低減した。


##### 使用技術

React.js, Redux, React-Redux, MUI, Next.js, Formik, Yup, Axios, Jest, ESLint, Yarn, Git, GitLab, Slack, Adobe XD, GitHub

##### 倉庫管理システムのフロントエンド開発

- Gitの学習<br />
  当初はGitの習熟度が低く、生産性に課題を感じていたため、業務外の時間を活用してGitの学習を実施。<br />
  `rebase`や`cherry-pick`などのコマンドを学習し、実務での活用に対応。<br />
  また、デフォルトブランチでないブランチや、最新になってないデフォルトブランチから作業ブランチを切ってしまうことでコンフリクトを起こすことがあったため、<br />
  `checkout デフォルトブランチ` → `pull` → `branch切り出し`をまとめて行うGit aliasを作成し、同様のミスを再発しないよう改善した。

- Vue.js・TypeScriptを用いたUI / ビジネスロジックの実装<br />
  当初はJavaScriptの経験しかなかったため、業務外の時間を活用してTypeScriptの学習を実施。<br />
  学習開始から約2週間で型の使い方や記述スタイルに慣れ、業務内でも滞りなくTypeScriptを活用できるようになった。


##### 使用技術
Vue.js, Vue-Router, Vuex, Vuetify, Axios, Joi, Lodash, VeeValidate, Backlog, GitHub, Slack

## 学歴

- 学士
  - 拓殖大学, 東京, 日本 (2015年 4月 - 2019年 3月)

- Diploma
  - Cornerstone International Community College of Canada, バンクーバー, カナダ(2024年 5月 - 2026年 5月)

## 言語

- 日本語 - ネイティブ
- 英語 - 日常会話レベル
