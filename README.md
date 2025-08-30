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
