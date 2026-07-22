# ItPay for WorkBuddy

WorkBuddy Skill package with a pinned, offline `@itpay/cli` bundle.

## Package contract

- Uploadable Skill root: `skills/itpay/`.
- Required entry: `skills/itpay/SKILL.md`.
- Runtime: Node.js 18+; no global ItPay install and no runtime npm download.
- Agent Type: `workbuddy` for the whole flow.
- Commands that persist `~/.itpay-v3` require the WorkBuddy Shell call to set `dangerouslyDisableSandbox: true`; denial stops the flow.
- Network scope is limited to the official ItPay Backend. Checkout is displayed for human completion; sensitive payment credentials never enter chat or CLI arguments.

## Distribution rules

WorkBuddy publicly documents local package upload: **Skills → Add Skill → Upload Skill**. Installation performs security checks, and users should be shown local command, file, network, third-party data, and financial-operation disclosures.

WorkBuddy also exposes SkillHub and enterprise self-built Skills, but no public community publisher schema or submission API is documented. First ship and test the local package; do not claim a public SkillHub listing until Tencent provides the publisher route.

## Verify and upload

```bash
npm test
cd skills/itpay
zip -qr ../../itpay-workbuddy-2.0.15.zip .
```

Test on macOS and Windows with no global `itpay`, a path containing spaces, a Chinese OS username, default permission prompts, and a temporary HOME for non-production smoke checks.

Official rules: [WorkBuddy Skills](https://www.workbuddy.cn/docs/workbuddy/From-Beginner-to-Expert-Guide/Function-Description/Skills-Market), [Permission modes](https://www.workbuddy.cn/docs/workbuddy/From-Beginner-to-Expert-Guide/Function-Description/Permission-Modes), [Changelog](https://www.workbuddy.cn/docs/workbuddy/Changelog).
