📦 minii-netflix-app
 ┣ 📂 public                  <-- 🌐 (Нийтэд нээлттэй файлууд. Жнь: logo.png, favicon.ico)
 ┃
 ┣ 📂 src                     <-- 💻 (ТАНЫ БИЧИХ БҮХ КОД ЭНД БАЙНА)
 ┃ ┃
 ┃ ┣ 📂 app                   <-- 🛣️ 1. ROUTING (Хуудсууд болон Замууд)
 ┃ ┃ ┣ 📂 (auth)              <-- 🔒 (Хаалтанд хийсэн нь URL-д харагдахгүй бүлэглэл)
 ┃ ┃ ┃ ┣ 📂 login
 ┃ ┃ ┃ ┃ ┗ 📄 page.tsx        <-- (site.com/login хуудас)
 ┃ ┃ ┃ ┗ 📂 register
 ┃ ┃ ┃   ┗ 📄 page.tsx        <-- (site.com/register хуудас)
 ┃ ┃ ┣ 📂 (main)              <-- 🏠 (Үндсэн сайт буюу нэвтэрсний дараах хуудсууд)
 ┃ ┃ ┃ ┣ 📂 browse
 ┃ ┃ ┃ ┃ ┗ 📄 page.tsx        <-- (site.com/browse - Киноны жагсаалт)
 ┃ ┃ ┃ ┣ 📂 movie
 ┃ ┃ ┃ ┃ ┗ 📂 [id]            <-- (Динамик хуудас. Жнь: site.com/movie/123)
 ┃ ┃ ┃ ┃   ┗ 📄 page.tsx      <-- (Киноны дэлгэрэнгүй мэдээлэл)
 ┃ ┃ ┃ ┗ 📄 layout.tsx        <-- (Дээд Navbar, доод Footer энд байрлана)
 ┃ ┃ ┣ 📂 watch               <-- 🎬 (Кино үзэх хэсэг тусдаа байна)
 ┃ ┃ ┃ ┗ 📂 [id]
 ┃ ┃ ┃   ┗ 📄 page.tsx        <-- (site.com/watch/123 - Зөвхөн тоглуулагч бүтэн дэлгэцээр)
 ┃ ┃ ┣ 📄 globals.css         <-- (Tailwind CSS-ийн үндсэн тохиргоо)
 ┃ ┃ ┗ 📄 layout.tsx          <-- (Бүх сайтын хамгийн гаднах эх бие - RootLayout)
 ┃ ┃
 ┃ ┣ 📂 components            <-- 🧩 2. SHARED UI (Дүлий буюу ерөнхий компонентууд)
 ┃ ┃ ┣ 📂 ui                  <-- (Shadcn UI-аас татаж авсан бэлэн зүйлс)
 ┃ ┃ ┃ ┣ ⚛️ button.tsx        
 ┃ ┃ ┃ ┣ ⚛️ input.tsx         
 ┃ ┃ ┃ ┣ ⚛️ skeleton.tsx      
 ┃ ┃ ┃ ┗ ⚛️ dialog.tsx        
 ┃ ┃ ┗ 📂 layout              <-- (Сайтын ерөнхий араг яс)
 ┃ ┃   ┣ ⚛️ navbar.tsx        <-- (Дээд цэс)
 ┃ ┃   ┗ ⚛️ footer.tsx        <-- (Доод хэсэг)
 ┃ ┃
 ┃ ┣ 📂 features              <-- 🔥 3. FEATURES (Төслийн хамгийн гол ЗҮРХ)
 ┃ ┃ ┃
 ┃ ┃ ┣ 📂 auth                <-- 🔐 А. Нэвтрэх систем
 ┃ ┃ ┃ ┣ 📂 components        <-- (Зөвхөн нэвтрэхэд зориулсан UI)
 ┃ ┃ ┃ ┃ ┣ ⚛️ login-form.tsx  
 ┃ ┃ ┃ ┃ ┗ ⚛️ register-form.tsx
 ┃ ┃ ┃ ┣ 📂 api               <-- (Supabase-тэй харьцах функцүүд)
 ┃ ┃ ┃ ┃ ┗ 📄 auth-actions.ts <-- (login(), logout(), signup() функцүүд)
 ┃ ┃ ┃ ┗ 📂 hooks             <-- (React Hooks)
 ┃ ┃ ┃   ┗ 📄 use-user.ts     <-- (Хэрэглэгч нэвтэрсэн эсэхийг шалгах)
 ┃ ┃ ┃
 ┃ ┃ ┣ 📂 movies              <-- 🍿 Б. Киноны мэдээлэл
 ┃ ┃ ┃ ┣ 📂 components
 ┃ ┃ ┃ ┃ ┣ ⚛️ movie-card.tsx  <-- (Нэг ширхэг киноны зурагтай карт)
 ┃ ┃ ┃ ┃ ┣ ⚛️ movie-row.tsx   <-- (Хөндлөнгөөр гүйлгэдэг киноны жагсаалт)
 ┃ ┃ ┃ ┃ ┗ ⚛️ hero-banner.tsx <-- (Хамгийн дээд талд автоматаар солигдох том зураг)
 ┃ ┃ ┃ ┗ 📂 api
 ┃ ┃ ┃   ┗ 📄 get-movies.ts   <-- (Баазаас кино татаж ирэх функц)
 ┃ ┃ ┃
 ┃ ┃ ┣ 📂 player              <-- 📺 В. Видео тоглуулагч (Vidstack)
 ┃ ┃ ┃ ┣ 📂 components
 ┃ ┃ ┃ ┃ ┣ ⚛️ video-player.tsx<-- (Үндсэн тоглуулагч)
 ┃ ┃ ┃ ┃ ┗ ⚛️ controls.tsx    <-- (Play, Pause, Дуу чангалах товчнууд)
 ┃ ┃ ┃ ┗ 📂 hooks
 ┃ ┃ ┃   ┗ 📄 use-progress.ts <-- (Хэрэглэгч хэд дэх минут дээр үзэж байгааг хадгалах)
 ┃ ┃ ┃
 ┃ ┃ ┗ 📂 billing             <-- 💳 Г. Төлбөр тооцоо (Хэрвээ төлбөртэй бол)
 ┃ ┃   ┣ 📂 components
 ┃ ┃   ┃ ┗ ⚛️ pricing-card.tsx<-- (Үнийн санал харуулах карт)
 ┃ ┃   ┗ 📂 api
 ┃ ┃     ┗ 📄 checkout.ts     <-- (QPay эсвэл Stripe холболт)
 ┃ ┃
 ┃ ┣ 📂 lib                   <-- 🛠️ 4. UTILS & CONFIGS (Туслах хэрэгслүүд)
 ┃ ┃ ┣ 📂 supabase            <-- (Өгөгдлийн сангийн тохиргоо)
 ┃ ┃ ┃ ┣ 📄 client.ts         <-- (Frontend-ээс бааз руу хандах)
 ┃ ┃ ┃ ┗ 📄 server.ts         <-- (Backend-ээс бааз руу хандах)
 ┃ ┃ ┗ 📄 utils.ts            <-- (Төрөл бүрийн жижиг функцүүд. Жнь: цаг хувиргах)
 ┃ ┃
 ┃ ┗ 📂 types                 <-- 🏷️ 5. TYPESCRIPT TYPES (Төрөлжүүлэлт)
 ┃   ┣ 📄 database.types.ts   <-- (Supabase-ээс автоматаар үүсэх баазын бүтэц)
 ┃   ┗ 📄 index.ts            <-- (Movie, User гэх мэт өөрийн бичсэн төрлүүд)
 ┃
 ┣ 📄 .env.local              <-- 🔑 (Нууц үгнүүд, API түлхүүрүүд энд байна. GitHub-д орохгүй!)
 ┣ 📄 next.config.ts          <-- ⚙️ (Next.js-ийн үндсэн тохиргоо)
 ┣ 📄 tailwind.config.ts      <-- 🎨 (Өнгө, фонт, дизайны тохиргоо)
 ┗ 📄 package.json            <-- 📦 (Суулгасан бүх сангуудын жагсаалт)
