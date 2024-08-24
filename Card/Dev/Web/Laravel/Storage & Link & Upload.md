```php
// "/storage/data"
Storage::url($file)

// "http://localhost:8000/assets/images/icon/document.png"
asset('assets/images/icon/document.png')

// "/home/fryctze/Documents/Project/Laravel/fordas/public/data"
public_path('data')

// "/home/fryctze/Documents/Project/Laravel/fordas/storage/data"
storage_path('data')
```

###### Upload Delete
```php
Storage::delete('public/' . $this->DOC_PATH . $data->filename);
UploadHelper::storeAs($this->map_file, 'public/'.$this->MAP_PATH, '.kml');

class UploadHelper {  
    public static function store($file, $path){  
        if ($file) return basename($file->store($path));  
        return '';  
    }  
    public static function storeAs($file, $path, $ext){  
        if ($file) return basename($file->storeAs($path, Str::random(40).$ext));  
        return '';  
    }  
    public static function getOriginalName($file){  
        return isset($file) ? $file->getClientOriginalName() : '';  
    }  
}
```