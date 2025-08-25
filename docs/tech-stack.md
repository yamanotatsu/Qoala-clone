# 🚀 技術スタック詳細仕様書

## 概要
SESマッチングプラットフォーム「Qoala Clone」の技術スタック構成。Next.js + TypeScriptをコアとしたフルスタック構成。

---

## 📋 技術スタック一覧

### **コアフレームワーク**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| Next.js | 14.x | フルスタックフレームワーク | App Router、API Routes、SSR/SSG、TypeScript完全対応 |
| React | 18.x | フロントエンドライブラリ | 豊富なエコシステム、コンポーネント指向 |
| TypeScript | 5.x | 型安全な開発 | バグ減少、開発効率向上、IDE支援 |
| Node.js | 18.x+ | サーバーサイドランタイム | Next.jsの実行環境 |

### **フロントエンド技術**

#### **UI・スタイリング**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| Tailwind CSS | 3.x | CSSフレームワーク | ユーティリティファースト、高いカスタマイズ性 |
| shadcn/ui | latest | Reactコンポーネントライブラリ | 高品質、アクセシビリティ対応、Tailwind統合 |
| Lucide React | latest | アイコンライブラリ | 軽量、豊富なアイコン、React対応 |
| Framer Motion | 11.x | アニメーションライブラリ | 宣言的アニメーション、パフォーマンス最適化 |

#### **状態管理・フォーム**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| Zustand | 4.x | グローバル状態管理 | 軽量、TypeScript対応、学習コスト低 |
| React Hook Form | 7.x | フォーム管理 | 高パフォーマンス、バリデーション統合 |
| Zod | 3.x | スキーマバリデーション | TypeScript統合、ランタイム型チェック |

#### **データフェッチング**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| TanStack Query | 5.x | サーバー状態管理 | キャッシュ、リアルタイム同期、エラーハンドリング |
| Axios | 1.x | HTTPクライアント | インターセプター、レスポンス変換 |

### **バックエンド技術**

#### **API・サーバーサイド**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| Next.js API Routes | 14.x | RESTful API | フロントエンドとの統合、型安全性 |
| tRPC | 10.x | 型安全なAPI通信 | エンドツーエンドの型安全性 |
| NextAuth.js | 4.x | 認証システム | OAuth対応、セッション管理、セキュリティ |

#### **データベース・ORM**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| **Supabase** | latest | **メインデータベース** | PostgreSQL + リアルタイム + 認証統合 + 管理画面 |
| Prisma | 5.x | ORM | TypeScript統合、マイグレーション、型安全 |
| **Vercel KV** | latest | **Redis互換キャッシュ** | Vercel統合、セッション管理、高速アクセス |

#### **外部API連携・AI**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| **@google/generative-ai** | latest | **AI解析エンジン** | Gemini API、高精度、日本語対応、コスト効率 |
| googleapis | latest | Gmail API連携 | 公式SDK、OAuth対応、メール取得・転送 |
| **Vercel Blob** | latest | **ファイルストレージ** | Vercel統合、簡単設定、自動スケール |

### **開発・品質管理**

#### **開発ツール**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| ESLint | 8.x | 静的解析 | コード品質向上、バグ検出 |
| Prettier | 3.x | コードフォーマット | 一貫したコードスタイル |
| Husky | 8.x | Git hooks | コミット前チェック |
| lint-staged | 13.x | ステージングファイル処理 | 効率的なlint実行 |

#### **テスト**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| Jest | 29.x | 単体テスト | 豊富な機能、Next.js対応 |
| React Testing Library | 14.x | Reactコンポーネントテスト | ユーザー視点のテスト |
| Playwright | 1.x | E2Eテスト | 高速、信頼性、クロスブラウザ |
| MSW | 2.x | APIモック | リアルなAPI環境模擬 |

### **デプロイ・インフラ**

#### **ホスティング・CI/CD・バッチ処理**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| **Vercel** | latest | **ホスティングプラットフォーム** | Next.js最適化、自動デプロイ、CDN |
| **Vercel Cron Jobs** | latest | **バッチ処理・定期実行** | サーバーレス、簡単設定、コスト効率 |
| GitHub Actions | latest | CI/CDパイプライン | GitHub統合、豊富なアクション |
| Docker | 24.x | コンテナ化（オプション） | 環境統一、デプロイメント |

#### **データベース・ストレージ**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| **Supabase** | latest | **本番・開発データベース** | PostgreSQL、リアルタイム、認証統合、管理画面 |
| **Vercel KV** | latest | **Redis互換キャッシュ** | Vercel統合、セッション管理、高速アクセス |
| Vercel Edge Config | latest | 設定データ（オプション） | 高速設定配信 |

### **特定機能向けライブラリ**

#### **メール・テキスト処理**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| node-html-parser | 6.x | HTMLメール解析 | 軽量、高速パース |
| compromise | 14.x | 自然言語処理 | 日本語対応、軽量NLP |
| string-similarity | 4.x | 文字列マッチング | 類似度計算、マッチング精度向上 |

#### **ユーティリティ**
| 技術 | バージョン | 用途 | 選定理由 |
|------|-----------|------|----------|
| date-fns | 2.x | 日付操作 | 軽量、関数型、国際化対応 |
| lodash | 4.x | ユーティリティ関数 | 豊富な関数、パフォーマンス |
| uuid | 9.x | ユニークID生成 | 標準的、衝突確率低 |
| bcryptjs | 2.x | パスワードハッシュ化 | セキュア、Node.js対応 |

---

## 📦 パッケージ管理

### **パッケージマネージャー**
- **npm** または **pnpm** (推奨: pnpm - 高速、ディスク効率)

### **Node.js バージョン管理**
- **nvm** (Node Version Manager)
- 推奨バージョン: Node.js 18.x LTS

---

## 🏗️ アーキテクチャ構成

### **アプリケーション構成**
```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   Database      │
│   (React)       │◄──►│   (API Routes)  │◄──►│   (Supabase)    │
│   Next.js       │    │   Next.js       │    │   PostgreSQL    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Vercel        │    │   Gmail API     │    │   Vercel KV     │
│   (Hosting)     │    │   Gemini AI     │    │   (Cache)       │
│   Cron Jobs     │    │   (External)    │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### **データフロー**
1. **認証**: NextAuth.js → Google OAuth → Vercel KV セッション管理
2. **メール取得**: Vercel Cron → Gmail API → Gemini AI解析 → Supabase保存
3. **データ解析**: Gemini API → 構造化JSON → データ検証・保存
4. **マッチング**: ルールエンジン → スコア計算 → 結果表示

---

## 🔧 開発環境要件

### **必要なソフトウェア**
- Node.js 18.x LTS以上
- npm 9.x以上 または pnpm 8.x以上
- Git 2.x以上
- VSCode (推奨エディタ)

### **推奨VSCode拡張機能**
- ES7+ React/Redux/React-Native snippets
- Tailwind CSS IntelliSense
- Prisma
- TypeScript Importer
- ESLint
- Prettier

### **環境変数**
```bash
# 認証
NEXTAUTH_SECRET=
NEXTAUTH_URL=
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=

# データベース
DATABASE_URL=
SUPABASE_URL=
SUPABASE_ANON_KEY=
KV_REST_API_URL=
KV_REST_API_TOKEN=

# Gmail API
GMAIL_CLIENT_ID=
GMAIL_CLIENT_SECRET=
GMAIL_REFRESH_TOKEN=

# AI
GEMINI_API_KEY=

# その他
NODE_ENV=development
```

---

## 📈 スケーラビリティ考慮

### **パフォーマンス最適化**
- Next.js ISR (Incremental Static Regeneration)
- React Server Components
- 画像最適化 (next/image)
- バンドル最適化

### **将来的な拡張性**
- マイクロサービス化対応
- GraphQL導入検討
- AI/ML機能統合準備
- モバイルアプリ対応 (React Native)

---

## 🛡️ セキュリティ対策

### **実装予定のセキュリティ機能**
- CSRF保護
- XSS対策
- SQL injection対策 (Prisma ORM)
- レート制限
- セキュアヘッダー設定
- OAuth 2.0認証
- データ暗号化

---

## 🚀 Vercel統合環境の特徴

### **Vercelエコシステムの活用**
- **Vercel Cron Jobs**: サーバーレスでのバッチ処理
- **Vercel KV**: Redis互換の高速キャッシュ
- **Vercel Blob**: ファイルストレージ
- **Vercel Analytics**: リアルタイムアクセス解析
- **Edge Functions**: 高速なエッジ処理

### **開発・デプロイの効率化**
- **ゼロ設定デプロイ**: GitHubプッシュで自動デプロイ
- **プレビューデプロイ**: PR毎の自動プレビュー環境
- **環境変数管理**: Vercelダッシュボードでの一元管理
- **ログ・監視**: 統合されたログ・メトリクス

### **コスト効率**
- **サーバーレス課金**: 使用量ベースの効率的なコスト
- **自動スケール**: トラフィックに応じた自動調整
- **CDN統合**: 全世界での高速配信

---

*最終更新: 2024年12月*