##Titlecase

This is a production-quality package made for cleaning and formatting book titles, but it can be used for titlecasing anything. It is far better than any of the other titlecasing packages available at the time of writing.

Please note that some assumptions are made by this package that would make it unsuitable for certain purposes. Specifically the package is made for book titles from the pre-Internet era and so it does not, in its current state, support domain names. For example: `look at this cool thing i found on google.com` would be changed to `Look at This Cool Thing I Found on Google. Com`. I can add support for domain names on request.

##Features

* Supports multiple languages: English, French, German, Italian, Spanish, Portuguese & Generic
* Supports contractions
* Supports initials, titles and abbreviations
* Supports Roman numerals, with exceptions for real words that look like roman numerals
* Supports hypenatation and slashes
* Repairs grammatical errors in English
* Decodes all HTML entities
* Fully UTF8 compliant
* Written for speed and efficiency - no regular expressions, minimal looping

##Installation

    go get github.com/AlasdairF/Titlecase

##Usage

    unformatted := ` this is a title by a. forsythe, made to demonstrate a example. WRITTEN ON 5TH DECEMBER, 2014.`
    formatted := titlecase.Format(unformatted, titlecase.English)
    // This Is a Title by A. Forsythe, Made to Demonstrate an Example; Written on 5th December, 2014
    
    unformatted = `   della corte d'appello di roma nell'anno mdccclxxxi `
    formatted = titlecase.Format(unformatted, titlecase.Italian)
    // Della Corte d'Appello di Roma nell'Anno MDCCCLXXXI
