# learn-helm

Learn helm!

For example:

If you want deploy a instance like

| key           | value                   |
| ------------- | ----------------------- |
| chart name    | haishen                 |
| instance name | haishen                 |
| image         | yuhenabc/haishen:latest |

in `test` namespace, there will be two ways to choosen from:

### command line values way

```bash
helm install --set nameOverride=haishen,image.repository=yuhenabc/haishen haishen ./webapp -n test
```

### yaml values way

```bash
helm install -f ./values/haishen.yaml haishen ./webapp -n test
```

In `./values/haishen.yaml`:

```yaml
nameOverride: haishen
image:
  repository: yuhenabc/haishen
  tag: latest
```
