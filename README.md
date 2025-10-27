# Nikita
Münzen = 999999999999999999999,
sourceId = localStorage.getItem('sourceId').split('"').join(''),
deviceLogId = localStorage.getItem('deviceLogId').split('"').join(''),
Benutzer = JSON.parse(localStorage.getItem('Benutzer'));
Benutzer.fürJeden(Benutzer__Wert => {
    fetch('https://logger-lb-5.anton.app/events', {
        Methode: 'POST',
        'Header': { 'Inhaltstyp': 'application/json' },
        Text: JSON.stringify({
            "Ereignisse": [{"Ereignis": "Coins anpassen", "Wert": Münzen, "Quelle": "Quellen-ID", "erstellt": (neues Datum ()).toISOString ()}],
            "log":users__value.l,
            "Anmeldeinformationen": {"authToken":users__value.t,"deviceLogId":deviceLogId}
        }),
    }).then(v=>v).catch(v=>v).then(data => { window.location.reload(); });
});
