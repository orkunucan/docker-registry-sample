### Private docker registry cook book


    # Before you begin must be install the this packages
	sudo apt-get update && sudo apt-get install apache2-utils docker-compose


Then


	# Clone the respository
	git clone https://github.com/orkunucan/docker-registry-sample.git
	cd docker-registry/auth
	# We must be create new user
	htpasswd -B registry.password domates
	
	# Use the password from the command line rather than prompting for it.
	htpasswd -B -b -n hasan hasan
	
	# Return the root repository folder
	cd ..
	docker-compose up -d