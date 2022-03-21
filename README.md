## Data Cleaning Documentation Guide
📝 This is a documentation guide to clean our data for maintaining data integrity and quality.

### Mobile numbers

Valid Mobile Number records:

✔️ Country code and length of country code should be valid
> If country code is 91, then length of the mobile number should be 10.

✔️ Mobile number should start with a valid digit accordingly to respective country code
> If country code is 91 and length of mobile number is 10, the starting digit should be between 6 and 9.

✔️ If there's no mobile number for any user, then the value would be `null`.

Invalid Mobile number records:

❌ It cannot be exponential
> 2.14E+11

❌ It cannot be `0` or `empty`.

❌ It cannot have whitespaces or strings.
> 999998 8888 \
> 99999a9999

❌ If there's a mobile number, country_code should never be `null` or `empty` or `0`.

❌ If there's a country code and there's no mobile_number, then country_code should be `null`.

❌ There should be no special characters in mobile_numbers.
> +, E, -, ,, ..
