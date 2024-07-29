# AmneziaVPN Config Decoder &amp; Encoder

This Python script converts AmneziaVPN configurations between Base64-encoded strings and JSON format.

## Requirements

Python 3 or higher (tested with Python 3.12)

## Usage

The script supports both encoding and decoding configurations:

**Decoding:**

```bash
python amnezia-config-decoder.py vpn://AAAGX.. [-o output.json]
```

* `vpn://AAAGX..`: The Base64-encoded string containing the AmneziaVPN configuration.
* `-o output.json`: (Optional) Path to the JSON file where the decoded configuration will be saved. If not specified, the configuration will be printed to the console.

**Encoding:**

```bash
python amnezia-config-decoder.py -i input.json
```

* `-i input.json`: Path to the JSON file containing the configuration to encode.

## Examples

**Decode a Base64 string to the console:**

```bash
python amnezia-config-decoder.py vpn://AAAGX..
```

**Decode a Base64 string and save to a file:**

```bash
python amnezia-config-decoder.py vpn://AAAGX.. -o config.json
```

**Encode a JSON configuration from a file:**

```bash
python amnezia-config-decoder.py -i config.json
```

## Background

AmneziaVPN uses a custom string encoding scheme to represent configurations. This script replicates the AmneziaVPN application encoding and decoding logic **without using Qt**, allowing you to work with configs in a much readable JSON format.

## Contributing

Contributions are welcome! Please open an issue or pull request if you have any suggestions or bug reports.

## License

This project is licensed under the GPL-3.0 license.
