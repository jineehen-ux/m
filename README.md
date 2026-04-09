minii-netflix-app/
├── src/
│   ├── app/
│   │   ├── layout.tsx                    ← Root layout
│   │   ├── globals.css
│   │   ├── (auth)/
│   │   │   ├── login/page.tsx            ← Нэвтрэх хуудас
│   │   │   └── register/page.tsx         ← Бүртгүүлэх хуудас
│   │   ├── (main)/
│   │   │   ├── layout.tsx                ← Navbar + Footer
│   │   │   ├── browse/page.tsx           ← 🏠 Нүүр хуудас
│   │   │   └── movie/[id]/page.tsx       ← 🎬 Киноны дэлгэрэнгүй
│   │   └── watch/[id]/page.tsx           ← ▶️ Видео тоглуулах
│   ├── components/
│   │   ├── layout/
│   │   │   ├── navbar.tsx
│   │   │   └── footer.tsx
│   │   └── ui/
│   │       ├── button.tsx
│   │       ├── input.tsx
│   │       ├── dialog.tsx
│   │       └── skeleton.tsx
│   ├── features/
│   │   ├── movies/
│   │   │   ├── api/get-movies.ts         ← Mock өгөгдөл (12 кино)
│   │   │   └── components/
│   │   │       ├── hero-banner.tsx
│   │   │       ├── movie-card.tsx
│   │   │       └── movie-row.tsx
│   │   └── player/
│   │       ├── components/
│   │       │   ├── video-player.tsx
│   │       │   └── controls.tsx
│   │       └── hooks/use-progress.ts
│   ├── lib/utils.ts
│   └── types/index.ts
├── package.json
├── tailwind.config.ts
└── next.config.ts
