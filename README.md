# AG plasm-grafana-dashboard (tested for Dusty)


![screenshot](https://github.com/AGx10k/plasm-grafana-dashboard/blob/master/plasm-dusty-dashboard-screenshot.png?raw=true)


1. `plasm-node --prometheus-external`
2. add job named `dusty` to `prometheus.yml`:
```
  - job_name: dusty
    static_configs:
      - targets: ['Dusty-Validator.host.com:9615', 'Dusty-Sentry.host2.com:9615']

```
3. import json
4. add notification channels to `block sync rate` and `Number of network gossip peers` panels
5. if prometheus job is named not `dusty` (`plasm` for example) then go to Settings\Variables and change `$job`
6. in case prometheus job is not `dusty` need to change it in 2 alerts manually - `block sync rate`, `Number of network gossip peers`:
  

![job name](https://github.com/AGx10k/plasm-grafana-dashboard/blob/master/job-name-in-alert.png?raw=true)
