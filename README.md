# CloudRip

A tool that helps you find the real IP addresses hiding behind Cloudflare by checking subdomains. For penetration testing, security research, and learning how Cloudflare protection works.

## What it does

- **Fast subdomain scanning** - Uses multiple threads to speed things up
- **Filters out Cloudflare IPs** - Only shows you the real server addresses
- **Bring your own wordlist** - Or use the built-in one (dom.txt)
- **Save your findings** - Export results to a file for later
- **Rate limiting** - Won't spam the target and get you blocked
- **Solid default wordlist** - Organized and comprehensive for better results

## Getting it running

You'll need Python 3 and a couple of libraries:
```bash
pip install colorama pyfiglet
```

## How to use it

Basic usage:
```bash
python3 cloudrip.py example.com
```

With all the options:
```bash
python3 cloudrip.py example.com -w dom.txt -t 20 -o results.txt
```

**Options:**
- `<domain>` - The site you're testing (like example.com)
- `-w <wordlist>` - Your own wordlist (defaults to dom.txt)
- `-t <threads>` - How many threads to run (default is 10)
- `-o <output_file>` - Save results to a file

## Example
```bash
python3 cloudrip.py example.com -w custom_subs.txt -t 20 -o found_ips.txt
```

## Version History

### v2.0.0 (Current)
- **Massive wordlist upgrade** - Took dom.txt from 100 to 600+ subdomains
- Added API variants, cloud infrastructure, IoT endpoints
- Covers auth/security, payment gateways, analytics, CI/CD pipelines
- Way better geo coverage - cities and more countries
- Handles modern cloud-native and microservices setups
- Better database and service discovery hits

### v1.5.0
- Rate limiting so you don't get blocked
- Thread handling works better now
- Doesn't crash on DNS failures anymore
- Prettier output with colors

### v1.0.0
- First drop with the core stuff
- Multi-threaded subdomain scanning
- Filters out Cloudflare IPs
- Bring your own wordlist
- Save results to file
- Basic dom.txt with ~100 entries

## Contributing

Got ideas for improvements? Found a bug? Pull requests and issues are welcome! If it's better wordlists, new features, or bug fixes - all contributions help.

## Important Legal Stuff

**Only use CloudRip on systems you have permission to test.** This tool is for ethical security research, penetration testing with authorization, and educational purposes. Using it against websites without permission is illegal and not cool. You're responsible for how you use this tool.

## License

MIT License - use responsibly.
