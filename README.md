# Exercism Canonical Data Syncer

This small application is used to help Exercism tracks keep their exercise-specific `tests.toml` files in sync with the latest canonical data in the [problem-specifications repo](https://github.com/exercism/problem-specifications).

## Usage

The application is a single binary and can be used as follows:

```
Usage: canonical_data_syncer [options]

Options:
  -e, --exercise <slug>        Only sync this exercise
  -c, --check                  Check if there missing tests. Doesn't update the tests. Terminates with a non-zero exit code if any one or more test cases are missing.
  -d, --default <mode>         What to do with missing test cases. Allowed values: c[hoose], i[nclude], e[xclude]
  -o, --verbosity <verbosity>  The verbosity of output. Allowed values: q[uiet], n[ormal], d[etailed]
  -h, --help                   Show CLI usage
  -v, --version                Display version information
```

Running the application will prompt the user to choose whether to include or exclude missing tests. It will update the `tests.toml` file accordingly. If you only want a quick check, you can use the `--check` option.

## Use in your track

To use the application in your track, you can copy the [`scripts/fetch-canonical_data_syncer`](./scripts/fetch-canonical_data_syncer) and/or [`scripts/fetch-canonical_data_syncer.ps1`](./scripts/fetch-canonical_data_syncer.ps1) files to your track's repository. Running either of these scripts will download the latest version of the `canonical_data_syncer` tool to your track's `bin` directory.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/exercism/canonical-data-syncer.