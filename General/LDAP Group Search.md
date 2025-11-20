
To check what AD groups your account is in, run the following command in your terminal:

Replace <[user.name](http://user.name)> with your primary username. Replace <[user.name](http://user.name)-a> with the username you want to check the group membership of

`ldapsearch -o ldif-wrap=no -LLL -H ldaps://mipdc1.innova.local:3269 -D <user.name>@innova.local -W -b dc=innova,dc=local -s sub -x "samAccountName=<user.name-a>" memberOf`

`ldapsearch -o ldif-wrap=no -LLL -H ldaps://mipdc1.innova.local:3269 -D eric.wannemacher@innova.local -W -b dc=innova,dc=local -s sub -x "samAccountName=eric.wannemacher-a" memberOf`