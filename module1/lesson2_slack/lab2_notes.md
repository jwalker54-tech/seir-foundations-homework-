**Predict first:** how many of the four messages will arrive?
	1. only one will be delivered as only one is critical, the others are not; only the ones with critical severity

    What happens, and why is a kill switch like this useful during maintenance windows?
	1. if you expect the system to be down and dont want it sending our alerts during a planned maintane window as it would make people think something is wrong when it is maintenance

    Did the severity change?
    yes

    why is a quiet INFO here GOOD design, not a failure?
    it allows you to seperate out different kinds of alerts, you dont want to spam messages as they can become noise that gets ignored.

    which severities arrived, and WHY those?
    only the ones specified as we changed the criteria.

    what would make this number spike on the Balerica bank?
    if there were too many entries in a short period of time
    
    which of these fake incidents deserves to wake a human at 3 AM?
    only ones that are critical and indicate an issue that needs immediate attention or cause further issues if left unchecked