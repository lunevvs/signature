# signature

The program which splits the input file on blocks with the selected size and
computes the signature of the each block. The signatures is saved in output
file.


## Usage
```
Usage:
    signature [KEYS]... INPUT_FILE OUTPUT_FILE

DESCRIPTION
    The program which splits the input file on blocks with the selected size
	and	computes the signature of the each block. The signatures is saved in
	output file.

KEYS
    -h, --help
        this message

    --version
        Print version

    -v, --verbose LEVEL (default: WRN)
        Print information verbosly. Possible values: DBG, INF, WRN, ERR.

    -b, --block-size BLOCK_SIZE (default: 1M)
        the size of block on which input file is split. The value supports
        suffixes: K=KiloByte, M=MegaByte, G=GigaByte. A number without suffix
        is KiloBytes.

    -o, --option OPTION
        set special option:
        * sign_algo=[crc32,md5] (default: crc32)
            signature algorithm
        * threads=NUM (default: as many threads as possible)
            number of created threads
        * log_file=<file path> (default: stdout)
            the log file path

EXAMPLES
    signature input.dat output.dat
    signature -b 32K input.dat output.dat -o threads=5
    signature --block-size 32K input.dat out.dat -o sign_algo=md5 -o threads=5
```

