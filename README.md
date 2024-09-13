Core Apps:
	frappe
	erpnext
	payments
	webshop (eCommerce)
-----------------------------------------
Add-ons: 
	hrms
	insights
	lms
	lending
	builder
	helpdesk
	healthcare	
	crm
	print_designer
	wiki
	gameplan
	ury https://github.com/ury-erp/ury.git (Open Source Kitchen Display System for more https://github.com/orgs/ury-erp/repositories)
	drive
	Front Desk https://github.com/core-initiative/front-desk (Hotel Front Office)
	ecommerce_integrations
	erpnext-shipping
	erpnext_price_estimation
	non_profit
	education
	changemakers
	restaurant_management (https://github.com/quantumbitcore/erpnext-restaurant.git)
	agriculture
	biometric-attendance-sync-tool
	waba_integration (WhatsApp Business)
	chat
	hospitality ( manage hotels & restaurants)
	bench_manager
	nextcloud-integration
-----------------------------------------
Standalone Application: books
-----------------------------------------
docker compose -p pwd -f pwd.yml up -d
docker logs  pwd-create-site-1 -f

[frontend Container] bench get-app erpnext			
[frontend Container] bench get-app payments
[frontend Container] bench get-app webshop
[frontend Container] bench get-app education
[frontend Container] bench get-app lms
[frontend Container] bench get-app hospitality
[frontend Container] bench --site frontend install-app erpnext
[frontend Container] bench --site frontend install-app payments
[frontend Container] bench --site frontend install-app webshop
[frontend Container] bench --site frontend install-app education
[frontend Container] bench --site frontend install-app hospitality
[frontend Container] bench --site frontend list-apps
[frontend Container] bench migrate --skip-failing

[backend Container] bench get-app erpnext
[backend Container] bench get-app payments
[backend Container] bench get-app webshop
[backend Container] bench get-app education
[backend Container] bench get-app lms
[backend Container] bench get-app hospitality
[backend Container] bench --site frontend install-app erpnext
[backend Container] bench --site frontend install-app payments
[backend Container] bench --site frontend install-app webshop
[backend Container] bench --site frontend install-app education
[backend Container] bench --site frontend install-app hospitality
[backend Container] bench --site frontend list-apps
[backend Container] bench migrate --skip-failing

Stop all Container and run again
----------------------------------------------
[frontend Container for CSS broken] bench build --app frappe --hard-link
[frontend Container for CSS broken] bench build --app erpnext --hard-link
[frontend Container for CSS broken] bench build --app payments --hard-link
[frontend Container for CSS broken] bench build --app webshop --hard-link
[frontend Container for CSS broken] bench build --app education --hard-link
[frontend Container for CSS broken] bench build --app hospitality --hard-link

bench --site frontend clear-cache
