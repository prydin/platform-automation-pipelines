```
fly -t cp login -n azure-centralus
./1-fly-install-opsman.sh -t cp -p azure-centralus -n install-opsman
fly -t cp up -p install-opsman

./3-fly-install-upgrade-products.sh -t cp -p us-central1-gcp -n install-upgrade-products -s true -o ops-files/resource-gcs.yml
fly -t cp up -p install-upgrade-products

fly -t cp dp -p install-opsman -n
fly -t cp dp -p install-upgrade-products -n
```