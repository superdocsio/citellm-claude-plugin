# CiteLLM for Claude

CiteLLM checks claims against your PDFs. Claude reads the PDF you attach, decides
whether each claim is supported, partially supported, contradicted or not covered,
and CiteLLM locates the exact source passage. A viewer opens inside the
conversation with every passage highlighted, so you can jump from a claim to its
evidence, and you can export a highlighted PDF or an evidence report.

This plugin connects Claude to the CiteLLM service at `https://mcp.citellm.com/mcp`
and adds a skill that guides Claude through reading, validating and reviewing
evidence. It works in Claude chat, Cowork and Claude Code.

## Try it

Attach a PDF and ask, for example:

- "Verify these claims against my attached PDF and highlight the evidence."
- "What were fiscal 2025 net sales and employee numbers in this 10-K? Show me where each figure comes from."
- "Compare the termination clauses in these two contracts."

## Sign in

The first time Claude uses CiteLLM, it asks you to connect your CiteLLM account.
Sign in with Google. A free account is created automatically; paid plans have
higher limits. Ask Claude to "check my CiteLLM allowance" to see yours.

In Claude chat and Cowork, Claude sends your attachment to CiteLLM from its code
sandbox. Allow `mcp.citellm.com` under **Settings → Capabilities → Code execution
and file creation → Network access**. Otherwise Claude offers a picker where you
select the PDF yourself.

## Your data

- Only the PDFs you attach or select are sent to CiteLLM, which extracts their text
  to find quotations. Your PDFs are private to your account.
- PDFs are temporary and expire automatically, unless your account saves them. Ask
  Claude to delete a PDF from CiteLLM at any time.
- CiteLLM stores your sign-in identity and email and your usage counts to apply
  your plan's limits.
- CiteLLM confirms where each quotation appears in the PDF. The assessment of each
  claim is Claude's, not an independent fact check.

See the [privacy policy](https://citellm.com/privacy) and
[terms of service](https://citellm.com/terms).

## Install in Claude Code

```sh
claude plugin marketplace add superdocsio/citellm-claude-plugin
claude plugin install citellm@superdocs
```

## Support

Email [citellm@superdocs.io](mailto:citellm@superdocs.io), or see [citellm.com/claude](https://citellm.com/claude).
CiteLLM is made by Superdocs.
