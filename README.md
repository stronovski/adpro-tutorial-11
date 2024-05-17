## 1. Compare the application logs before and after you exposed it as a Service.

Setelah service di-expose, maka log akan mencatat setiap request yang diterima oleh service. Seperti halnya dalam contoh berikut ketika dilakukan refresh dalam aplikasi sehingga log akan bertambah setiap waktu.

Sebelum:
![alt text](image-1.png)

Setelah:
![alt text](image.png)

Dapat dilihat bahwa catatan log juga akan mencatat permintaan yang masuk yang kemudian akan dialihkan melalui Service yang dapat menyediakan akses eksternal ke aplikasi, seperti permintaan GET /


## 2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to
`kube-system`.

Dengan menggunakan -n, service yang diinginkan berarti merupakan service yang berada di dalam namespace tersebut, sehingga dapat menitikberatkan fokus get pada namespace setelah query -n. Hal ini akan diperlukan ketika terdapat beberapa service yang memiliki nama yang sama, tetapi dengan tujuan berbeda dan memiliki namespace yang tersebar.