Paramount-Series-50-Ebike-Conversion

I designed and built my own 13S5P lithium ion battery pack in order to convert an old Paramount mountain bike into an ebike. 

Before:

<img width="4032" height="3024" alt="IMG_5441-2" src="https://github.com/user-attachments/assets/aa241e10-9e2e-4f6e-b18c-d7225eacf886" />

<img width="4032" height="3024" alt="IMG_5485-2" src="https://github.com/user-attachments/assets/e7348fb4-9ecc-4928-9e7b-9be136b2de9b" />

After:

<img width="872" height="538" alt="Screenshot 2026-08-12 at 6 17 08 PM" src="https://github.com/user-attachments/assets/9f3e7798-2200-4c62-add5-7b3a1d3301aa" />

<img width="812" height="548" alt="Screenshot 2026-08-12 at 6 16 56 PM" src="https://github.com/user-attachments/assets/6e698c10-f50d-419a-90a0-5a1bd54e5eb6" />

Project Overview:

What I Built:

I built a 46.8V, 13Ah battery to convert an old mountain bike frame into a Class 3 Ebike. I used an old steel cross country mountain bike frame that my grandfather has been riding since the 70’s. The main components are the battery, a 500W rear brushless hub motor, an 18A max input current controller, a throttle, a pedal assist sensor, brake sensors, new rim brakes, a new chain, a new rear derailleur, and a new cassette. 

Why I Built It: 

I decided to build this bike for my father and grandfather. My grandfather has been riding this frame since the 70’s. He gifted this bike to my father a few years back after he stopped riding. It had a lot of worn down parts and was kind of a pain to ride so my father didn’t get much use out of it. Coming home for the summer, I decided it was time to give the bike new life. My father has always wanted an ebike and so I decided I could build one for him. Being interested in batteries, I decided to take on the extra challenge of building my own.

My Goals and Constraints:

My goals were to build a safe and durable ebike capable of reaching 25 MPH on flat roads without pedaling, and with 30 miles of range. My main constraint was cost. I had a budget of $1000 dollars for this project. Building the battery was the biggest cost as I had very little equipment at home to do this with and cells are expensive. I also wanted the bike to weigh in at under 50 pounds after completion. I also needed to make sure that the bike frame could accommodate all of the new things going on the bike. I also needed to consider the stress that the motor was going to put on my rear drop outs. 

Outcome:

On flat pavement, the bike is able to reach 25 MPH without any pedaling. With pedaling, it sits comfortably at 28-29 MPH. The range of the bike will depend on whether or not you are using heavy throttle or more pedal assist and what speed mode you are mainly in. It hovers around an estimated 35 miles when using heavy throttle and some pedaling. It has a total of 608.4 Wh but usable energy is probably a bit lower. So with the 35 miles of range, the estimated Wh/mile is around 17.38. I ended up spending around $990 dollars on this project. The bike weighs 40.5 pounds. Everything fit well on the bike like I planned except the front derailleur which isn't that necessary for this bike. The bike is fitted with many important safety features such as a torque arm, brake sensors, and zip ties for holding cables in place.

System Block Diagram/Design Photos:

<img width="1042" height="633" alt="Screenshot 2026-08-05 at 10 01 35 AM" src="https://github.com/user-attachments/assets/a332fdd0-7fc1-4517-8106-d221066df356" />

<img width="4280" height="3352" alt="IMG_5607 2" src="https://github.com/user-attachments/assets/4e9c9497-758e-43ba-94ff-a1ab2f4f7059" />

Important Electrical Calculations:

1. Battery Energy:

E = V(nominal)xAh(total) = 46.8 x 13 = 608.4 Wh

Battery has an energy capacity of 608.4 Wh. Usable energy is probably lower.

2. Maximum Controller Input Power:

The controller has a max rated input current of 18A.

At full charge the battery has 54.6V. So Pmax = 54.6 x 18 = 982.8 W.

This means the controller has a maximum battery side input power of 982.8 W when the battery is at max voltage.

At batteries nominal voltage of 46.8V the Pnominal = 46.8 x 18 = 842.4 W.

These are theoretical power input values and do not tell us how much power the controller is delivering to the motor.

3. Estimated Range:

Using a 90% usable energy estimation, and an average estimated consumption of 17Wh/mile which is typical for this type of motor:

Range = Usable energy/(Wh/Mile) = (.9 X 608.4)/(17) = 32.2 miles.

4. Voltage Sag Test:

Uses a measured initial voltage of 50.4V and a display measured post-acceleration voltage of 50.2V. This was for a 7 second acceleration test and used the display to measure voltage which is probably inaccurate.

Vdrop = Vinitial - Vfinal = 50.4 - 50.2 = 0.2V.

%drop = 0.2/50.4 = .39%

This voltage was measured by the display and is most likely highly inaccurate.

Build Process Summary:

My build process started by stripping the bike of all of the old shifting, wheels, and chain. I then built the battery using a spot welder. Then I fitted the battery into the casing and soldered on the XT90 connection on the main power wires. I mounted it on the bike. I then mounted the controller, motor, screen and throttle.

After connecting everything together I was able to test if my design was at least somewhat functional. The motor did not spin initially. I decided to take off the battery and investigate and I found that when securing the case, one of the thin BMS cell group wires had been torn from the BMS. I had to re-solder all 14 connections using a new bunch of wires. 

I secured the battery to the bike and tested the motor and it worked correctly. I then attached the rear derailleur, chain, brakes, brake sensors, and the pedal assist sensor.

Mechanical Integration Summary:

This ebike conversion project was built around a 13S5P battery pack that I mounted to the cylindrical downtube with a cylindrical mounting tube and hose clamps. Originally, I planned to mount the ESC underneath the battery on the underside of the downtube, however the factory ESC clamps were too small for the large downtube diameter. I considered braising on the ESC but this would have been an added cost that I wasn’t willing to take on. So I mounted the ESC to the front side of the seattube where it happily fit. 

The motor fit snugly in the steel rear dropouts. The steel frame gave me a bit of security to know that the rear dropouts weren’t going to quickly wear down from the heavy torque, especially because I installed a universal torque arm. 

I was able to secure all of the wires to the frame with mainly zipties, but while still leaving enough slack for them to wiggle a bit.

Future Improvements:

- I think that there could be improvements made on improving the motor rattle at high speeds. Or at least figuring out the source of it. My first step would be to use temperature sensors to test whether the rattling only occurs at high motor temps.

- I would like to eventually add disk brakes to this bike, however that would require a new front wheel. E bikes are a lot more powerful and I think having the strength and further consistency of disk brakes as opposed to rim brakes would be nice.

- Lastly, I would like to make the bike more comfortable. The bike currently has no suspension and feels a bit stiff. I would like to add a shock absorbing stem and a dropper seat post.

What I learned:

- How individual lithium ion cells are combined to create one larger functioning battery.

- The general idea behind how a battery pack is assembled.

- How the battery and controller/inverter work together to spin the rotor.

- How CC-CV charging works and why is it necessary.

Here are my progress photos:

<img width="477" height="380" alt="Screenshot 2026-08-12 at 7 30 10 PM" src="https://github.com/user-attachments/assets/786e1493-6170-4de7-9fdb-69aeb4231b0a" />

This is the lithium ion cell that I used. The Monocle INR 18650 P26A.

<img width="3727" height="4442" alt="tempImage5jf5pm" src="https://github.com/user-attachments/assets/e048a8d2-19ee-47e4-83a0-4b07d84d74c0" />

This is me measuring the voltage of each individual cell to make sure that there weren't any bad ones.

<img width="406" height="450" alt="Screenshot 2026-07-14 at 8 58 05 AM" src="https://github.com/user-attachments/assets/da6096c7-86b6-4d86-a256-6351d9b9c64c" />

This is the orientation of the cells before spot welding. You can see that I added insulator rings to the positive terminal of the cells to keep cell positive more separate from cell negative.

<img width="445" height="700" alt="Screenshot 2026-08-02 at 9 45 34 PM" src="https://github.com/user-attachments/assets/a00ca2e0-45e0-406a-a72a-66ee4af68f53" /> 

This is the pack post spot welding.

<img width="914" height="635" alt="Screenshot 2026-07-14 at 9 00 08 AM" src="https://github.com/user-attachments/assets/8b2f811f-7bd8-4946-b189-e27579355b31" />

I added a bit of insulator tape and started to figure out how long all of the BMS balance wires needed to be and validated that the BMS would fit.

<img width="494" height="646" alt="Screenshot 2026-07-14 at 9 01 37 AM" src="https://github.com/user-attachments/assets/c0a3e1e7-f669-42aa-815f-046c472115c1" />

I then soldered on the balance wires to each cell group.

<img width="451" height="376" alt="Screenshot 2026-07-14 at 9 06 52 AM" src="https://github.com/user-attachments/assets/9915a542-f8b2-4f36-8ea6-0d66dc155106" />

I soldered the rest of the wires and then finished insulation the entire battery.

<img width="528" height="412" alt="Screenshot 2026-07-14 at 9 08 08 AM" src="https://github.com/user-attachments/assets/a790f7e0-4397-4203-9b86-25a27bee2e47" />

Made sure to add the inline fuse, and then I was ready to fit the battery in the pack and then I tested the voltage of the power wires.

<img width="566" height="718" alt="Screenshot 2026-07-14 at 9 22 11 AM" src="https://github.com/user-attachments/assets/78f1b438-677f-4e28-8421-d480e08896de" />

I mounted the battery pack, controller, wheel to the bike but the wheel would not respond to the throttle.

<img width="279" height="569" alt="Screenshot 2026-07-14 at 9 08 52 AM" src="https://github.com/user-attachments/assets/64d6c5ba-94c8-4740-9ac6-52f9f9faeab5" />

I discovered that one of the BMS balance wires was broken when I was inserting the battery into the casing. So I had to order new balance wires and re-solder all of them.

<img width="697" height="377" alt="Screenshot 2026-07-14 at 9 09 55 AM" src="https://github.com/user-attachments/assets/4c8fd2ec-bdcf-4164-b190-4b1ba884973e" />

This time I reinforced the white BMS connector with extra insulator tape.

https://github.com/user-attachments/assets/f7685518-4ae5-4343-bd6b-281c48106b2e

I remounted the battery and the wheel responded to the throttle as planned.

https://github.com/user-attachments/assets/909b0014-d12a-4832-a319-c719571f4bf7

Screen.

<img width="872" height="670" alt="Screenshot 2026-07-26 at 10 30 43 PM" src="https://github.com/user-attachments/assets/8ee4705b-d508-47a7-8c02-fc7ea043f699" />

I added the tire to the back rim.

<img width="494" height="606" alt="Screenshot 2026-08-12 at 6 23 02 PM" src="https://github.com/user-attachments/assets/71537dc1-2da1-43e3-be37-ddd7b5992676" />

Handlebars with throttle on left and screen on right.

<img width="525" height="708" alt="Screenshot 2026-08-12 at 6 21 28 PM" src="https://github.com/user-attachments/assets/9488757c-ed81-4d45-a6bd-57dfe867ccb6" />

Battery and controller.

<img width="522" height="689" alt="Screenshot 2026-08-12 at 6 22 17 PM" src="https://github.com/user-attachments/assets/63397964-7ca0-40e6-a05d-3aa60da43de6" />

Battery to controller XT90 connection.

<img width="374" height="591" alt="Screenshot 2026-08-12 at 6 20 40 PM" src="https://github.com/user-attachments/assets/cfea052a-a20c-49e8-b6e6-16420056ae58" />

Drive side axle with torque arm.

<img width="444" height="492" alt="Screenshot 2026-08-12 at 6 20 57 PM" src="https://github.com/user-attachments/assets/4dddef9c-61fd-43cf-a3b3-578d891b8ad7" />

Non-drive side axle.

<img width="521" height="703" alt="Screenshot 2026-08-02 at 9 45 57 PM" src="https://github.com/user-attachments/assets/b6f2df05-a1e4-4f8c-9c72-1b64ec26bc82" />

Front Rim Brake.

<img width="505" height="690" alt="Screenshot 2026-08-02 at 9 46 08 PM" src="https://github.com/user-attachments/assets/b847d670-8e57-4136-b394-eccfd92a2def" />

Rear Rim Brake.

<img width="872" height="538" alt="Screenshot 2026-08-12 at 6 17 08 PM" src="https://github.com/user-attachments/assets/9f3e7798-2200-4c62-add5-7b3a1d3301aa" />

Final Photo Drive Side.

<img width="812" height="548" alt="Screenshot 2026-08-12 at 6 16 56 PM" src="https://github.com/user-attachments/assets/6e698c10-f50d-419a-90a0-5a1bd54e5eb6" />

Final Photo Non-drive Side.

https://github.com/user-attachments/assets/d6382416-3bef-4d25-9b0b-de143a25eade

Downhill test run clip.

https://github.com/user-attachments/assets/c1bc059b-d885-4b4b-afb8-47811cfc42c1

Uphill test run clip.

https://github.com/user-attachments/assets/48cc867e-3c4a-477d-a456-a1bcf3825056

25 MPH top speed test clip.





























