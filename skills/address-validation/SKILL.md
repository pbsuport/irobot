---
name: address-validation
description: Validate and verify postal addresses for accuracy and deliverability. Use when: (1) user asks to "validate", "verify", or "check" an address, (2) user needs to standardize or format an address, (3) user wants to confirm if an address exists or is deliverable, (4) user says "address validation" or "verify this address". Supports multiple countries and address formats.
---

# Address Validation

Validate, standardize, and verify postal addresses for accuracy and deliverability.

## Workflow

1. **Parse the address** - Extract components (street, city, state, postal code, country)
2. **Standardize format** - Apply postal standards for the country
3. **Validate components** - Check each part against known formats
4. **Verify existence** - Use available tools to confirm address exists
5. **Return results** - Provide validation status and suggestions

## Validation Levels

### Level 1: Format Validation
Check if address follows standard format:
- Required fields present (street, city, postal code)
- Postal code matches country format
- State/province is valid for country

### Level 2: Component Validation
Verify individual components:
- Street number is numeric
- Postal code format matches region
- City exists in state/province
- Country code is valid (ISO 3166)

### Level 3: Deliverability Check
Confirm address is real and deliverable:
- Use postal service APIs if available
- Cross-reference with mapping services
- Check for known address databases

## Address Parsing

### US Address Format
```
[Street Number] [Street Name] [Street Type] [Unit]
[City], [State] [ZIP Code]
[Country]

Example:
123 Main Street, Apt 4B
New York, NY 10001
USA
```

### Canadian Address Format
```
[Street Number] [Street Name] [Street Type] [Unit]
[City], [Province] [Postal Code]
[Country]

Example:
456 Maple Avenue, Suite 200
Toronto, ON M5V 2H1
Canada
```

### UK Address Format
```
[Building/Unit]
[Street Number] [Street Name]
[City]
[Postal Code]
[Country]

Example:
Flat 3
25 Oxford Street
London
W1D 2DW
United Kingdom
```

## Postal Code Formats

| Country | Format | Example |
|---------|--------|---------|
| US | #####  or #####-#### | 10001, 10001-1234 |
| Canada | A#A #A# | M5V 2H1 |
| UK | AA## #AA or A#A #AA | W1D 2DW, M1 1AA |
| Australia | #### | 2000 |
| Germany | ##### | 10115 |
| France | ##### | 75001 |

## Validation Checks

### Required Fields
- [ ] Street address present
- [ ] City present
- [ ] Postal/ZIP code present
- [ ] Country identifiable

### Format Checks
- [ ] Postal code matches country format
- [ ] State/province valid for country
- [ ] No invalid characters
- [ ] Reasonable length

### Logic Checks
- [ ] Postal code matches city/region
- [ ] Street type is valid (St, Ave, Blvd, etc.)
- [ ] Unit number format is valid

## Output Format

```markdown
## 📍 Address Validation Result

**Input Address:**
[Original address as provided]

**Standardized Address:**
[Formatted according to postal standards]

**Validation Status:** ✅ Valid | ⚠️ Needs Review | ❌ Invalid

### Component Breakdown
| Component | Value | Status |
|-----------|-------|--------|
| Street | 123 Main St | ✅ Valid |
| City | New York | ✅ Valid |
| State | NY | ✅ Valid |
| Postal Code | 10001 | ✅ Valid |
| Country | USA | ✅ Valid |

### Issues Found
- [List any issues or warnings]

### Suggestions
- [Corrections or improvements if needed]
```

## Common Issues

### Fixable Issues
- Missing apartment/unit number → Prompt for clarification
- Misspelled city/street → Suggest correction
- Wrong postal code format → Reformat
- Abbreviated vs full state name → Standardize

### Critical Issues
- Postal code doesn't match city → Flag for review
- Non-existent street → Cannot validate
- Incomplete address → Request missing info

## Tools Integration

If web_fetch/web_search available:
- Cross-reference with Google Maps
- Check USPS for US addresses
- Verify with Canada Post for Canadian addresses

If no external tools:
- Perform format validation only
- Apply regex patterns for postal codes
- Check against known city/state combinations

## Parameters

- **Country**: auto-detect | specific country code
- **Strictness**: lenient | standard | strict
- **Output**: summary | detailed | json
