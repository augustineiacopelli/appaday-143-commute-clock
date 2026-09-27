# Commute Clock

**AppADay #143** | Category: Data (D) | Shipped September 27, 2026

**Live app:** https://augustineiacopelli.github.io/appaday-143-commute-clock/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

Commute Clock shows what each drive to work costs in gas and what a day at home keeps in your pocket. Set your commute once, slide the number of days you actually go in, and watch the yearly cost, the savings, and the hours you get back update as you move.

## How it works

The app has three tabs in a nav bar pinned to the top of the screen.

**Clock** is the main view. A headline states what you keep each year, and a slider sets how many days a week you commute. Four cards give the daily, weekly, monthly, and yearly gas cost at that day count, each with your full schedule figure beneath it for comparison. A bar chart shows the yearly cost at every day count from zero up to your full schedule, and tapping any bar moves the slider there. A strip below adds up your savings over one, three, and five years at today's gas price.

The **Add the time cost** section turns commute minutes into hours per year and shows how many you reclaim by staying home. Put a value on that time with either an hourly rate or an annual salary. Salary is converted to an hourly figure by dividing by your weekly hours times 52, since a salary also pays for holidays and vacation. The section then totals the gas and time savings together.

**Setup** holds one way miles, MPG, gas price, work weeks per year, the days your job expects, and your lunch habit. Choosing Drive home for lunch adds a midday round trip to every commute day. A price source toggle chooses between the price you type and the average from your own fillups.

**Fillups** is a tank log. Record the date, gallons, total paid, and an optional odometer reading for each fillup. The log shows your average price per gallon over your last five tanks, your average cost per fillup, your total spent, and your price for every tank. With two or more odometer readings it also works out your real MPG, and one tap applies it to the calculator.

## The math

Cost per commute day is miles one way times trips per day, divided by MPG, times the gas price. Trips per day is 2, or 4 when you drive home for lunch. Weekly cost is the daily cost times commute days, yearly cost is weekly cost times work weeks, and monthly cost is yearly divided by 12. The fillup price is weighted by gallons, and logged MPG divides the miles between odometer readings by the gallons that refilled them, which assumes each fillup tops off the tank.

## Details

Everything is saved in your browser under the localStorage key `appaday-143-commute-clock`, so your settings, active tab, and full fillup log return on your next visit. Nothing leaves your device. Reset settings restores the default commute but keeps your fillup log; individual fillups are removed with their own delete buttons.

The default gas price of $3.94 is the Kansas average for September 2026. Commute traffic usually cuts fuel economy 15 to 30 percent below the window sticker, so the dashboard reading gives a truer number.

## Built with

A single `index.html` with inline CSS and vanilla JavaScript, Google Fonts (Sora and JetBrains Mono), and an SVG chart drawn by hand. No frameworks, no build step, no API calls. Responsive from 375px phones to desktop, with 44px minimum tap targets and keyboard support for the tabs and chart bars.

---

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), one complete app shipped every day.
