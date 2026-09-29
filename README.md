# BestRemit Agent Plugin

Compare money transfer apps before sending money abroad. BestRemit gives compatible AI agents access to live reference FX rates and indicative remittance quotes through the hosted BestRemit MCP server.

## Overview

BestRemit helps users compare available international money transfer options side by side, including exchange rates, transfer fees, payment methods, and estimated recipient amounts.

The plugin is read-only and informational. It does **not**:

- initiate or execute money transfers;
- access bank accounts, balances, or payment credentials;
- track transfers created with third-party providers;
- debit funds, authorize payments, or modify financial accounts.

Transfers are completed directly with the third-party provider selected by the user.

## MCP server

This repository is the open-source plugin package. The production MCP service is hosted separately at:

`https://bestremit.app/api/mcp/mcp`

Transport: Streamable HTTP.

No API key or BestRemit account is required to use the comparison tools.

## Tools

### `compare_remittance_quotes`

Compare live or current indicative offers from supported money transfer apps for a source currency, destination currency, and send amount. Results can include provider availability, exchange rates, fees, payment methods, provider links, and estimated recipient amounts.

Example prompts:

- `I want to send $1,000 from the US to China. Which money transfer app could leave my recipient with the most CNY?`
- `Which money transfer apps can I use to send €500 from Germany to the UK? Compare fees, exchange rates, and how much arrives.`
- `I'm sending 10,000 USD to India. Which money transfer apps have an available offer, and how much would my recipient get?`

### `get_fx_rate`

Check BestRemit's current reference exchange rate for a currency pair.

Example prompts:

- `What is the current USD to CAD exchange rate?`
- `What is 1 JPY worth in CNY right now?`

## Providers

BestRemit compares offers from supported providers such as Wise, Remitly, Western Union, Xoom, Instarem, Panda Remit, LemFi, OFX, and others where available. Provider availability varies by transfer route and amount.

## Installation

### Cursor Marketplace

After the plugin is listed:

1. Open **Customize** in Cursor.
2. Find **BestRemit** in the Marketplace.
3. Select **Install** and choose user or project scope.
4. Ask Cursor to compare a transfer route or check an FX rate.

### Local testing before submission

Copy this repository to Cursor's local plugin directory:

```bash
mkdir -p ~/.cursor/plugins/local/bestremit
cp -R . ~/.cursor/plugins/local/bestremit/
```

Restart Cursor or run **Developer: Reload Window**, then open **Customize** and confirm that the BestRemit MCP server is available.

## Data and financial disclosures

- Quotes, exchange rates, fees, and recipient amounts are estimates and may change.
- Users should check the provider's final offer before sending money.
- BestRemit is an independent informational comparison service and does not process payments or hold funds.
- Some provider links may be affiliate referral links. BestRemit may earn a commission at no additional cost to the user.
- BestRemit states that rankings are based on estimated recipient outcomes rather than sponsored placement.
- No BestRemit account or banking details are required to compare offers.

See the [BestRemit Privacy Policy](https://bestremit.app/privacy) and [Terms of Service](https://bestremit.app/terms).

## Security

Please report security issues privately. See [SECURITY.md](SECURITY.md).

## License

The plugin packaging/configuration in this repository is licensed under the MIT License. BestRemit's hosted service, backend implementation, name, and brand assets are not licensed by this repository except as necessary to identify and distribute this plugin. See [NOTICE](NOTICE).

## Support

- Website: https://bestremit.app
- Email: support@bestremit.app
