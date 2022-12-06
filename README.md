# tap-on-tkgs-declarative

This applies the kapp controller apps, namely tap-install-gitops which synchronizes instructions in the packaging subfolder and post-tap-install-gitops that synchronizes whats in the post-packaging subsfolder. The instructions in the packaging subfolder is focused on tap installation. The post-packaging subfolder folder is for additional configuration once tap is installed, e.g. tenant (aka namespace) onboarding, vanity urls, kapp controllers to manage techdocs and/or accelerators.

`kapp deploy -a tap-manager -f ./app -n tap-install`
`kapp deploy -a post-tap-manager -f ./post-app -n tap-install`