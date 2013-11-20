# Drupal 7 on OpenShift

### Git commands

This repo was created with the following commands:

```
git remote add -f drupal https://github.com/pressflow/7.git
git subtree add --prefix php drupal pressflow-7.23 --squash
```

When a new Drupal version (like 7.24) comes out, you should be able to upgrade it with the following command:

```
git remote add -f drupal https://github.com/pressflow/7.git
git subtree add --prefix php drupal pressflow-7.24 --squash
```

### Creating an app

Note: this won't work in one shot currently. Some order-of-operations things need to be worked out with the environmental variables.

`rhc app-create drupal php-5 mysql-5 cron https://cartreflect-claytondev.rhcloud.com/reflect?github=smerrill/openshift-community-pressflow7 --from-code=https://github.com/smerrill/pressflow-7-quickstart.git`
