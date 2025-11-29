# Training Kubernetes

Menuntut ilmu, belajar kubernetes

## Melihat Nodes

- `kubectl get nodes`


## Melihat Pod

- `kubectl get pod namapod`
- `kubectl get pod -o wide`
- `kubectl describe pod namapod`


## Membuat Pod

- Buat file config dengan ekstensi yaml ikuti seperti di folder templates/
- Eksekusi command `kubectl create -f filepod.yaml` di cli


## Mengakses Pod

- `kubectl port-forward namapod portAkses:portPod` hanya dilakukan untuk test di internal/local kubernetes, tidak berarti akses di internet akan menggunakan cara ini


## Melihat Label

- `kubectl get pods --show-labels`


## Mencari Pod berdasarkan Label

- `kubectl get pods -l key`
- `kubectl get pods -l key=value`
- `kubectl get pods -l '!key'`
- `kubectl get pods -l key!=value`
- `kubectl get pods -l 'key in (val1, val2)'`
- `kubectl get pods -l 'key notin (val1, val2)'`


## Namespace

Adalah grouping sebuah pod/cluster, ini bukan untuk mengisolasi resource karena setiap resource masih bisa berinteraksi satu sama lain

## Melihat namespace

- `kubectl get namespaces`

## Membuat namespace

- `kubectl create -f namafile.yaml`

## Membuat pod di namespace

- `kubectl create -f namafile.yaml --namespace namespace`

## Menghapus namespace

- `kubectl delete namespace namanamespace` semua resource yang ada pada namespace akan ikut terhapus, berhati - hatilah

## Menghapus pod

- `kubectl delete pod namapod`
- `kubectl delete pod namapod1 namapod2 namapod3`
- `kubectl delete pod -l key=value`
- `kubectl delete pod --all --namespace namanamespace`