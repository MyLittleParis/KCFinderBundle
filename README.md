KCFinder for symfony2 (unofficial)

http://kcfinder.sunhater.com

Install :
composer
"mylittleparis/kc-finder-bundle": "^1.0"
php composer.phar install 

appkernel
new lib\KCFinderBundle\libKCFinderBundle(),

routing
lib_kcfinder: 
    resource: "@libKCFinderBundle/Resources/config/routing.yml" 
    prefix: /admin

config
lib_kc_finder:
    upload_url: "/uploads/images_articles"
    upload_dir: "%kernel.root_dir%/../web/uploads/images_articles"

security 
security:
    access_control:
        - { path: ^/admin/kcfinder*, role: ADMIN }