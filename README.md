# Tiptel and Yealink image converter

This tool converts images to .dob files to use as logo in Tiptel and Yealink phones. All images will be converted
to 16 level grayscale. The output is tested on a Tiptel IP 286. The display in these phones support 4 levels of grayscale (white, 2 levels of gray, black).

![Example](http://brixit.nl/sites/brixit.nl/files/tiptel.png)

## Supported phones

- Tiptel IP 286
- Tiptel IP 284
- Tiptel IP 282
- Yealink T10T
- Yealink T12
- Yealink T22
- Yealink T26
- Yealink T28
- Yealink T80

## Dependencies

- python3
- pillow

## Usage

### Command line

```bash
# Convert logo to .dob without resizing
$ DOB/convert.py logo.png logo.dob

# Convert logo to .dob for a Tiptel IP 286
$ DOB/convert.py -p ip286 logo.png logo.dob

# Convert .dob back to a .png
$ DOB/convert.py -r logo.dob logo.png
```

### Package

```python
# Convert logo to .dob for a T28
from DOB import img_to_dob, presets

img_to_dob(infile=open("myimg.png",'rb'), outfile=open("phonelogo.dob",'wb'), preset=presets['t28'])
```

