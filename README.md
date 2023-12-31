# MiniRelay

## Brief

Minimal, half TH35 (Din rail) module sized (9 mm x 49 mm) relay module. It can fit on a Din rail in places, in which the others are too big. 

![connections](images/view.png)

![picture](images/picture.jpg)

## Usage and description

The dry contact of the [1721081-2](https://www.te.com/commerce/DocumentDelivery/DDEController?Action=showdoc&DocId=Data+Sheet%7FPCJ_series_relay_data_sheet_E%7F6A18%7Fpdf%7FEnglish%7FENG_DS_PCJ_series_relay_data_sheet_E_6A18.pdf%7F1-1721081-2) relay can withstand ~3 A and can switch 250 VAC. The input/ driving/ supply voltage can in theory be as high as just bellow 40 V (due to used series diode), but in practice the [MCP1799T-3302H/TT](https://www.microchip.com/en-us/product/MCP1799) LDO will start to overheat on input voltages equal or higher to ~17 V. To reach better input voltages (i.e., 24 V), the LDO has to be replaced with a one with larger casing, or the D2 LED can be desoldered, to reduce the LDO output current. A series resistor can also be added to the coil (the practical pull up voltage for this relay is still lower than 3.3 V).

The Input voltage can be as low as 5 V for the module to operate. 

The module consists on reverse polarity protection on the +/- pins (up to 40 V). 

Since the module uses 49 mm spread castellated holes, many popular din rail holders from Thingiverse designed for the raspberry Pi can be of use (as [this one](https://www.thingiverse.com/thing:3369750/files) from the picture).

