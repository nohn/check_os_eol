# check_os_eol

`check_os_eol` is a Bash script designed to check the End Of Life (EOL) status of various Linux distributions. It reads the OS version from `/etc/os-release`, compares it with a predefined list of EOL dates, and alerts if the OS is approaching or has surpassed its EOL date.

![GitHub](https://img.shields.io/badge/license-GPLv3-blue.svg)
![GitHub issues](https://img.shields.io/github/issues/pr0j3ctx/check_os_eol)
![GitHub pull requests](https://img.shields.io/github/issues-pr/pr0j3ctx/check_os_eol)
![Icinga Exchange](https://img.shields.io/badge/Icinga-Exchange-blue.svg)

## Features

- Supports multiple major Linux distributions including Ubuntu, Debian, CentOS, RHEL, Fedora, Rocky Linux, AlmaLinux, SUSE, and openSUSE.
- Configurable warning and critical thresholds.
- Provides human-readable output indicating the EOL status.

## Usage

```bash
./check_os_eol.sh [WARN_DAYS] [CRIT_DAYS]
```

- `WARN_DAYS`: Number of days before EOL to issue a warning (default: 90 days).
- `CRIT_DAYS`: Number of days before EOL to issue a critical alert (default: 30 days).
- `-h`: Display help message.

### Examples

Check with default thresholds (90 days for warning, 30 days for critical):

```bash
./check_os_eol.sh
```

Check with custom thresholds (e.g., 60 days for warning, 20 days for critical):

```bash
./check_os_eol.sh 60 20
```

### Help

To display the help message:

```bash
./check_os_eol.sh -h
```

## Output

The script provides output in the following formats:

- `OK`: The OS will not reach EOL soon.
- `WARNING`: The OS will reach EOL within the specified warning period.
- `CRITICAL`: The OS will reach EOL within the specified critical period or is already EOL.
- `UNKNOWN`: The OS or its EOL date could not be determined.

## Supported Distributions

- **Ubuntu**
  - 18.04 (EOL: 2023-04-30)
  - 20.04 (EOL: 2025-04-30)
  - 22.04 (EOL: 2027-04-30)
  - 24.04 (EOL: 2029-04-30)
- **Debian**
  - 10 (EOL: 2024-06-30)
  - 11 (EOL: 2026-06-30)
  - 12 (EOL: 2028-06-30)
- **CentOS**
  - 7 (EOL: 2024-06-30)
  - 8 (EOL: 2021-12-31)
- **RHEL**
  - 7 (EOL: 2024-06-30)
  - 8 (EOL: 2029-05-31)
  - 9 (EOL: 2032-05-31)
- **Fedora**
  - 37 (EOL: 2024-12-31)
  - 38 (EOL: 2025-06-30)
- **Rocky Linux**
  - 8 (EOL: 2029-05-31)
  - 9 (EOL: 2032-05-31)
- **AlmaLinux**
  - 8 (EOL: 2029-05-31)
  - 9 (EOL: 2032-05-31)
- **SUSE**
  - SLES 12 (EOL: 2027-10-31)
  - SLES 15 (EOL: 2031-07-31)
  - openSUSE Leap 15.5 (EOL: 2024-12-31)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/pr0j3ctx/check_os_eol.git
    ```
2. Change into the directory:
    ```bash
    cd check_os_eol
    ```
3. Make the script executable:
    ```bash
    chmod +x check_os_eol
    ```

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss your changes or improvements.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Changelog

### [Unreleased]
- Initial release of `check_os_eol`.

### [1.0.0] - 2024-07-08
- Added support for Ubuntu, Debian, CentOS, RHEL, Fedora, Rocky Linux, AlmaLinux, SUSE, and openSUSE.
- Configurable warning and critical thresholds.
- Added human-readable output indicating the EOL status.
```
