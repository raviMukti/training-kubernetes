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

- `kubectl port-forward namapod portAkses:portPod` hanya dilakukan untuk test di internal/local kubernetes, tidak berarti akses diinternet akan menggunakan cara ini
