# laravel-code-snippets
Snippets and Helpers I use during a Laravel build.


## .bashrc aliases
```bash
alias clearallcache='php artisan route:clear && php artisan view:clear && php artisan config:clear &&
         php artisan cache:clear && php artisan clear-compiled && composer dump-autoload'

alias cachemeoutside='php artisan route:clear && php artisan view:clear && php artisan config:clear &&
         php artisan cache:clear && php artisan clear-compiled && composer dump-autoload'

alias fixstoragelink='rm -rf /home/forge/mywebsite.com/public/storage && cd /home/forge/mywebsite.com && php artisan storage:link'

alias tarmeup='tar -zcvf "mywebsite-$(date '+%Y-%m-%d').tar.gz" --exclude-from=tar_excludes.txt --exclude-vcs mywebsite.com/'


```



## Nova Snippets
- [Nova Navigation Grouping](#nova-grouping)
- [Nova Label Function](#nova-label)

#### Nova Grouping
[https://nova.laravel.com/docs/1.0/resources/#grouping-resources](https://nova.laravel.com/docs/1.0/resources/#grouping-resources "Nova Grouping")
```php
/**
 * The logical group associated with the resource.
 *
 * @var string
 */
public static $group = 'myGroupName';
```

#### Nova Label

```php
    /**
     * Get the displayble label of the resource.
     *
     * @return string
     */
    public static function label()
    {
        return __('My Label Name');
    }
```
