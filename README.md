# OpenAtrium 2 on OpenShift

### Git commands

This repo was created with the following commands:

```
git remote add -f pressflow-drops https://github.com/phase2/openatrium-drops-7.git
git subtree add --prefix php pressflow-drops master --squash
```

When a new OpenAtrium 2 version (like 7.x-2.13) comes out, you should be able to upgrade it with the following command:

```
git remote add -f pressflow-drops https://github.com/phase2/openatrium-drops-7.git
git subtree pull --prefix php pressflow-drops master --squash
```

### Creating an app

`rhc app-create openatrium php-5.3 mysql-5.1 cron \
  https://cartreflect-claytondev.rhcloud.com/reflect?github=smerrill/openshift-community-pressflow7 \
  --from-code=https://github.com/smerrill/openatrium-2-quickstart.git`
