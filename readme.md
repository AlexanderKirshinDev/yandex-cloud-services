# Yandex Cloud Services

## Install

Via composer:

    composer require kirshin/yandex-cloud-services

## Yandex Cloud Services for Laravel

## Providers

### Yandex Object Storage

### Usage

After installing this package adds the following code to your config/filesystems.php:

    'yandex' => [
                'driver' => 'yandexcloud',
                'key' => env('YANDEX_ACCESS_KEY_ID'),
                'secret' => env('YANDEX_SECRET_ACCESS_KEY'),
                'bucket' => env('YANDEX_BUCKET_NAME'),
                'region' => 'us-east-1',
    ],
    
And then you can use

    $disk = Storage::disk('yandex');

to get your yandex object storage instance

###### Don't forget to add the Kirshin\YandexCloudServices\Laravel\Providers\ObjectStorage\YandexObjectStorageProvider to your $providers array if your laravel version lower than 5.5
