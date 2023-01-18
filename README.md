# LKT MIME

A practical lib for check and detect MIME types.

## Detect MIME by file extension

```php
use Lkt\MIME;

// Generic checker
MIME::getByExtension('jpeg');

// Image specific checker
MIME::getImageByExtension('jpg');

// Video specific checker
MIME::getVideoByExtension('mp4');

// Office specific checker. Includes Open/Microsoft Office formats, PDF, CSV, TXT, ABW
MIME::getOfficeByExtension('pdf');

// Archive specific checker. Includes ZIP, 7Z, RAR, BZ, BZ2, TAR, ARC
MIME::getArchiveByExtension('pdf');

// Audio specific checker. Includes MP3, OPUS, OGA, AAC, WEBA, CDA, MID, MIDI, WAV
MIME::getAudioByExtension('oga');

// Programming languages specific checker
MIME::getCodeByExtension('php');

// Programming languages specific checker
MIME::getEbookByExtension('epub');

// Font specific checker
MIME::getFontByExtension('otf');
```

## Check if a MIME represents certain type of content

```php
use Lkt\MIME;

// Check if MIME represents an image
MIME::isImage('png');

// Check if MIME represents audio
MIME::isAudio('mp3');

// Check if MIME represents video
MIME::isVideo('mp4');

// Check if MIME represents a font
MIME::isFont('ttf');
```

## Access to MIME constants

You can use any of this MIME with the `Const` column constant (see table below):

```php
use Lkt\MIME;

MIME::PDF;
MIME::HTML;
```

## Supported MIME

Any extension not included in the following list will return `application/octet-stream`.

| Const                     | Extension | MIME                                                                      |
|---------------------------|-----------|---------------------------------------------------------------------------|
| ::JSON                    | json      | application/json                                                          |
| ::JSONLD                  | jsonld    | application/ld+json                                                       |
| ::OCTET_STREAM            | bin       | application/octet-stream                                                  |
| ::ABIWORD                 | abw       | application/x-abiword                                                     |
| ::ARCHIVE_DOCUMENT        | arc       | application/x-freearc                                                     |
| ::KINDLE_EBOOK            | azw       | application/vnd.amazon.ebook                                              |
| ::BZIP                    | bz        | application/x-bzip                                                        |
| ::BZIP2                   | bz2       | application/x-bzip2                                                       |
| ::CDA                     | cda       | application/x-cdf                                                         |
| ::CSH                     | csh       | application/x-csh                                                         |
| ::MS_DOC                  | doc       | application/msword                                                        |
| ::MS_DOCX                 | docx      | application/vnd.openxmlformats-officedocument.wordprocessingml.document   |
| ::MS_EOT                  | eot       | application/vnd.ms-fontobject                                             |
| ::EPUB                    | epub      | application/epub+zip                                                      |
| ::GZIP                    | gzip      | application/gzip                                                          |
| ::MS_ICO                  | ico       | image/vnd.microsoft.icon                                                  |
| ::JAR                     | jar       | image/java-archive                                                        |
| ::APPLE_INSTALLER_PACKAGE | mpkg      | application/vnd.apple.installer+xml                                       |
| ::ODP                     | odp       | application/vnd.oasis.opendocument.presentation                           |
| ::ODS                     | ods       | application/vnd.oasis.opendocument.spreadsheet                            |
| ::ODT                     | odt       | application/vnd.oasis.opendocument.text                                   |
| ::PDF                     | pdf       | application/pdf                                                           |
| ::PHP                     | php       | application/x-httpd-php                                                   |
| ::PPT                     | ppt       | application/vnd.ms-powerpoint                                             |
| ::PPTX                    | pptx      | application/vnd.openxmlformats-officedocument.presentationml.presentation |
| ::RAR                     | rar       | application/vnd.rar                                                       |
| ::RTF                     | rtf       | application/rtf                                                           |
| ::SH                      | sh        | application/x-sh                                                          |
| ::TAR                     | tar       | application/x-tar                                                         |
| ::MS_VISIO                | vsd       | application/vnd.visio                                                     |
| ::XHTML                   | xhtml     | application/xhtml+xml                                                     |
| ::XLS                     | xls       | application/vnd.ms-excel                                                  |
| ::XLSX                    | xlsx      | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet         |
| ::XML                     | xml       | application/xml                                                           |
| ::ZIP                     | zip       | application/zip                                                           |
| ::SEVEN_ZIP               | 7z        | application/x-7z-compressed                                               |
| ::AAC                     | aac       | audio/aac                                                                 |
| ::MID                     | mid       | audio/midi                                                                |
| ::MIDI                    | midi      | audio/x-midi                                                              |
| ::MP3                     | mp3       | audio/mpeg                                                                |
| ::OGA                     | oga       | audio/ogg                                                                 |
| ::OPUS                    | opus      | audio/opus                                                                |
| ::WAV                     | wav       | audio/wav                                                                 |
| ::WEBA                    | weba      | audio/webm                                                                |
| ::OTF                     | otf       | font/otf                                                                  |
| ::TTF                     | ttf       | font/ttf                                                                  |
| ::WOFF                    | woff      | font/woff                                                                 |
| ::WOFF2                   | woff2     | font/woff2                                                                |
| ::GIF                     | gif       | image/gif                                                                 |
| ::PNG                     | png       | image/png                                                                 |
| ::JPEG                    | jpg, jpeg | image/jpeg                                                                |
| ::SVG                     | svg       | image/svg+xml                                                             |
| ::WEBP                    | webp      | image/webp                                                                |
| ::AVIF                    | avif      | image/avif                                                                |
| ::BMP                     | bmp       | image/bmp                                                                 |
| ::TIFF                    | tif, tiff | image/tiff                                                                |
| ::MS_ICO                  | ico       | image/vnd.microsoft.icon                                                  |
| ::CSS                     | css       | text/css                                                                  |
| ::HTML                    | html, htm | text/html                                                                 |
| ::PLAIN                   | txt       | text/plain                                                                |
| ::CSV                     | csv       | text/csv                                                                  |
| ::ICS                     | ics       | text/calendar                                                             |
| ::JS                      | js, mjs   | text/javascript                                                           |
| ::AVI                     | avi       | video/x-msvideo                                                           |
| ::MP4                     | mp4       | video/mp4                                                                 |
| ::MPEG                    | mpeg      | video/mpeg                                                                |
| ::OGG                     | ogg       | video/ogg                                                                 |
| ::MPEG_TS                 | ts        | video/mp2t                                                                |
| ::WEBM                    | webm      | video/webm                                                                |