# Change Log

## [1.1.0] - 2015-11-08
### Added
- Option for preparing a pre-downloaded and/or pre-indexed reference.  This will skip the download and clean any applicable portion of the reference/index
- Index version compatibility system.  Will ensure at alignment time the index is compatible with current software version
- Additional runtime status reporting, especially in areas where processing can take a significant amount of time (ORF detection, index preparation, index loading, etc)

### Changed
- UniRef50 option to UniRef90 (in accordance with empirical testing)
- A few minor description changes

## [1.0.3] - 2015-09-30
### Added
- UniRef50 as one of the preparation/download options

## [1.0.2] - 2015-09-29
### Added
- UniProt reporting now properly parses header styles of both SwissProt/TrEMBL and UniRef

## [1.0.1] - 2015-09-28
### Changed
- Default alignment threshold score from 30 to 20 (in accordance with empirical testing)

## [1.0.0] - 2015-08-11
### Added
- Minimum ORF length filtering
- Related options (Constant minimum length, percentage minimum length, adjustment for smaller read lengths)

### Fixed
- Translating edges of detected ORFs (previously were truncated)

### Changed
- A few minor description changes

## [0.2.1] - 2015-08-06
### Fixed
- Alignment stats shown at completion now properly account for supplementary alignments

## [0.2.0] - 2015-08-02
### Added
- Changelog (history starts here)
- Option to redirect all output (reports and SAM) to file prefix and not stdout
- Print basic alignment stats upon completion
- Show count percentages in UniProt report (both full and basic)

### Fixed
- Option for minimum ORF length temporarily taken out (to be added in version 0.3.0)
- Typo in Uniprot report
- A few minor compilation warnings

### Changed
- Option for minimum ORF length now set to argument "-l".  "-o" used for output file prefix
- Report type "-u" option starts at 0 now, with 1 being default (full report)
- Reorganized usage message to group protein/ORF related options into their own section (to be used more in future development)

### Known Issues
- Alignment stats shown at completion do not properly subtract out supplementary alignments, so total and percentages are slightly off from flagstat output
- File output currently requires prefix to be given, will not autogenerate name if one isn't specified
