git clone https://github.com/elizaOS/babylon.git
cd babylon
bun install

# Setup environment & database
cp .env.example .env
bunx prisma generate
bunx prisma db push
bunx prisma migrate dev
