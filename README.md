# ActiveJob Retry Calculator

A simple browser-based tool to visualize retry schedules for Rails ActiveJob's `retry_on` method.

## The Problem

When using ActiveJob's `retry_on` with `:polynomially_longer`, it's hard to mentally calculate how long retries will take and when they'll occur. This tool shows you exactly what will happen.

## Usage

**Online:** https://flixt.github.io/activejob-retry-calculator/

**Local:** Open `index.html` in your browser. No server or dependencies required.

## Features

- **Wait Strategy**: Choose between `:polynomially_longer` or a fixed duration
- **Attempts**: Configure total attempts (including the original execution)
- **Jitter**: Set the random delay factor (default 0.15 = 15%)
- **Live Code Preview**: See the equivalent `retry_on` call
- **Retry Table**: View each attempt with wait times and cumulative durations
- **Min/Max Ranges**: Account for jitter randomness in timing estimates

## Disclaimer

This is an independent tool and is not affiliated with or endorsed by Rails or the Rails core team. The retry formula is based on publicly documented behavior from the [ActiveJob source code](https://github.com/rails/rails/blob/main/activejob/lib/active_job/exceptions.rb).

## License

MIT - see [LICENSE](LICENSE)
