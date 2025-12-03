# NOTE: THIS IS FOR INFORMATIONAL AND SUPPLEMENTAL PURPOSES ONLY
It is now an official feature in DT4 Settings > Files > Import > Dates: ✅ Use content creation & modification dates
(and was introduced as a Hidden Preference in DT3 - see below)

# DT3-pdf-metadate
AppleScript to take PDF metadata and update its entry in DEVONThink 3. Sometimes it is imported with only the Finder metadata.

To prevent this on import, you need to use the hidden preference UsePDFDocumentDates by running this in the terminal:
`defaults write com.devon-technologies.think3 UsePDFDocumentDates -bool TRUE`
but that doesn't always affect already imported PDFs.

## Install
This AppleScript relies on exiftool. Best option is to install via homebrew:
`brew install exiftool`

This script assumes it is installed in `/opt/homebrew/bin/exiftool`. If you keep homebrew in a different default directory, you will need to change that in the script.

Drop the script in `~/Library/Application Scripts/com.devon-technologies.think3/Menu` or a subdirectory of that.

## Usage
Select the PDFs you want to scan and change in your DEVONThink library and select the script from the AppleScript menu (represented by an icon).

## Known Issues
**exiftool Path**: Working on better detection of `which exiftool`.
