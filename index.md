<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

   			/* START:: Messaging Window Minimize Listener */
			window.addEventListener( "onEmbeddedMessagingWindowMinimized", () => {
			
				console.log( "START:: Messaging Window Minimize" );
				alert( "Chat is not closed. It is just minimized." );
				console.log( "END:: Messaging Window Minimize" );
				
			} );
			/* END:: Messaging Window Minimize Listener */

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
