To test compile caching for a given goal G:

1. Remove "last run" fingerprints: `./pants clean-all`
2. Remove the cache: `rm -rf .local_cache`
3. Execute the goal: `./pants <G> src/java/org/example`
4. Check the cache: `ls .local_cache/pants_backend_jvm_tasks_jvm_compile_zinc_zinc_compile_ZincCompile/src.java.org.example.example/`

Rinse and repeat for different goals.
