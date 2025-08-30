argocd login argocd.gcp.YOURDOMAIN.COM --insecure


argocd app create demoapp1\
      --repo "https://github.com/lazyllmg/argoapps.git" \
      --path "demoapp1" \
      --dest-server "https://kubernetes.default.svc" \
      --dest-namespace "demoapp1" \
      --revision "master" \
      --sync-policy "automated" \
      --auto-prune \
      --self-heal

argocd app create demoapp2\
      --repo "https://github.com/lazyllmg/argoapps.git" \
      --path "demoapp2" \
      --dest-server "https://kubernetes.default.svc" \
      --dest-namespace "demoapp2" \
      --revision "master" \
      --sync-policy "automated" \
      --auto-prune \
      --self-heal

argocd app create boutique-prod \
      --repo "https://github.com/lazyllmg/argoapps.git" \
      --path "boutique/prod" \
      --dest-server "https://kubernetes.default.svc" \
      --dest-namespace "boutique-prod" \
      --revision "master" \
      --sync-policy "automated" \
      --auto-prune \
      --self-heal
