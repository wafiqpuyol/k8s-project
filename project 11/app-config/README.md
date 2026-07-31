This project uses Kustomize, ArgoCD for GitOps and CI/CD along with branch promotion strategy.

Update Staging ENV:-
-> Create a promotional branch for staging env
-> Open a PR to promote the changes to staging

Update Production ENV:-
-> Grab staging env image from argocd & commit to the production promotional branch
-> Open a PR to promote the changes to production env
