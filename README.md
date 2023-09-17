# Tutorial Converting and Downloading RAW file from Himawari 8/9 into NC files
## Overview
These scripts are originally created by Xin Zhang for downloading gridded-processed data of Himawari-8 Satellite. However, it has been years ago, and there are some changes, especially for the sample programs's version. So, I actually just give an update for the sample programs. This scripts can be run using any codes editor, but this time I will use [Google Colaboratory](https://colab.research.google.com/) as my script editor.

## Requirements
- [NetCDF Operators (NCO)](http://nco.sourceforge.net/)
- [Climate Data Operators (CDO)](https://code.mpimet.mpg.de/projects/cdo/wiki/Cdo)
- [ftplib](https://docs.python.org/3/library/ftplib.html)
- [xarray](https://github.com/pydata/xarray)
- [tqdm](https://github.com/tqdm/tqdm)

## Usage
- Download or clone the repository first
```
git clone git@github.com:jasminefadhila/TutorialConvertH89.git
```
Check the help information
```
python count2tbb.py --help
Usage: count2tbb.py [OPTIONS]

  Himawari-8 gridded format shell script. v1.00 (201605)
      Converted to .py and modified by [Xin Zhang] (20181225)
  Fuctions:
      Download, count2tbb, convert and merge to daily nc files
  Contact:
      xinzhang1215@gmail.com

Options:
  -r, --req_path TEXT   Directory where you put count2tbb_v101.  [default:
                        ./count2tbb_v101]
  -s, --save_path TEXT  Directory where you want to save files.  [default:
                        ./data]
  -sd, --sdate TEXT     Beginning date of downloaded files
                          YYYY-MM-DD-hh:mm
  -ed, --edate TEXT     Ending date of downloaded files
                          YYYY-MM-DD-hh:mm
  -ts, --tstep INTEGER  Time step (min) between files  [default: 720]
  -c, --chn TEXT        Channel name in Capital.
                          EXT, VIS ,SIR or TIR
                        [default: TIR]
  -n, --num TEXT        Band number according to channel
                        -----------------------------------
                        Reference:
                        -----------------------------------
                        [EXT] 01:Band03
                        -----------------------------------
                        [VIS] 01:Band01
                        02:Band02 03:Band04
                        -----------------------------------
                        [SIR] 01:Band05
                        02:Band06
                        -----------------------------------
                        [TIR]
                        01:Band13 02:Band14 03:Band15 04:Band16 05:Band07
                        06:Band08 07:Band09 08:Band10 09:Band11 10:Band12
                        -----------------------------------  [default: 2]
  -c, --compiler TEXT   Compiler: gfortran, ifort  [default: gfortran]
  -d, --debug INTEGER   Debug level  [default: 0]
  --help                Show this message and exit.
```
## Google Colaboratory's Version

```
!pip install -q condacolab
import condacolab
condacolab.install()
```

## Reference
Click this [link](https://github.com/zxdawn/Himawari-8-gridded/tree/master) to see the original scripts. Big thanks for you!
