
### Step 1:

Download the driver/ppd from https://www.konicaminolta.at/de/business-solutions/kundensupport/download-center.html

### Step 2:

Add the printer:

- Open https://localhost:631
- add device: https://printer.boku.ac.at/ipp/bokuprint-mono
- change settings to right paper size and to greyscale

### Step 3:

Open cups and edit printers.conf, change line:

```
< https://printer.boku.ac.at/ipp/bokuprint-mono
> https://username:password@printer.boku.ac.at/ipp/bokuprint-mono
```

and add line

```
AuthInfoRequired username,password
```

### Step 4 (optional)

Do the same for bokuprint-color

### Step 5 (optional)

Set Default Options for the printers (only guessed of course):

- Paper Source Unit: PC-215
- Staple Unit: FS-536
