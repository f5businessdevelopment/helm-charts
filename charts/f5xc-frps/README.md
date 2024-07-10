## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  `helm repo add f5businessdevelopment https://f5businessdevelopment.github.io/helm-charts`

If you had already added this repo earlier, run `helm repo update` to retrieve the latest versions of the packages.  You can then run `helm search repo f5businessdevelopment` to see the charts.

To install the f5xc-frps chart:

    `helm install my-releasename f5businessdevelopment/f5xc-frps`

    `helm install --dry-run --set-file caCert=certs/ca.crt --set-file serverCert=certs/server.crt --set-file serverKey=certs/server.key my-release f5businessdevelopment/f5xc-frps`

To uninstall the chart:

    helm delete my-releasename
