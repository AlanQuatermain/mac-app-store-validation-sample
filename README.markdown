Mac App Store Validation
========================

The code here is based upon the [documentation released by Apple][docs]. It's been de-obfuscated somewhat, but still has enough to give an idea of how one might take it further. The code in the `asn1` folder was generated using the `asn1c` tool using the definitions on the aforementioned Apple document.

It validates the package receipt and will check the contents of that receipt against its own Info.plist as well as ensuring it has a valid digest for the current machine. In order to protect the Info.plist it also check the app's code signature, since modifications to that file will invalidate the signature.

This implementation isn't guaranteed to be perfect by any means, but it ought to be better than nothing.

[docs]: https://developer.apple.com/devcenter/mac/documents/validating.html
