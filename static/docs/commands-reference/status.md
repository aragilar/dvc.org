# status

Show changed stages in the pipeline and mismatches between local cache and cloud
remote.

```usage
    usage: dvc status [-h] [-q] [-v] [-j JOBS] [-c] [-r REMOTE]
                      [targets [targets ...]]

    positional arguments:
      targets               DVC files.

    optional arguments:
      -h, --help            show this help message and exit
      -q, --quiet           Be quiet.
      -v, --verbose         Be verbose.
      -j JOBS, --jobs JOBS  Number of jobs to run simultaneously.
      --show-checksums      Show checksums instead of file names.
      -c, --cloud           Show status of a local cache compared to a remote
                            repository
      -r REMOTE, --remote REMOTE
                            Remote repository to compare local cache to
```

## Examples

```dvc
    $ dvc status

      bar.dvc
              outs
                      changed:  bar
              deps
                      changed:  foo
      foo.dvc
              outs
                      changed:  foo

    $ dvc status -c

        new:      foo

```
