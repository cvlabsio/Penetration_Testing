**Usage**:
   ```
   urlcrazy [options] domain
   ```

**Options**:
   - `-k, --keyboard=LAYOUT`: Specifies the keyboard layout for generating typos. Options include qwerty, azerty, qwertz, dvorak. Default is qwerty.
   - `-p, --popularity`: Checks the popularity of the domain variations using Google search.
   - `-r, --no-resolve`: Disables DNS resolution, useful when you only want to generate domain variations without resolving them.
   - `-i, --show-invalid`: Displays invalid domain names along with valid ones.
   - `-f, --format=TYPE`: Specifies the output format as human-readable, JSON, or CSV. Default is human-readable.
   - `-o, --output=FILE`: Specifies an output file to save the results.
   - `-n, --nocolor`: Disables colorized output.
   - `-d, --debug`: Enables debugging output for development purposes.
   - `-h, --help`: Displays the help menu.
   - `-v, --version`: Prints version information.

**Examples**:
   - Generate domain variations: `urlcrazy example.com`
   - Check popularity of variations: `urlcrazy -p example.com`
   - Show invalid domain names: `urlcrazy -i example.com`
   - Save results to a file: `urlcrazy -o output.txt example.com`
   - Disable colorized output: `urlcrazy -n example.com`
