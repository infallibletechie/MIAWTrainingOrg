<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00D3t000005YGES',
				'MIAW',
				'https://test-ec-dev-ed.develop.my.site.com/ESWMIAW1701005238481',
				{
					scrt2URL: 'https://test-ec-dev-ed.develop.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://test-ec-dev-ed.develop.my.site.com/ESWMIAW1701005238481/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

</html>
