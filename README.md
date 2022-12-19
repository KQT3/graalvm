### Setup Graalvm

```
export PATH=/path/to/<graalvm>/bin:$PATH
  
export JAVA_HOME=/path/to/<graalvm>

export PATH=/graalvm-ce-java19-22.3.0/bin:$PATH
export JAVA_HOME=/graalvm-ce-java19-22.3.0
```

### Mvn build graalvm

```
mvn -Pnative native:compile
```

### Run graalvm build

```
target/graalvm
```

### Build time

```
mvn clean package = [INFO] Total time:  4.222 s
mvn -Pnative native:compile = [INFO] Total time:  01:53 min
```

### Check memory

```
sudo dnf install ps_mem
ps_mem -p <pid>

without graalvm = 216.4 MiB
With graalvm = 63.8 MiB
216 / 63 = 3.4 = 340% more lightweight in memory
```
