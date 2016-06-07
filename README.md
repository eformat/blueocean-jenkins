-- install jenkins using template (need to custom build)
oc new-project ci2
oc new-app ./jenkins-persistent-template.yaml
oc deploy jenkins --latest

-- dependencies if you need to install manually through configure jenkins
blueocean-dashboard
sse-gateway

blueocean-web
metrics (3.0.9), variant (1.0) doesn't exist

blueocean-plugin
blueocean-commons (1.0-SNAPSHOT), blueocean-web (1.0-SNAPSHOT), github-branch-source, blueocean-rest (1.0-SNAPSHOT), favorite (1.16)
