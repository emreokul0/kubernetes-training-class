# Kubectl Get Pods Commands

1. **kubectl get pods**

    Varsayılan namespace'teki tüm pod'ları listeler.
    - Bu komut, pod'ların isimlerini, durumlarını, yeniden başlama sayısını ve yaşını görüntüler.

    ```bash
    kubectl get pods
    ```

2. **kubectl get pods -n \<namespace>**

    Belirtilen namespace'teki pod'ları listeler. Eğer namespace belirtilmezse varsayılan namespace kullanılır.
    - Namespace'ler, kaynakları gruplamak için kullanılır. Örneğin, prod ve dev gibi ortamlarda ayrım yapabilirsiniz.

    ```bash
    kubectl get pods -n dev
    ```

3. **kubectl get pods --all-namespaces**

    Tüm namespace'lerdeki pod'ları listeler.
    - Bu komut, tüm namespace'lerdeki pod'ları tek seferde görüntülemenizi sağlar. Özellikle tüm küme genelindeki pod'ları izlemek için faydalıdır.

    ```bash
    kubectl get pods --all-namespaces
    ```

4. **kubectl get pods -o wide**

    Pod'lar hakkında genişletilmiş bilgiyle (IP adresi, node, container'lar, vb.) listeler.
    - Bu komut, pod'ların hangi node üzerinde çalıştığını, pod'ların IP adresini ve daha fazla detayı verir.

    ```bash
    kubectl get pods -o wide
    ```

5. **kubectl get pods --selector \<label>**

    Belirli bir etikete (label) sahip pod'ları listeler.
    - Pod'ları, belirli bir etiket (label) ile filtreleyerek listeler. Etiketler, uygulamaları kategorilere ayırmak için kullanılır.

    ```bash
    kubectl get pods --selector app=my-app
    ```

6. **kubectl get pods --field-selector \<field=value>**

    Belirli bir alana göre pod'ları filtreler. Örneğin, belirli bir node üzerinde çalışan pod'ları listeleyebilirsiniz.
    - Bu komut, pod'ların durumu, adı, node adı gibi belirli alanlara göre filtreleme yapar.

    ```bash
    kubectl get pods --field-selector spec.nodeName=node-1
    ```

7. **kubectl get pods --sort-by=\<field>**

    Pod'ları belirli bir alana göre sıralar.
    - Bu komut, listelediğiniz pod'ları örneğin yaşa (AGE) veya yeniden başlama sayısına (RESTARTS) göre sıralamanıza olanak tanır.

    ```bash
    kubectl get pods --sort-by=.status.startTime
    ```

8. **kubectl get pods -o json**

    Pod bilgilerini JSON formatında döner.
    - Bu komut, pod bilgilerini JSON formatında almanızı sağlar. JSON çıktısı genellikle programlama amaçlı veya daha detaylı incelemeler için kullanılır.

    ```bash
    kubectl get pods -o json
    ```

9. **kubectl get pods -o yaml**

    Pod bilgilerini YAML formatında döner.
    - Bu komut, pod bilgilerini YAML formatında döndürür. YAML formatı, Kubernetes kaynakları için standarttır ve pod'ları incelemek ya da yeniden oluşturmak için kullanılır.

    ```bash
    kubectl get pods -o yaml
    ```

10. **kubectl get pods -w**

    Pod'ların durumunu gerçek zamanlı olarak izler.
    - Bu komut, pod'ların durumunu "watch" modunda izlemeye devam eder. Eğer bir pod eklenir, silinir ya da durumu değişirse, bu ekranda gerçek zamanlı olarak güncellenir.

    ```bash
    kubectl get pods -w
    ```

11. **kubectl get pods --show-labels**

    Pod'ların etiketlerini (labels) de gösterir.
    - Bu komut, pod'lar ile birlikte her pod'un sahip olduğu etiketleri de listelemeyi sağlar. Etiketler, kaynakları kategorize etmek için kullanılır.

    ```bash
    kubectl get pods --show-labels
    ```

12. **kubectl get pods --limit=\<number>**

    Belirli sayıda pod'u listeler.
    - Bu komut, çok sayıda pod'un olduğu kümelerde kullanışlıdır. Listeleyeceğiniz pod sayısını sınırlamak için kullanılır.

    ```bash
    kubectl get pods --limit=5
    ```

13. **kubectl get pods --no-headers**

    Pod'ları başlık olmadan (headers olmadan) listeler.
    - Bu komut, çıktıdaki başlık satırını gizler. Özellikle çıktıların işlenmesi gerektiğinde faydalıdır.

    ```bash
    kubectl get pods --no-headers
    ```
