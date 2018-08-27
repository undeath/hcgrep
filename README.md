# hcgrep

hcgrep allows using grep with [hashcat mask](https://hashcat.net/wiki/doku.php?id=mask_attack) syntax

## Usage

hcgrep works just like grep with hashcat masks. Most grep options work, altough some do not make sense or may break hcgrep's functionality.


	usage: hcgrep [-h] [--mask-match-mode {a,f,s,e}]
				  [--custom-charset1 CUSTOM_CHARSET1]
				  [--custom-charset2 CUSTOM_CHARSET2]
				  [--custom-charset3 CUSTOM_CHARSET3]
				  [--custom-charset4 CUSTOM_CHARSET4]
				  mask

	Run grep with a hashcat mask

	positional arguments:
	  mask

	optional arguments:
	  -h, --help            show this help message and exit
	  --mask-match-mode {a,f,s,e}, --mm {a,f,s,e}
							desired matching mode, [a]ny, [f]ull, [s]tart, [e]nd.
							Default: a
	  --custom-charset1 CUSTOM_CHARSET1, -1 CUSTOM_CHARSET1
	  --custom-charset2 CUSTOM_CHARSET2, -2 CUSTOM_CHARSET2
	  --custom-charset3 CUSTOM_CHARSET3, -3 CUSTOM_CHARSET3
	  --custom-charset4 CUSTOM_CHARSET4, -4 CUSTOM_CHARSET4

	Any desired grep options can be appended to the command line

## Requirements

* GNU grep
* Python 3


## Technical Details

hcgrep converts a given mask into grep regex and then calls grep. It will have roughly the same performance as grep.

