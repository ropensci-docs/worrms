# worrms

World Register of Marine Species Client

## Fail behavior

The WoRMS REST API doesn't have sophisticated error messaging, so most
errors will result in a `(204) - No Content` or in `(400) - Bad Request`

Because WoRMS doesn't do comprehensive error reporting, we do a fair
amount of checking user inputs to help prevent errors that will be
meaningless to the user. Let us know if we can improve on this.

## Author

Scott Chamberlain <myrmecocystus@gmail.com>
