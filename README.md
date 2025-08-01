
# Aurelia Bank AML Analytics Assistant

## Overview

This AI-powered analytics assistant provides natural language access to Aurelia Bank's Anti-Money Laundering (AML) data ecosystem. The system combines advanced SQL querying capabilities with AI-driven analysis to help financial crime analysts investigate suspicious activities, monitor compliance, and generate regulatory insights.

### Key Capabilities

- **Natural Language Querying**: Transform English questions into complex SQL queries across multiple data sources
- **Pattern Analysis**: AI-powered classification and summarization of transaction patterns and behaviors
- **Information Extraction**: Extract structured insights from unstructured data like SAR narratives
- **Cross-Source Analytics**: Automatic correlation of data across MongoDB and PostgreSQL sources
- **Artifact Generation**: Create reusable data tables and insights for ongoing analysis

### Data Domain

The system provides access to Aurelia Bank's comprehensive AML data infrastructure:

- Customer profiles and risk assessments
- Transaction records and suspicious activity flags
- AML case management data
- Sanctions and PEP lists
- Regulatory filings (SARs)

## Getting Started

### Best Practices for Effective Queries

1. **Be Specific with Time Ranges**
   - Good: "Show suspicious transfers from the last 30 days"
   - Avoid: "Show recent suspicious transfers"

2. **Include Relevant Context**
   - Good: "Find high-risk customers with transfers over $10,000 to sanctioned countries"
   - Avoid: "Show me risky customers"

3. **Specify Analysis Requirements**
   - Good: "Analyze transaction patterns of these accounts for structuring behavior"
   - Avoid: "Check if these accounts are suspicious"

### Example Queries by Use Case

#### Transaction Analysis
```
What are the largest cross-border transfers in the last week?
Show me all transactions with structuring indicators from high-risk customers
Find patterns of transfers between related accounts that might indicate layering
```

#### Customer Due Diligence
```
Which customers have had their risk level increased in the last month?
Show me all PEPs with transactions to high-risk jurisdictions
List customers with multiple SAR filings but no enhanced due diligence
```

#### Regulatory Reporting
```
Summarize SAR filings from Q2 2025 by suspicious activity type
Find all cases that need regulatory filing in the next 7 days
Show me customer accounts that recently matched sanctions list entries
```

#### Pattern Detection
```
Analyze these transaction sets for potential smurfing behavior
Find unusual patterns in cross-border transfers to these jurisdictions
Identify accounts showing signs of nested correspondent banking
```

### Working with Results

The assistant can:

1. **Create Data Tables**
   - Request specific columns and filters
   - Sort and group data as needed
   - Export results for further analysis

2. **Generate Summaries**
   - Ask for pattern analysis in the results
   - Request risk categorization
   - Get behavioral summaries

3. **Follow-up Analysis**
   - Reference previous results in new queries
   - Drill down into specific aspects
   - Compare patterns across time periods

### Tips for Complex Analysis

1. **Break Down Complex Questions**
   Instead of:
   "Show me all suspicious patterns in high-risk customer transactions"

   Try:
   1. "List all high-risk customers with transactions above $10,000"
   2. "For these customers, analyze their transaction patterns"
   3. "Classify which patterns indicate potential money laundering"

2. **Iterate on Results**
   - Start with broad queries and narrow down
   - Use results to inform follow-up questions
   - Ask for specific aspects of the data you want to focus on

3. **Specify Output Preferences**
   - Request specific formats for data presentation
   - Ask for particular metrics or calculations
   - Indicate if you need summarized or detailed views

## Technical Details

### Data Sources

#### MongoDB Collections
- **accounts**: Risk profiles, entity types, transaction limits
- **amlCases**: Investigation data, flags, case management
- **sanctions**: Watch lists, programs, jurisdictions

#### PostgreSQL Tables
- **customers**: KYC data, risk ratings, PEP status
- **financialTransfers**: Transaction details, risk indicators
- **sars**: Regulatory filings and narratives

### AI Capabilities

1. **Classification**
   - Categorize transaction patterns
   - Identify suspicious behaviors
   - Risk-rate customer activities

2. **Summarization**
   - Condense transaction patterns
   - Summarize case narratives
   - Extract key risk indicators

3. **Information Extraction**
   - Parse transaction details
   - Extract entities from narratives
   - Identify relationship patterns

## Support

For optimal results:
- Provide clear context for your queries
- Specify time ranges when relevant
- Include threshold values for filtering
- Indicate preferred output formats

---

*Built with advanced AI capabilities for Aurelia Bank's AML compliance initiative*
