1.
git clone https://github.com/sribika/priceping-tst

2.
git checkout -b setup/project-structure

php -v
composer -v

3.
mkdir api client

4.
composer create-project laravel/laravel api

(
    cd api
    php artisan serve
)


5.
npx create-next-app@latest client

(
    cd client
    npm run dev
)

-----------
repo-root/
├── api/        # Laravel backend
└── client/    # Next.js frontend
-----------

7.
Go back to root:
cd ..

git add .

git commit -m "Initialize Laravel backend and Next.js frontend structure"
