# Kubernetes - Vagrant - Ansible

Kubernetes ile birden fazla sunucuyu tek bir sunucudan yöneterek devops süreçlerinin kolayca yönetilmesi amaçlanmaktadır. Sunucuları ayağa kaldırmak için vagrant yazılımı ve sunuculara uygulamaların yüklenmesi için ansible yazılımından yararlanılmıştır.

İlgili uygulamamızda 3 adet sunucu oluşturarak (bir adet master ve 2 adet node, arttırılabilir olarak) bir çalışma ortamı hazırlanmıştır.

Gerekli uygulamalar;
- Vagrant
- Ansible
- Virtualbox

İlgili sunucuları çalıştırmak için;
```bash
vagrant up
```

ilgili sunuculara gereken programlari yüklemek için;
```bash
ansible-playbook k8s-playbook.yml
```

Master sunucuya erişim sağlamak için;
```bash
vagrant ssh k8s-master
```

Master sunucuya bağlı olan tüm sunucuları görmek için master sunucu içerisinde;
```bash
kubectl get nodes
```
