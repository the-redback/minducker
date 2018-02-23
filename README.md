# MinDucker

- Carry over docker images from Local Machine to Minikube
- Removes extra dangling images created by old images

```
$ minducker <imagename>
```

## Sample Output

```console
$ minducker maruftuhin/apiserver
REPOSITORY             TAG                 IMAGE ID            CREATED             SIZE
maruftuhin/apiserver   rbac-doc            f48716892153        2 minutes ago       69.6MB
c8307148bbf4: Loading layer [==================================================>]  63.68MB/63.68MB
The image maruftuhin/apiserver:rbac-doc already exists, renaming the old one with ID sha256:851781e3f50c89843c78c851939f12eca60a23c9f843bfed265d5c1407a62bf1 to empty string
Loaded image: maruftuhin/apiserver:rbac-doc
Removing dangling images
Deleted: sha256:851781e3f50c89843c78c851939f12eca60a23c9f843bfed265d5c1407a62bf1
Deleted: sha256:7952556923b02e2bbb2f8e9e8c7879539396ad71a6ba48ba1f9b40eeb19e0d50
```
