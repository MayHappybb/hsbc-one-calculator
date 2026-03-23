# HSBC One Calculator

A simple web calculator to help HSBC HK One account holders calculate how much they need to remit to meet the HKD $10,000 average balance requirement.

![Calculator Preview](./preview.png)

## Background

Non-Hong Kong ID holders who open an HSBC One account must maintain an average "全面理财总值" (Total Relationship Balance) of HKD $10,000 for the first 3 full calendar months. If not met, a monthly service fee of HKD $100 is charged.

This tool helps you calculate exactly how much additional deposit is needed based on your remittance history.

## Features

- 📅 **Account Opening Date Input** - Specify when you opened your account
- 💰 **Multiple Remittance Tracking** - Add all your deposits with dates and amounts
- 📊 **Smart Calculation** - Automatically calculates:
  - Assessment period (first 3 full calendar months)
  - Current balance-days accumulated
  - Required additional deposit amount
  - Days remaining until assessment ends
- 🎨 **Clean UI** - Claude-inspired minimal design, easy to use
- 🔒 **Privacy First** - No registration, no data storage, everything runs locally

## How to Use

1. Open `index.html` in your browser
2. Enter your account opening date
3. Add your remittances (date + amount in HKD)
4. Click "Calculate Requirements"
5. See the required additional deposit to meet the HKD $10,000 average

### Example

If you opened your account on **Feb 23, 2026** and remitted **HKD $3,000** on **Mar 13, 2026**:

- Assessment Period: Mar 1 - May 31, 2026 (92 days)
- Current Balance-Days: 3,000 × 79 days = 237,000
- Required Balance-Days: 10,000 × 92 = 920,000
- **Additional Deposit Needed: ~HKD $8,645**

## Calculation Logic

The calculator uses the following formula:

```
Daily Average = Sum of (Balance × Days) / Total Days ≥ 10,000
```

Where:
- **Assessment Period**: First 3 full calendar months after account opening
- **Balance-Days**: Amount deposited × number of days it contributes to the period
- **Target**: 10,000 HKD × total assessment days

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No server required - runs entirely client-side

## Local Development

```bash
# Clone the repository
git clone https://github.com/mayhappy/hsbc-one-calculator.git

# Navigate to project
cd hsbc-one-calculator

# Start local server (optional)
python3 -m http.server 9090

# Open http://localhost:9090
```

Or simply open `index.html` directly in your browser.

## Disclaimer

This calculator is for reference only. Please verify with HSBC for official requirements and fee structures. The developer is not responsible for any discrepancies or financial decisions made based on this tool.

## License

MIT License - Feel free to use and modify.

---

Made with ❤️ for HSBC One account holders in Hong Kong.
