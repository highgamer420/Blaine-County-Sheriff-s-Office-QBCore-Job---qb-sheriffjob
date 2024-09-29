# Blaine-County-Sheriff-s-Office-QBCore-Job---qb-sheriffjob
qb-sheriffjob is a fully-featured Sheriff's Office job for FiveM using the QBCore framework. It allows players to take on the role of law enforcement officers within the Blaine County Sheriff's Office (BCSO). This resource comes with a structured rank system, rank-based vehicle access, a duty system, and customizable job settings.

--- Features

Rank System: Progress through the ranks from Cadet to Sheriff with customizable payments for each grade.

Duty System: Players can toggle between on-duty and off-duty modes.

Rank-Specific Vehicles: Each rank in the Sheriff's Office has access to specific vehicles (customizable).

Flexible Configuration: Modify ranks, vehicles, payments, and more through the config.lua file.

Seamless QBCore Integration: Uses the QBCore framework for easy job and player management.

Lightweight and Customizable: Optimized for performance and customization to fit your server’s needs.

--- Job Ranks

BCSO Cadet (Grade 0)

Deputy (Grade 1)

Senior Deputy (Grade 2)

Master Deputy (Grade 3)

Field Training Officer (Grade 4)

Sergeant (Grade 5)

Staff Sergeant (Grade 6)

Lieutenant (Grade 7)

Captain (Grade 8)

Undersheriff (Grade 9)

Sheriff (Grade 10)

--- Vehicle System

Each job rank is assigned specific vehicles based on their grade. You can customize these vehicles in config.lua.

Example:

Cadet: police vehicle model

Deputy: police2 vehicle model

Sergeant: sheriff vehicle model

Sheriff: sheriff3 vehicle model

--- Commands

/sheriffvehicle: Spawn a vehicle based on your job rank.

/toggleduty: Toggle on/off duty status (can be configured).


--- Customize the vehicles and ranks in config.lua to fit your server's needs.

--- Requirements

qb-core: Ensure you have the QBCore framework installed and configured.

 Vehicles: Ensure all vehicle models used in the script are available in your server's vehicle pack.

--- Customization

You can easily pay by editing config.lua.

You can add or remove vehicles for each job rank to fit your server's theme or available vehicle pack.

 How to Use

Assign players the sheriff job using an admin command

Players can toggle duty status using /toggleduty and spawn vehicles using /sheriffvehicle.

The job will automatically handle payments, rank promotions, and vehicle assignments.

--- License

This resource is open-source and free to use. Modify it as needed for your server.

--- Installation

Download the qb-sheriffjob resource from the GitHub repository.

Extract the folder to your resources/[jobs] directory.

Add to server.cfg:

Copy code

ensure qb-sheriffjob

Configure the job in qb-core/shared/jobs.lua:

Copy code

``` ['sheriff'] = {
    label = 'Blaine County Sheriff\'s Office',
    defaultDuty = true,
    offDutyPay = false,
    grades = {
        ['0'] = { name = 'BCSO Cadet', payment = 500 },
        ['1'] = { name = 'Deputy', payment = 750 },
        ['2'] = { name = 'Senior Deputy', payment = 950 },
        ['3'] = { name = 'Master Deputy', payment = 1200 },
        ['4'] = { name = 'Field Training Officer', payment = 1450 },
        ['5'] = { name = 'Sergeant', payment = 1750 },
        ['6'] = { name = 'Staff Sergeant', payment = 2000 },
        ['7'] = { name = 'Lieutenant', payment = 2200 },
        ['8'] = { name = 'Captain', payment = 2500 },
        ['9'] = { name = 'Undersheriff', isboss = true, payment = 4500 },
        ['10'] = { name = 'Sheriff', isboss = true, payment = 5500 },
    },
},```
