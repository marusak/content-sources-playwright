# Install

yarn install

# Install Playwright browsers and dependencies

yarn playwright install --with-deps

# Copy the example.env > .env

This stores your local credentials

# (Optionally) Pull front-end/backend tests:

yarn get-tests

# Option 1 Run local:

For local testing, make sure your front-end/backend servers are running and accessible, then:

- Ensure you do NOT specify a proxy in your .env file (put an empty value: "")
- Make sure your .env's BASE_URL is pointed to the local front-end server "https://stage.foo.redhat.com:1337"

# Option 2 Run local:

For local stage testing, make sure the following:

- PROXY must be set correctly in your .env file.
- Make sure your .env's BASE_URL is pointed to the targeted env, if targeting PROD, the proxy is not needed.

# Run your tests:

yarn playwright test

# Run a specific test:

yarn playwright test UI/CreateCustomRepo.spec.ts
