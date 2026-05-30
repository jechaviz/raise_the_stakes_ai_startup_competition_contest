# Dealum And Funding Field Notes

## What Dealum Is

Dealum is a deal-flow, accelerator, and early-stage investor management
platform. For this application, it is the external portal where the startup
profile, competition answers, team fields, funding fields, and final
submission state are managed.

Official references:

- Dealum home: https://dealum.com/
- Dealum startup/company FAQ: https://help.dealum.com/en/article/company-startup-faq-89t9s9/
- Dealum accelerator solution: https://dealum.com/solutions/accelerator

## What Funding Total Means

For RAISE eligibility, treat `funding total` as the cumulative amount of
capital already raised by the company before this application.

Use the broadest conservative interpretation unless the form says otherwise:

- equity investment already closed;
- SAFEs or convertible notes already signed;
- non-dilutive grants already awarded;
- accelerator checks already committed;
- debt or venture debt if the form asks for total financing.

Do not include:

- projected revenue;
- pipeline investors;
- verbal interest;
- unsigned grants;
- customer contracts unless the form explicitly asks for revenue.

Current application boundary:

- Eligibility target: below EUR 10,000,000 total funding.
- Current repo value: `secure_input_required_below_eur_10000000`.
- Final submit gate: fill only from verified company records, not memory.

## Safe Dealum Entry Policy

- Use public/product evidence from this repo, the demo, and reusable V/WAIBAv
  receipts.
- Keep legal entity name, RFC/tax identifiers, address, personal documents,
  email, phone, cap table, bank data, and credential material outside the repo.
- Keep founder 2, Paris attendance, exact legal entity, and exact funding total
  as secure session fields until the authenticated Dealum draft is open.
