![Records](https://img.shields.io/badge/records-1639-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Price](https://img.shields.io/badge/price-49-brightgreen)

# DeFi Protocol Risk Metrics

Comprehensive risk metrics dataset for decentralized finance protocols, including smart contract vulnerabilities, protocol health scores, and security classifications.

## Dataset Overview

## Data Dictionary

| Field | Type | Description |
|-------|------|-------------|
| protocol_name | string | DeFi protocol identifier |
| health_factor | float | Collateralization ratio |
| liquidation_threshold | float | LTV at which liquidation triggers |
| ltv_ratio | float | Loan-to-value percentage |
| collateral_amount | float | USD value of collateral |
| borrow_amount | float | USD value borrowed |
| oracle_deviation_pct | float | Oracle price deviation from spot |
| borrow_apy | float | Annual borrow rate |
| supply_apy | float | Annual supply rate |
| tvl_usd | float | Total value locked in USD |
| severity | string | Risk severity: critical/high/medium/low |
| risk_category | string | Type of risk |



| Property | Value |
|----------|-------|
| **Total Records** | 3,000 |
| **Sample Included** | 100 rows |
| **License** | CC-BY-SA-4.0 |
| **Price (Full)** | $49 |

## Purchase Full Dataset

The complete dataset (3,000 records) is available for purchase:

- **Store:** [https://payhip.com/Manteclaw](https://payhip.com/Manteclaw)
- **Email:** manteclaw@proton.me

## Files

| File | Description |
|------|-------------|
| `sample_data.csv` | 100-row representative sample |
| `metadata.json` | Dataset schema, tags, pricing |
| `notebooks/starter.ipynb` | Jupyter notebook for exploration |

## Sample Preview (first 10 rows)

| id | category | severity | title | description | vulnerable_code | fixed_code | fix_pattern | language | compiler_version | context | is_synthetic | generation_timestamp | variant_seed |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SYNTH-00001451-00019 | front_running | medium | Front Running in money_market contract (variant 1451) | Integer overflow in money_market balance calculation | function addBalance(uint256 amount) public {     balance ... | function addBalance(uint256 amount) public {     uint256 ... | secure-pattern | solidity | 0.8.22 | money_market | True | 2026-08-08T00:01:52.555828+00:00 | 1451 |
| SYNTH-00009496-00056 | front_running | critical | Front Running in staking contract (variant 9496) | Delegatecall vulnerability in staking proxy pattern | // Variant 9496: staking function upgrade(address newImpl... | function upgrade(address newImplementation) public onlyOw... | secure-pattern | solidity | 0.8.19 | staking | True | 2026-08-08T00:01:52.427301+00:00 | 9496 |
| SYNTH-00005560-00002 | arbitrary_external_call | medium | Arbitrary External Call in options contract (variant 5560) | Unprotected selfdestruct in options contract | // Variant 5560: options function destroy() public {     ... | function destroy() public onlyOwner {     emit ContractDe... | secure-pattern | solidity | 0.8.19 | options | True | 2026-08-08T00:01:52.416297+00:00 | 5560 |
| SYNTH-00000232-00026 | proxy_storage_collision | medium | Proxy Storage Collision in insurance contract (variant 232) | tx.origin authentication bypass in insurance | function transferOwnership(address newOwner) public {    ... | function transferOwnership(address newOwner) public onlyO... | secure-pattern | solidity | 0.8.19 | insurance | True | 2026-08-08T00:01:52.448303+00:00 | 232 |
| SYNTH-00007098-00003 | reentrancy_read | high | Reentrancy Read in lending contract (variant 7098) | Flash loan attack vector in lending price calculation | function getCollateralValue() public view returns (uint25... | // Variant 7098: lending function getCollateralValue() pu... | pull-over-push | solidity | 0.8.19 | lending | True | 2026-08-08T00:01:52.443300+00:00 | 7098 |
| SYNTH-00009941-00014 | reentrancy_no_eth | low | Reentrancy No Eth in options contract (variant 9941) | Single-source price oracle vulnerable to manipulation in ... | function getPrice() public view returns (uint256) {     r... | function getPrice() public view returns (uint256) {     (... | pull-over-push | solidity | 0.8.19 | options | True | 2026-08-08T00:01:52.441300+00:00 | 9941 |
| SYNTH-00005942-00071 | access_control | critical | Access Control in staking contract (variant 5942) | Delegatecall vulnerability in staking proxy pattern | // Variant 5942: staking function upgrade(address newImpl... | function upgrade(address newImplementation) public onlyOw... | secure-pattern | solidity | 0.8.22 | staking | True | 2026-08-08T00:01:52.430301+00:00 | 5942 |
| SYNTH-00004358-00019 | signature_replay | low | Signature Replay in bridge contract (variant 4358) | Delegatecall vulnerability in bridge proxy pattern | // Variant 4358: bridge function upgrade(address newImple... | function upgrade(address newImplementation) public onlyOw... | secure-pattern | solidity | 0.8.20 | bridge | True | 2026-08-08T00:01:52.426301+00:00 | 4358 |
| SYNTH-00000232-00071 | proxy_storage_collision | medium | Proxy Storage Collision in insurance contract (variant 232) | tx.origin authentication bypass in insurance | function transferOwnership(address newOwner) public {    ... | function transferOwnership(address newOwner) public onlyO... | secure-pattern | solidity | 0.8.19 | insurance | True | 2026-08-08T00:01:52.624344+00:00 | 232 |
| SYNTH-00006143-00033 | integer_overflow | medium | Integer Overflow in dex contract (variant 6143) | integer_overflow vulnerability in dex contract allows una... | function withdraw() public {     uint256 amount = balance... | function withdraw() public nonReentrant {     uint256 amo... | secure-pattern | solidity | 0.8.22 | dex | True | 2026-08-08T00:01:52.543820+00:00 | 6143 |

## License

This dataset is licensed under [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/).

## Citation

```bibtex
@dataset{defi_risk_2026,
  title        = {DeFi Protocol Risk Metrics},
  author       = {Manteclaw},
  year         = {2026},
  url          = {https://github.com/manteclaw/defi-risk},
  license      = {CC-BY-SA-4.0},
  note         = {Sample dataset. Full version available at https://payhip.com/Manteclaw},
}
```

---
*Dataset curated by [Manteclaw](https://github.com/manteclaw). For inquiries: manteclaw@proton.me*

## More Datasets from Manteclaw

| Dataset | Records | Price | Link |
|---------|---------|-------|------|
| DeFi Protocol Risk Metrics | 1,639 | $49 | [GitHub](https://github.com/manteclaw/defi-risk) |
| Drug Interaction & Pharmacology | 2,231 | $35 | [GitHub](https://github.com/manteclaw/pharmacology) |
| Warehouse Robotics & Logistics | 2,000 | $50 | [GitHub](https://github.com/manteclaw/warehouse-logistics) |
| LLM Safety & Red Teaming | 2,000 | $49 | [GitHub](https://github.com/manteclaw/llm-safety) |
| Crypto Quant Trading Signals | 1,500 | $69 | [GitHub](https://github.com/manteclaw/crypto-quant) |
| Cybersecurity Intrusion Detection | 2,000 | $49 | [GitHub](https://github.com/manteclaw/cybersecurity-intrusion) |

**All datasets available at:** https://payhip.com/Manteclaw
