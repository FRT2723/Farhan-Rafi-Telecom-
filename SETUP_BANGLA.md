# মোবাইল থেকে চালানোর সহজ গাইড

১) এই ZIP ফাইলটি ডাউনলোড করে কোনো Git hosting/Cloud IDE-তে তুলুন।
২) Backend চালাতে PostgreSQL database তৈরি করুন এবং `.env.example` থেকে `.env` বানান।
৩) DATABASE_URL ও JWT_SECRET বসান।
৪) `npm install`, `npx prisma generate`, `npx prisma migrate dev --name init`, `npm run seed` চালান।
৫) Backend-এর public HTTPS URL নিন এবং Flutter-এর `app/lib/config.dart`-এ বসান।
৬) Flutter project build করে Android APK বানান: `flutter build apk --release`.

নোট: bKash merchant/app credentials এবং recharge provider-এর API credentials ছাড়া live payment/recharge করা যাবে না। এগুলো `.env`-এ রাখবেন, অ্যাপের ভিতরে নয়।
