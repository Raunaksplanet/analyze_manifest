# Android Manifest Analyzer

A CLI tool that analyzes AndroidManifest.xml from any **decompiled APK folder**.
It extracts components, exported risks, intent filters, deep links, permissions, and generates a structured security report.
It also auto-saves the output as `<foldername>.txt`.

## Features

* Automatically locates AndroidManifest.xml inside a decompiled APK
* Extracts activities, services, receivers, providers
* Flags exported components and insecure configurations
* Summarizes intent filters and deep link URIs
* Identifies dangerous and signature-level permissions
* Resolves `@string/...` references from `strings.xml`
* Generates both text and JSON reports
* Saves output automatically

## Installation

```bash
git clone https://github.com/yourusername/android-manifest-analyzer
cd android-manifest-analyzer
pip install -r requirements.txt
```

## Usage

### Analyze a decompiled APK folder

```bash
python3 analyze.py <decompiled_folder>
```

### Generate JSON output

```bash
python3 analyze.py <decompiled_folder> -f json
```

### Output Auto-Save

The tool automatically writes:

```
<foldername>.txt
```

## Output Sections

The generated text report includes:

1. Component summary
2. Intent filters and deep links
3. Permissions
4. Security findings
5. Raw data summary

## Command Line Options

| Option                | Description            | Default  |
| --------------------- | ---------------------- | -------- |
| `<decompiled_folder>` | Path to decompiled APK | Required |
| `-f`, `--format`      | `text` or `json`       | `text`   |

## Requirements

* Python 3.6+
* beautifulsoup4

Install with:

```bash
pip install beautifulsoup4
```

## License

MIT License.

## Contributing

Open an issue or submit a PR.
