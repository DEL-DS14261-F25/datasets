# datasets
Datasets needed for various assignments


## Loading and saving data from external sources - Google Colab

### Uploading files from your local file system

```
from google.colab import files
uploaded = files.upload()
```

### Downloading files to your local file system

```
from google.colab import files
with open('example.txt', 'w') as f:
  f.write('some content')
files.download('example.txt')
```

## Mounting Google Drive

```
from google.colab import drive
drive.mount('/content/drive')
with open('/content/drive/My Drive/foo.txt', 'w') as f:
  f.write('Hello Google Drive!')
!cat /content/drive/My\ Drive/foo.txt
drive.flush_and_unmount()
print('All changes made in this colab session should now be visible in Drive.')
```

