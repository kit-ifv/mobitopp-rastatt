# mobitopp-rastatt
This project is a mobiTopp example poject to get started with mobiTopp and to test its features.
Please notice that this model does not contain real data about the actual population of the modeled area and therefore cannot be used to estimate the impact of measures on the actual area.

## mobiTopp
[mobiTopp](http://mobitopp.ifv.kit.edu/) is an agent-based travel demand model developed at the [Institute for transport studies at the Karlsruhe Institute of Technology](http://www.ifv.kit.edu/english/index.php). Publications about mobiTopp can be found on the [project site](http://mobitopp.ifv.kit.edu/28.php).

## Execution
### Using gradle
The example project comes shipped with gradle tasks to run it directly from source. A population can be generated with the `run_rastatt_long-term-module` task and travel demand can be simulated using the `run_rastatt_short-term-module_100p` task. 

```
./gradlew clean --refresh-dependencies build run_rastatt_long-term-module run_rastatt_short-term-module_100p
```

### Using .sh or .bat
Additionally, four .sh (resp. .bat) files are included that can be used to run the gradle wrapper without manually typing the commands above.
 - run-clean-build.sh (.bat) refreshes the projects dependencies and compiles the java code
 - run_rastatt_long-term-module.sh (.bat) runs the long-term module to generate a population (includes clean build)
 - run_rastatt_short-term-module_100p.sh (.bat) runs the short-term module to simulate travel demand of 100% of the population (includes clean-build, requires a previously generated population)
 - run_rastatt_short-term-module_10p.sh (.bat) runs the short-term module to simulate travel demand of 10% of the population (includes clean-build, requires a previously generated population)
 - run_rastatt_short-term-module_1p.sh (.bat) runs the short-term module to simulate travel demand of 1% of the population (includes clean-build, requires a previously generated population)

## Results
The results of the long-term module can be found in `output/rastatt`.

The results of the short-term module can be found in `output/results/simulation`.
