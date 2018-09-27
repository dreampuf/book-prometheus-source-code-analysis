# Before we read

Check out the source code.

```bash
mkdir -p src/github.com/prometheus/
git clone https://github.com/prometheus/prometheus.git src/github.com/prometheus/prometheus
```

Total Golang source code line
```bash
cd src
wc -l $(for i in $(go list ./...); do find $i -iname '*.go'; done)
```

I'm checking out Prometheus 2.4.2. The instructions above shows 70k lines in total. After exclude testing code, it shows 45k.

# Components of Prometheus 

- cmd
- config
- discovery
- prompb
- promql
- rules engine
- scrape
- storage
- web
