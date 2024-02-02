The aim of the `python3` library is to open, modify and write `Biometric Information files` based on the standard proposed by the NIST (for short: NIST format).
The main development is done against `traditionnal` NIST files; the creation of the parser for `XML` files will be done in a second time.

The development and maintenance have been made by Marco De Donno, School of Criminal Justice, Faculty of Law, Criminal Justice and Public Administration, University of Lausanne, Switzerland. This library is not related to the National Institute of Standards and Technology.

This version is a port of the legacy `python2` implementation (https://github.com/mdedonno1337/NIST).

The standard propose the following type of biometric data:

| Type    | Description                                             |
| ------- | ------------------------------------------------------- |
| Type-01 | Transaction information                                 |
| Type-02 | User-defined descriptive text                           |
| Type-03 | (Deprecated)                                            |
| Type-04 | High-resolution grayscale fingerprint image             |
| Type-05 | (Deprecated)                                            |
| Type-06 | (Deprecated)                                            |
| Type-07 | User-defined image                                      |
| Type-08 | Signature image                                         |
| Type-09 | Minutiae data                                           |
| Type-10 | Photographic body part imagery (including face and SMT) |
| Type-11 | Forensic and investigatory voice data                   |
| Type-12 | Forensic dental and oral data                           |
| Type-13 | Variable-resolution latent friction ridge image         |
| Type-14 | Variable-resolution fingerprint image                   |
| Type-15 | Variable-resolution palm print image                    |
| Type-16 | User-defined variable-resolution testing image          |
| Type-17 | Iris image                                              |
| Type-18 | DNA data                                                |
| Type-19 | Variable-resolution plantar image                       |
| Type-20 | Source representation                                   |
| Type-21 | Associated context                                      |
| Type-22 | Non-photographic imagery                                |
| Type-98 | Information assurance                                   |
| Type-99 | CBEFF biometric data record                             |

The Type-23 to Type-97 are reserved for future use.

The aim of this library is to be compatible (read and write) with the standard is used correctly (compatibility tested with "BioCTS for ANSI /NIST-ITL v2") and the Sample Data provided by the NIST.
At the moment, the records Type-07 (User-defined) and Type-08 (Signature image) are not parsed; the rest of the NIST file is still loaded and parsed.
As such, when using "output" functions (i.e. print to screen and write to file), the `clean()` function will remove those records.

Some functions are added to simplify some operation, especially regarding the fingerprint processing (extraction of image, annotation of minutiae on the image, ...).

# References

Data Format for the Interchange of Fingerprint, Facial & Other Biometric Information, NIST Special Publication 500-290 Rev1 (2013), https://www.nist.gov/itl/iad/image-group/ansinist-itl-standard-references

