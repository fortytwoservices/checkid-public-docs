# Custom Password Blacklist

CheckID supports custom password blacklists, allowing organisations to prevent the use of weak, predictable, or organisation-specific passwords during password creation or reset.

This capability aligns with modern identity security practices and complements global banned password controls.

## How It Works

When enabled, CheckID validates new or changed passwords against:

- The global banned password list  
- The organisation’s custom banned password list (if configured)

If a password matches a banned term, the password is rejected and the user must choose a different password.

### Normalisation and Matching Logic

To prevent simple bypass techniques, CheckID applies password normalisation before validation. This includes:

- Converting the password to lowercase  
- Applying common character substitutions (e.g. `@ → a`, `$ → s`, `0 → o`)

This ensures that trivial variations are detected when the base term (e.g. `password`) is banned:

- `Password1`
- `P@ssw0rd`
- `Pa$$word`
- `passw0rd123`

## Configuration and Submission of List

### List Creation

To configure a custom banned password list:

1. The customer prepares a plain text file containing banned terms  
2. One term per line

#### File Format Requirements

- File type: `.txt`  
- Encoding: UTF-8  
- One term per line  
- No special formatting  
- Maximum size: defined per contract or environment limits  

#### Example File

```txt
checkid
companyname
helsinki
internaltool
projectx
```

### Submission of List

1. The file is sent securely to the CheckID team  
2. The list is imported into the customer’s CheckID instance  
3. Confirmation is provided once activation is complete  

## Important Notes

- Changes require submission of an updated file.
- Applies only to password creation and reset events  
- Does not retroactively invalidate existing passwords  
- Customers should focus on organisation-specific terms (brand names, internal systems, locations, abbreviations)  
- No need to include variations such as `Company123` - normalisation handles common substitutions and patterns
