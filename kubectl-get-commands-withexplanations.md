# Kubectl Get Commands

İşte Kubernetes'te kullanılan `kubectl get` komutlarının detaylı açıklamalarıyla birlikte bir tablo:

| **Komut**                                        | **Açıklama**                                                                                 |
|--------------------------------------------------|----------------------------------------------------------------------------------------------|
| `kubectl get pods`                               | Bulunduğunuz namespace içindeki tüm pod'ları listeler.                                        |
| `kubectl get pods --all-namespaces`              | Tüm namespace'ler altındaki tüm pod'ları listeler.                                            |
| `kubectl get pods -o wide`                       | Pod'ların genişletilmiş bilgilerini (Node adı, IP adresi, vs.) gösterir.                      |
| `kubectl get pods -n <namespace>`                | Belirtilen namespace içindeki tüm pod'ları listeler.                                          |
| `kubectl get pods --field-selector=status.phase=Running` | Sadece `Running` durumundaki pod'ları listeler.                                     |
| `kubectl get pods -o json`                       | Pod'ların listesini JSON formatında gösterir.                                                 |
| `kubectl get pods -o yaml`                       | Pod'ların listesini YAML formatında gösterir.                                                 |
| `kubectl get pods --sort-by=.metadata.name`      | Pod'ları isimlerine göre sıralayarak listeler.                                                |
| `kubectl get pods --selector=<etiket-anahtar>=<etiket-değeri>` | Belirtilen etikete sahip pod'ları listeler.                                      |
| `kubectl get pods -l app=<uygulama-adı>`         | Belirtilen uygulama etiketiyle eşleşen pod'ları listeler.                                     |
| `kubectl get pod <pod-adı> -o yaml`              | Belirtilen pod hakkında ayrıntılı bilgiyi YAML formatında gösterir.                           |
| `kubectl get pods --watch`                       | Pod'lardaki değişiklikleri gerçek zamanlı olarak izler.                                       |
| `kubectl get pods --no-headers`                  | Pod'ları başlıklar olmadan listeler (özellikle betiklerde kullanışlıdır).                     |
| `kubectl get pods --output=custom-columns=<özellikler>` | Özelleştirilmiş sütunlarla pod'ları listeler.                                     |
| `kubectl describe pod <pod-adı>`                 | Belirtilen pod hakkında detaylı bilgiyi gösterir.                                             |
| `kubectl get services`                           | Bulunduğunuz namespace içindeki tüm servisleri listeler.                                      |
| `kubectl get services --all-namespaces`          | Tüm namespace'lerdeki servisleri listeler.                                                    |
| `kubectl get services -o wide`                   | Servislerin genişletilmiş bilgilerini (Cluster IP, Portlar, vs.) gösterir.                    |
| `kubectl get services -n <namespace>`            | Belirtilen namespace içindeki servisleri listeler.                                            |
| `kubectl get nodes`                              | Kubernetes kümesindeki tüm node'ları listeler.                                                |
| `kubectl get nodes -o wide`                      | Node'lar hakkında genişletilmiş bilgileri (Kapasite, Kullandıkları Kaynaklar, IP'ler) gösterir.|
| `kubectl get namespaces`                         | Kubernetes kümesindeki tüm namespace'leri listeler.                                           |
| `kubectl get deployments`                        | Deployment objelerini listeler.                                                              |
| `kubectl get deployments --all-namespaces`       | Tüm namespace'lerdeki deployment'ları listeler.                                               |
| `kubectl get replicasets`                        | ReplicaSet objelerini listeler.                                                              |
| `kubectl get configmaps`                         | Belirtilen namespace içindeki configmap'leri listeler.                                        |
| `kubectl get secrets`                            | Belirtilen namespace içindeki secret'ları (gizli veriler) listeler.                           |
| `kubectl get ingress`                            | Belirtilen namespace içindeki ingress kaynaklarını listeler.                                  |
| `kubectl get events`                             | Kubernetes olaylarını (events) listeler.                                                      |

Bu tablo, Kubernetes'deki temel `kubectl get` komutlarının ayrıntılı bir açıklamasını sağlar ve çeşitli Kubernetes objelerinin nasıl listelenebileceğini gösterir.
