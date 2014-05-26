# Symfony

- Buat [proyek](http://symfony.com/doc/current/book/installation.html): ```composer create-project symfony/framework-standard-edition symfony 2.4.*```
- Masukkan jenis basis data `pdo_sqlite` saat diminta
- Buka laman http://pfwlab.local/symfony/web/app_dev.php/ untuk mengonfirmasi bahwa instalasi berhasil
- Buat bundel HelloWorld: ```php app/console generate:bundle --namespace=Pfw/Bundle/HelloWorldBundle```
    - Nama bundel: enter
    - Direktori: enter
    - Konfigurasi: annotation
    - Struktur: yes
    - Konfirmasi: enter
    - Perbarui kernel: enter
    - Perbarui routing: enter
- Ubah src/Pfw/Bundle/HelloWorldBundle/Controller/DefaultController.php
```php
    /**
     * @Route("/")
     * @Route("/hello/{name}")
     * @Template()
     */
    public function indexAction($name = 'World')
    {
        return array('name' => $name);
    }
```
- Bersihkan cache: ```php app/console cache:clear -e prod```
- Buang bundel standar: [How to remove the AcmeDemoBundle](http://symfony.com/doc/current/cookbook/bundles/remove.html)
- Buka laman http://pfwlab.local/symfony/web/

- Unduh Bootstrap http://getbootstrap.com/getting-started/#download
