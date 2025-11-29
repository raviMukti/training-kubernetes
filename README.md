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