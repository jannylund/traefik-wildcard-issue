# Traefik issue with triggering ACME

NOTE! - This example uses example.com domain and can not be used for real. Do a find and replace on `example.com` and update email in `traefik.yaml` to make it work.


# PROBLEM

Without a dynamic file provider, there are no requests for certificates happening.


This example has a file provider with the default generated wildcard cert in the file `dynamic.yaml`. This works properly, but moving the configuration into `traefik.yaml` and not using the `providers.file` does not work.