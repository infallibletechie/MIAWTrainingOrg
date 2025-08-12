<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

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
   <div style="position: fixed; bottom: 35px; right: 35px; border-radius: 40px; background: #801818; cursor: pointer; color: white">
         <div onclick="launchChat()">
            <img 
               src="<Please use your image>"
               style="border-radius: 50%; float:left; margin: 5px;"
               height="50px"
               width="50px"/>
	       <h3 style="float:right;">Hi, How can I help you?</h3>
         </div>
   </div>
   <script>
	function launchChat() {
           embeddedservice_bootstrap.utilAPI.launchChat()
               .then(() => {
                   console.log(
                       'Successfully launched Messaging'
                   );
               }).catch(() => {
                   console.log(
                       'Some error occurred when launching Messaging'
                   );
               }).finally(() => {
                   console.log(
                       'Successfully launched Messaging - Finally'
                   );
               });
       }
   </script>
</html>
