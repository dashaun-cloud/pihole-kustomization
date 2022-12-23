# pihole-kustomization

```bash
flux create source git pihole \
  --url=https://github.com/dashaun-cloud/pihole-kustomization \
  --branch=main \
  --export > ./clusters/arkansas/pihole-source.yaml
```

## Add the Kustomization

```bash
flux create kustomization pihole \
  --source=pihole \
  --path="./kustomize" \
  --prune=true \
  --export > ./clusters/arkansas/pihole-kustomization.yaml
```