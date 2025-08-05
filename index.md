<html>
	<audio id="AudioId">
	    <source src="SampleMusic.mp3" type="audio/mpeg">
	</audio>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
   
			/* START:: Conversation Sent Listener */
			window.addEventListener( "onEmbeddedMessageSent", ( event ) => {
			
				console.log( "START:: Conversation Sent" );
				console.log( "Page location is " + window.location.href );
				console.log( "Event detail: ", JSON.stringify( event.detail ) );
				let objSound = document.getElementById( "AudioId" );
				objSound.play();
				console.log( "END:: Conversation Sent" );
			
			} );
			/* END:: Conversation Sent Listener */

			embeddedservice_bootstrap.init(
				'00DHo000002fRR9',
				'MIAW',
				'https://infallibletechie2-dev-ed.develop.my.site.com/ESWMIAW1754416406121',
				{
					scrt2URL: 'https://infallibletechie2-dev-ed.develop.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://infallibletechie2-dev-ed.develop.my.site.com/ESWMIAW1754416406121/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</html>
