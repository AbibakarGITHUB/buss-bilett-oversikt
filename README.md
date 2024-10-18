# buss-bilett-oversikt

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <div id="app"></div>




    <script>




        //model

let age = '';



function updateView() {
    const app = document.getElementById('app');
    app.innerHTML += `
        <h1>Welcome to the bus ticketing system.</h1>
        <p>Here are the bus ticket prices:</p>

<table>
        <p class="oversikt"></p>
        
            <tr class="price">
                <th class="header">Barne</th>
                <th class="grey">149.99 / month</th>
            </tr

            <tr class="price">
                <th class="header">Voksen</th>
                <th class="grey">249.99 / month</th>
            </tr>
            <tr class="price">
                <th class="header">Senior</th>
                <th class="grey">199.99 / month</th>
            </tr>
        </table>

        <input type="number" id="bil" placeholder="Put age in">
        <button onclick="findOut()" id="find">Find Ticket</button>
    `;
}

function findOut() {
    const age = document.getElementById('bil').value;
    let ticketType = "";

    if (age < 16) {
        ticketType = "Barne ticket";
    } else if (age >= 16 && age < 65) {
        ticketType = "Voksen ticket";
    } else {
        ticketType = "honer ticket";
    }

    alert("You qualify for a " + ticketType);
}


//uppdate

updateView();



    </script>
</body>
</html>
