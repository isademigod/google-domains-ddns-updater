## Google Domains Dynamic DNS Updater

### Installation

#### Linux bash script

*Before install, make your own [JSON](#json-example) first.*

On Terminal:
```bash
# Update IP at runlevel 0 1 2 3 4 5 6 (while booting, rebooting, shutdown, etc.)
update-rc.d bootmail start 90 0 1 2 3 4 5 6 .
```

Add line below using `crontab -e`.
```bash
# Update IP for every 5 mins
*/5 *    *   *   *   /etc/init.d/update-ddns
```

## JSON Example
```json
{
	"amount": 3,
	"host":
	{
		"hostname": "mysubdomain.mydomain",
		"username": "iVETU0O6r0CTNYdX",
		"password": "XsaMlfmzSU1dRrMg"
	},
	"host":
	{
		"hostname": "mysubdomain2.mydomain",
		"username": "sUNeCRROUlnYbyDJ",
		"password": "afM95PIqWOGSNHHw"
	},
	"host":
	{
		"hostname": "mysubdomain3.mydomain",
		"username": "tNCcjHOKHyVnHTg0",
		"password": "GiBeuNrU92JXLd1w"
	}
}
```