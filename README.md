[![](https://images.microbadger.com/badges/version/thawsystems/uninno.svg)](https://microbadger.com/images/thawsystems/uninno "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/thawsystems/uninno.svg)](https://microbadger.com/images/thawsystems/uninno "Get your own image badge on microbadger.com")

# Usage

```bash
mbp:~ dave$ docker run -it --rm --network=none -v ~/inno-files:/inno-files thawsystems/uninno
uninno@5ca3746f269c:~$ uninno.pl -h
Usage: extract.pl [-l | -e | -x] [-h] [-d path] setup.exe [file.ext] [file.*] ...
Extracts files from InnoSetup setup.exe installers, loading setup-#.bin slices as appropriate.
You may optionally specify filenames or filename patterns to have only matching files extracted.
Options:
-h  Show this help
-l  List files instead of extracting
-e  Extract files with full (relative) path (default action)
-x  Extract files with stripped path
-d  Specify output path (default: ./app/)
uninno@5ca3746f269c:~$ uninno.pl -e /inno-files/innosetup-5.5.9.exe -d /inno-files/app/
Installer version: 5507
Number of files: 85
2: license.txt App 1540 2016-02-07 00:00:00 C...done
3: ISetup.chm App 359556 2016-04-06 00:00:00 C...done
4: Compil32.exe App 779440 2016-04-06 00:00:00 C...done
...
83: ISPP.dll App 200360 2016-04-06 00:00:00 C...done
84: ISPPBuiltins.iss App 11701 2016-02-07 00:00:00 C...done
mbp:~ dave$ ls ~/inno-files/app/
Compil32.exe			ISPPBuiltins.iss		WizModernSmallImage-IS.bmp	islzma64.exe
Default.isl			ISetup.chm			WizModernSmallImage.bmp		isscint.dll
Examples			Languages			isbunzip.dll			isunzlib.dll
ISCC.exe			Setup.e32			isbzip.dll			iszlib.dll
ISCmplr.dll			SetupLdr.e32			isfaq.htm			license.txt
ISPP.chm			WizModernImage-IS.bmp		islzma.dll			whatsnew.htm
ISPP.dll			WizModernImage.bmp		islzma32.exe
```
