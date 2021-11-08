# Philips PE1542 Modification

This project provides you a 3D model and video with instructions on howto replace the analog meters with digital meters on a Philips PE1542 bench power supply.

The video is avaliable by clicking on the image below.

[![VIDEO](https://img.youtube.com/vi/GQAOcTNk6Aw/0.jpg)](https://www.youtube.com/embed/GQAOcTNk6Aw)

In the video I have used meters with 3 decmials precision but, the sampling rate on these were increadbly slow. I later switched to meters with 2 decmicals precision which were faster. I suspect that these meters contain intergrating ADCs, hence the slow updating times.

Click [here](https://www.ebay.com/itm/114450600499?_trkparms=ispr%3D1&hash=item1aa5c99233:g:H5sAAOSwFT9ffec9&amdata=enc%3AAQAGAAAC0PYe5NmHp%252B2JMhMi7yxGiTJkPrKr5t53CooMSQt2orsSR84A%252FGMxXIqJzFmDq6lDLqUTR3Bl74YVPAzSZgklE7A4E7AafKXuqp5a6Nd8SiAN00fvunW16DeLbMUQN2qul6EoHi%252B%252Bt7qApaOfyBFxUCJLqMMCxBYSup1%252BcuwBOkjAL9nYiLIs0vtt%252B6VI21%252BC%252F37dQEO9wHusG6TuyFzwqdnQUST%252FmsduTEjontwFJ4UM4nT0vx49mEb%252FwYXxf7QZIl1mX9QrMmSryWw1D0w2GRvI70cyYweEGdHCIHEHoBkTrA0rusmiEIuDlfQZGT6%252Fd3PcgBDTEgEjSoK8pHdr6SSF8eAxbLqFHibaLOCjcL220E5c%252FTC%252BcF4s%252BnzK2iYVNSd7OErDWTlBXFqnTSvZEdAstSwEL2f9JVv%252FnyuUQt8%252BjDJUj5P49pzn8gA4xGiGHqdT%252BCCIZbGSF0YA290wjOF3L%252FQpRQ%252Fk4VZHvo81HNkp4UgSKN2S7Vfm%252BcTz3FhSiCmPTuJg1PiPEsNcNr4uTT0wIaoIDLr22haHb9i5UCqDOfzeoon9nIzbMtnSmcO8Ez9X6VtZNR%252BRcqijGwjzu9pfadEb%252BJAhkfA05cXn75IvRsZhekc0Lj11zd3N9Hym3Dnqso8%252FBqTFDcHq234R2pafUbhKoNu1jPdnpbbJdJRz9f3zeeB6TdhhOX17OQjecESP7d6HwRMP7lidA48OqfqC6r2V0s%252BMnmNNdIRn%252B3kS0iwNnV42TNg15es3MJr36bh94%252BHSWFGjc%252F4o%252BGng%252FuxS45IB1H%252B6adGcX2mKAsY50goUns8cHRqd3%252B9arSwqwTh3LWY%252F%252FvCJIYPJ%252B6BE3K%252FO3PAKH1BGZE80LFIwzsV17C%252BswOankD7PvO24uSTfIGnYHf4FqP5Bmaq75B9P3IlHE1jQHSk%252BtWaqsnLRMO1LZqLxUegxWp%252BZxXVysHSOmg%253D%253D%7Cclp%3A2334524%7Ctkp%3ABFBMipq295Zf) to view/purchse the meters on eBay.

The mains transformer has 3 ouputs. 2 of them are outputting around 30 [Vpp], the last one is at 12[Vpp].

The maximum operating voltage for the replacment meters are 20 [V], this means that for 2 ouputs with 30[Vpp] some voltage drop is needed. This was acheived by implementing a [Zener Voltage Regulator](https://www.electronics-tutorials.ws/diode/diode_7.html) circuit after the rectifing capacitor on the two outputs.

The project contains the following folders
1. **3D Model:** An STL file which contains a mount that will fit into the space where the origianl meters were placed.
2. **Images**: Pictures showcasing the final results of the modification (images might be a bit big to view via GitHub, best to download them)

Note: 
1. The holes in the 3D model are designed for M2 screws.
2. No mechanical changes are required other than removing the original meters.
3. Zener Voltage Regulators must be placed on the smoothing Capacitors with 30 [Vpp] (as seen in the video).
4. The Ground tracks going to the output connectors must be cut and the shunt resistor wires need to be placed inbetween this cut (as seen in the video).
5. The Volt/Current switch will now be inactive, in the furutre I plan to change this to a on/off button for each output.

Here is the final results

<img src="https://github.com/Skitter-JP/Philips_PE1542_Modification/blob/main/Images/Final_result_3_decimals.JPG" width=40% height=40%>

