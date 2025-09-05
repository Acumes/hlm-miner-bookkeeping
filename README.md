# Allocator Bookkeeping Repository for hlm-miner

## Allocator JSON Link

[hlm-miner Allocator JSON](https://github.com/filecoin-project/Allocator-Registry/blob/main/Allocators/recLhrJ8U6TbIpbwp.json)

## Client Due Diligence

hlm-miner verifies clients and builds trust through a robust process:

- **Application Process**: Clients submit a formal application via a secure portal, including:
  - Legal entity name, registration details, and contact information.
  - Dataset details (type, size, intended use).
  - Proof of data ownership or licensing (e.g., certificates, contracts, consent forms).
- **Verification**: 
  - Third-party KYC services (e.g., Onfido, Jumio) confirm legal entity status and authorized representatives.
  - Background checks via public records and web searches ensure no prior legal or ethical issues.
  - Client details are cross-checked with [datacapstats.io](https://datacapstats.io/) to identify duplicate or suspicious applications.
- **Initial Trust**: 
  - Each client receives a unique ID for tracking in [datacapstats.io](https://datacapstats.io/) and [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) logs.
  - Clients sign agreements committing to compliance with data laws (e.g., GDPR, CCPA, PIPL) and program rules.
  - Initial DataCap allocation is limited to 0.5 PiB, with additional allocations (up to 1 PiB) based on usage and compliance.
- **Sybil Attack Prevention**:
  - Rate limits: One application per legal entity or IP address every 30 days.
  - Deterministic checks: Cross-verify client IDs, wallet addresses, and dataset metadata; require unique dataset fingerprints (e.g., cryptographic hashes).
  - Smart contracts flag matching wallet addresses or dataset hashes.
  - No client receives more than 10% of total DataCap (0.5 PiB initially) until diversity goals (10+ clients) are met.
  - Monthly random audits of 10% of applications detect Sybil patterns.
- **Enterprise/Paying Clients**: Require corporate charters, data acquisition agreements, third-party audits, direct interviews, and financial record verification.
- **Rejection Criteria**: Datasets with unverified ownership, pirated content, or legal violations are rejected.
- **Audit Evidence**: 
  - A secure database stores client applications, KYC results, and compliance records.
  - Anonymized logs are published on [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping).
  - Quarterly audit summaries detail verified clients, rejections, and Sybil attempts, with Governance Team access to a read-only audit portal.

## Data Due Diligence

hlm-miner ensures datasets meet program scope, legal compliance, and client ownership:

- **Program Scope**:
  - Datasets must be public or private, align with network goals (e.g., scientific, archival, media, open-source), and support diversity (5+ dataset types, 10+ clients, ≥4 regions).
  - Clients submit dataset details (type, size, use, source, ownership proof).
  - Datasets are reviewed for diversity (<50% of DataCap per dataset type) and network value; low-quality or irrelevant data is rejected.
- **Legal Compliance**:
  - Required documentation:
    - Public datasets: Open-source licenses (e.g., CC0, MIT) or public domain confirmation.
    - Private datasets: Contracts, consent forms, or data creation records.
    - Sensitive datasets: Compliance with GDPR, CCPA, PIPL, HIPAA.
  - Legal experts review high-risk datasets (e.g., medical, financial).
  - Storage Providers (SPs) are verified for compliant data handling (e.g., encryption).
  - Monthly audits check 10% of active datasets.
- **Ownership Verification**:
  - Proof via source URLs, licenses, data creation records, or third-party audits.
  - Filecoin Content Identifiers (CIDs) verify dataset integrity and ownership.
  - Enterprise clients’ claims are cross-checked with external records.
- **Data Sampling**:
  - Monthly random sampling: 10% of each client’s DataCap (e.g., 0.05 PiB per 0.5 PiB).
  - Quarterly stratified sampling: Covers all dataset types and regions.
  - Cryptographic hashes (e.g., SHA-256) verify dataset type, size, and integrity.
- **Tools**:
  - [Datacapstats.io](https://datacapstats.io/): Tracks deal metadata and verifies client claims.
  - Go-swan-client/Lotus: Validates deal proposals and extracts sample data.
  - Filecoin CIDs: Confirm dataset integrity.
  - Third-party tools (e.g., Chainalysis) verify blockchain or sensitive data.
- **Audit Evidence**:
  - A secure database stores dataset details, ownership proofs, and sampling results.
  - Anonymized audit trails are published on [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping).
  - Quarterly reports detail verified datasets, sampling results, and compliance issues, with Governance Team access to a secure audit portal.
- **Non-Compliance**: Datasets with unverified ownership or legal violations are rejected; repeated deal mismatches lead to DataCap suspension.

## Short Description of Pathway for Clients

hlm-miner offers a secure, transparent pathway for DataCap allocation, prioritizing legal compliance, dataset diversity, and high retrievability. With thorough KYC, ownership verification, and ongoing audits, we ensure trust and compliance with global regulations (e.g., GDPR, CCPA). Supporting diverse datasets (scientific, media, open-source) across multiple regions, hlm-miner is perfect for clients seeking reliable, decentralized storage on Filecoin.

## Contact Info

- **Email**: [finance@grandhelmsman.com](mailto:finance@grandhelmsman.com)
- **Slack**: acumes

## Detailed Allocator Policies, Procedures, and Requirements

Published on [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping), hlm-miner’s policies outline:

- **Client Due Diligence**: KYC, ownership verification, Sybil prevention via rate limits, deterministic checks, and audits.
- **Data Due Diligence**: Scope verification, legal compliance, ownership checks, monthly random and quarterly stratified sampling using [datacapstats.io](https://datacapstats.io/), go-swan-client, and CIDs.
- **Reporting**: Bi-monthly RSR, monthly utilization, and quarterly diversity reports with compliance details.
- **Consequences**: DataCap suspension for non-compliance.
- **Updates**: Policies are updated based on Governance feedback for transparency.

## Risk Mitigation Strategies

hlm-miner safeguards its pathway through:

- **Operational Security (OpSec)**: Secure application portal, encrypted records, third-party KYC.
- **User Agreements**: Signed commitments to data laws and program rules.
- **Throttling/Alerts**: Smart contracts flag duplicate applications; rate limits restrict submissions to one per 30 days per entity/IP.
- **Audits**: Monthly 10% random audits and quarterly comprehensive reviews detect abuse or Sybil attempts.
- **Reputation Scoring**: Prioritizes clients with verified track records.
- **Consequences**: Non-compliant clients face DataCap suspension.

## Dispute Resolution

- **Internal Disputes**: Clients submit concerns to [finance@grandhelmsman.com](mailto:finance@grandhelmsman.com). The compliance team reviews within one week, using [datacapstats.io](https://datacapstats.io/) data. Non-compliant clients receive warnings; unresolved issues lead to DataCap suspension.
- **External Disputes**: For conflicts with other allocators or Governance, hlm-miner provides audit trails (client IDs, dataset metadata, compliance records) via [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) and a secure audit portal. Disputes are resolved within two weeks, with escalation to Governance if needed.
- **Transparency**: All disputes and resolutions are logged on [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping).

## Compliance Audit Check

hlm-miner ensures compliance through:

- **Client Verification**: KYC, ownership, and legal documentation checks before allocation.
- **SP Compliance**: SPs’ data handling protocols (e.g., encryption) align with regional laws.
- **Data Due Diligence**: Monthly 10% sampling and quarterly audits verify scope, legality, and ownership using [datacapstats.io](https://datacapstats.io/) and Filecoin tools.
- **Reporting**: Bi-monthly RSR, monthly utilization, and quarterly diversity reports on [GitHub](https://github.com/Acumes/hlm-miner-bookkeeping) include compliance summaries.
- **Audits**: Monthly 10% random audits of clients/SPs, with Governance access to encrypted records via a secure portal.
- **Consequences**: Non-compliant clients/SPs face DataCap suspension until issues are resolved.
