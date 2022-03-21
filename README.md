## Data Cleaning Documentation Guide
📝 This is a documentation guide to clean our data for maintaining data integrity and quality.

### Mobile numbers

Valid Mobile Number records:

✔️ Country code and length of country code should be valid.
> If country code is 91, then length of the mobile number should be 10.

✔️ Mobile number should start with a valid digit accordingly to respective country code.
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

### Speciality

All valid specialities are added in `specialities` table.

✔️ Specialities data present in other tables should use reference of specialities table.

✔️ If there's no speciality found for any user, `null` should be used.

Invalid speciality records:

❌ A speciality in other tables cannot be `empty` or `0` or `#N/A` or `NA`.

### Email

Valid Email records:

✔️ Always a string and doesn't contain only numbers.

✔️ Always have a domain name
> @xyz.com, @abc.com

✔️ If there's no email found for any user, `null` should be used.

Invalid Email records:

❌ An email record should never be `empty` or `0` or `#N/A` or `NA`.

### First and Last Name

Invalid records:

❌ It can never be `empty` or `0` or `#N/A` or 'NA'


---

✔️ If there's a data dump happening through csv in `universal3` table, the default user status should be `universal`.

✔️ If there's any doctor that has been allocated to a DigiMR, the user status in universal3 table should be `digiMR`.

✔️ Whenever any doctor's call status is logged in `telecaller_member_call_histories`, the `DigiMR_call_status` in universal3 should also be similary updated.

