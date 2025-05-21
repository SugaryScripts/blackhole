```sh
# Initialize Prisma (if not done already)
npx prisma init 

# Run migration 
npx prisma migrate dev --name init

# Generate Prisma client 
npx prisma generate

# Run seed 
npx prisma db seed
```