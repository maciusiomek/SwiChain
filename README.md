<center><h1>SwiChain</h1></center>
<h3>A little macropad that you can use with Bluetooth!</h3> 

The purpose of this project was to make a macropad that I can program however I want that and would look cool. I always wanted to have something like Stream Deck to have easier control over the music, muting my microphone or playing sound effects on calls with my friends, so I've made this!<br>
<center><img width="400" height="auto" alt="a" src="https://github.com/user-attachments/assets/6bb41995-056b-4a12-8ce3-0617c36ccc1f" /></center>
<hr>
<h2>Connections and pricing.</h2>
The project is based around Seeed XIAO nRF52840 running ZMK firmware. The buttons and EC11 are connected to the xiao and programmed like in the table bellow:<br><br>


<table>
  <tr>
    <th><center>EC11</center></th>
    <th><center>SW1</center></th>
    <th><center>SW2</center></th>
    <th><center>SW3</center></th>
  </tr>
  <tr>
    <td><center>SW - D7<br>A - D8<br>B - D9</center></td>
    <td><center>D0</center></td>
    <td><center>D1</center></td>
    <td><center>D2</center></td>
  </tr>
  <tr>
    <td><center>Press - Pairing<br>Left/Right - Volume</center></td>
    <td><center>Previous</center></td>
    <td><center>Pause/Play</center></td>
    <td><center>Next</center></td>
  </tr>
  <tr>
    <th><center>SW4</center></th>
    <th><center>SW5</center></th>
    <th><center>SW6</center></th>
    <th><center>SW7</center></th>
  </tr>
  <tr>
    <td><center>D3</center></td>
    <td><center>D4</center></td>
    <td><center>D5</center></td>
    <td><center>D6</center></td>
  </tr>
  <tr>
    <td><center>F23</center></td>
    <td><center>Win+3</center></td>
    <td><center>Win+4</center></td>
    <td><center>Win+5</center></td>
  </tr>
</table>
Underglow - WS2812 LEDs are connected to D10, looking from the top the first one connected is in the top-right corner and the chain is going clockwise. <br><br>
To modify the function of each button (or EC11!) go to <a href="https://github.com/maciusiomek/zmk-config-maciusiomek">my other repository</a>, fork it and modify config/swichain.keymap however you want! You can find the list of keycodes you can use <a href="https://zmk.dev/docs/keymaps/list-of-keycodes">here</a>! <br><br>
<table>
  <tr>
    <th>Quantity</th>
    <th>Part</th>
    <th>For what?</th>
    <th>LCSC ID/Where to buy</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>1</td>
    <td>PCB</td>
    <td>Well, it's a pcb! It's the foundation of the macropad!</td>
    <td>Buy a pcb from JLCPCB or PCBWay (download Gerber.zip!)</td>
    <td>$7.80 for 5 on JLCPCB's JLCONE app</td>
  </tr>
  <tr>
    <td>1</td>
    <td>18650 holder</td>
    <td>To hold the 18650 on the back!</td>
    <td>C49118399</td>
    <td>$0.20</td>
  </tr>
  <tr>
    <td>7</td>
    <td>MX type switches</td>
    <td>SWITCHESSS!!!!</td>
    <td>Just buy some from aliexpress or smth</td>
    <td>$3-5 for 10</td>
  </tr>
  <tr>
    <td>1</td>
    <td>EC11</td>
    <td>For volume control!</td>
    <td>C470754</td>
    <td>$0.35</td>
  </tr>
  <tr>
    <td>6</td>
    <td>WS2812</td>
    <td>For underglow!</td>
    <td>C42417498</td>
    <td>$0.47 for 10</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Seeed XIAO NRF52840</td>
    <td>Brain of the macropad!</td>
    <td>Buy it on aliexpress or from the official website</td>
    <td>$10</td>
  </tr>
  <tr>
    <td>1</td>
    <td>A simple switch</td>
    <td>ON/OFF/ON/OFF...</td>
    <td>I just used the one I had, I think it might be SK-12F14</td>
    <td>$0.30</td>
  </tr>
  <tr>
    <td>1</td>
    <td>Li-Ion 18650</td>
    <td>"The power of the sun in the palm of my hand"</td>
    <td>Just use the one you've got or buy a good quality one</td>
    <td>$5</td>
  </tr>
</table>
<br>
So basically it costs about $50-60 with shipping, but you can save like 30 bucks by reusing old parts and buying things locally. For me, the price was around $28.


<br><hr>
<h2>Installing the firmware.</h2>
To install the firmware first we have to compile it. You can just download the compiled file in the release tab, or go to my other repository with all of the configs <a href="https://github.com/maciusiomek/zmk-config-maciusiomek">here</a>, fork it and compile it by yourself in the action tab (Press "Build ZMK firmware" and give it 5 minutes).<br><br>

Now that you've got your .uf2 file, connect your Seeed XIAO nRF52840 and double press the reset button. A removable disc should appear - upload your firmware to it. Give it a minute or so and press the reset button again. You might get some error indicating that the disk was not properly ejected. You can just ignore them.


So basically that's it! Go to your bluetooth settings and you should see a device named "SwiChain"! Enjoy your new macropad!
<hr>
Big thanks to the guy who made<a href="https://www.ubiqueiot.com/posts/xiao-nrf52840-zmk"> this tutorial</a> and creators of <a href="https://github.com/zmkfirmware/zmk">ZMK firmware</a>! <br>
Also here are some 3D previews of the PCB and a schematic!
<br><br>
<img width="810" height="674" alt="a" src="https://github.com/user-attachments/assets/6bb41995-056b-4a12-8ce3-0617c36ccc1f" />
<img width="776" height="618" alt="b" src="https://github.com/user-attachments/assets/92901b17-2e62-4e9f-b5e1-524a289bbfaf" />
<img width="3633" height="2598" alt="document" src="https://github.com/user-attachments/assets/a5ec42d5-f959-4d30-ab02-8182bd9e6ab7" />
