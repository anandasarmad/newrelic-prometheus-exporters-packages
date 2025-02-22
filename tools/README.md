## docs-specs-generator

This tool helps to automatically generate the spec file and docs for integrations.

In input folder you need to place the prometheus output of the exporter together with the entity
synthesis rules.

The tool is not fully parametrised yet, therefore if you need to change any parameter you can check 
directly the main.go.

Run it with ` go run ./cmd/docs-specs-generator/main.go --prom_metrics_path=etcd.prom`. The output is placed in the output folder.

### What is not automatized

 - You still need to indicate for each metric the unit in the spec file with one of 
   ```
   count, percent, seconds, milliseconds, microsenconds, bytes,
   countPerSecond, bytesPerSecond, bitPerSecond
   ```

 - You still need to add the description of the integration in the docs, it only helps to generate the metrics list with
   the description.   

 - You still need to review is the output makes sense and is compliant with all specifications.
