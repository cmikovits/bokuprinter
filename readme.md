
### Step 1:

- Download the driver/ppd from https://www.konicaminolta.at/de-at/support/download-center
- Search fro C558 and choose bizhub C558 (not bizhub 558 or bizhub 558e)
- download the PPD driver e.g. "PPD driver (110001.0000 MU) for KONICA MINOLTA bizhub Colour Series"

### Step 2:

Add the printer:

- Open https://localhost:631
- add device: https://printer.boku.ac.at/ipp/bokuprint-mono
- use the .ppd file from English/CUPS1.2/KOC759UX.ppd (there is also a file KOC759opn.ppd, no idea which is the correct one, but UX seems to work), the file is called 759, but our model is 558 which is also included there
- change settings to right paper size and to greyscale

Instead of using the generic URL and retrieve prints using card/password, one can send them directly to print by using the URL: https://printer.boku.ac.at/ipp/bokuprint-nr06-color (note that bokuprint-nr06-mono and bokuprint-nr06-color seems to do the same thing)

### Step 3 (optional):

Open cups and edit printers.conf, change line:

```
< https://printer.boku.ac.at/ipp/bokuprint-mono
> https://username:password@printer.boku.ac.at/ipp/bokuprint-mono
```

and add line

```
AuthInfoRequired username,password
```

Without this step user/password should be asked every time.

### Step 4 (optional)

Do the same for bokuprint-color

### Step 5 (optional)

Set Default Options for the printers (only guessed of course):

- Model: C558
- Paper Source Unit: PC-215
- Staple Unit / Finisher: FS-536
