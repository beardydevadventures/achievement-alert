<h1>Achievement Alert</h1>

Installing to website:

Achievement Alert makes use of the jQuery and Font-Awesome libraries. Please make sure these are included on your webpage.

<link href="//maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css" rel="stylesheet">

<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>


After including these two libraries you need place the Achievement Alert files in the following directories:

/css/achievment_alert.css
/js/achievement_alert.js


Then include these files in your webpage:

<link rel="stylesheet" href="css/achievement_alert.css">

<script src="js/achievement_alert.js"></script>

If you want to have a sound play for the achievement put a mp3 sound file in a sounds folder located in the root of your site:

/sounds/achievement_alert.mp3


Using Achievement Alert:

To make the alert appear you use the following code.

$().achievement_alert({
	points : '350',
	name : 'Achievement Name'
});

Achievement alert can handle the following options, if nothing is set it will use the default.

$().achievement_alert({
	duration: 400,					// Duration for fade animation in milliseconds
    display: 3000,					// How long the achievement text is displayed in milliseconds
    title: 'Achievement', 	// Title of alert box
    points : '350',					// Number of points to be displayed
    currency : 'P', 				// Points description
    name : 'Achievement Name', 		// Name of achievement
    icon : 'fa-trophy', 			// Icon to be shown (uses font awesome)
    sound : 'F' 					// Play achievement sound or not set to either T or F
});


An example:
A user clicked on a button gets an alert

$("#click_button").on('click', function() {
	$().achievement_alert({
		display: 1000,
        title: 'Achievement Alert',
        points : '35',
        currency : ' Points',
        name : 'You clicked the button!',
        icon : 'fa-thumbs-up'
	});
});