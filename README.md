# Mini-repo

A minimal repo to measure the overheads of running pants which aren't related to the scale of the repository.

## Performance

### No-ops
```
$ time ./pants goals
...
./pants goals  0.98s user 0.42s system 83% cpu 1.674 total
```

```
$ time ./pants help
...
./pants help  0.99s user 0.42s system 82% cpu 1.711 total
```

### v1
```
$ time ./pants run hello:
...
./pants run hello:  1.99s user 0.62s system 78% cpu 3.330 total
```

### v2

```
$ time ./pants --v2 --no-v1 run hello:
Running target: hello:hello
Hello, World!
hello:hello ran successfully.
./pants --v2 --no-v1 run hello:  1.37s user 0.55s system 80% cpu 2.389 total
```



