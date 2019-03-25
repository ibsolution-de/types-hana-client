# Typings for @sap/hana-client

Typescript support/bindings on top of @sap/hana-client SAP Nodejs module to work with Hana DB from Nodejs application.

Currently SAP missing Typescript Typings for their module. So we decided to share our code to opensource community.

## DISCLAMER

The IBsolution GmbH Materials may include certain third party free or open source components ("FOSS Components"). You may have additional rights in such FOSS Components that are provided by the third party licensors of those components.

The IBsolution GmbH Materials may require certain third party software dependencies ("Dependencies") for the use or operation of such IBsolution GmbH Materials. These dependencies may be identified by IBsolution GmbH in NPM Package json files, product documentation or by other means. IBsolution GmbH does not grant You any rights in or to such Dependencies under this Developer Agreement. You are solely responsible for the acquisition, installation and use of Dependencies. IBsolution GmbH DOES NOT MAKE ANY REPRESENTATIONS OR WARRANTIES IN RESPECT OF DEPENDENCIES, INCLUDING BUT NOT LIMITED TO IMPLIED WARRANTIES OF MERCHANTABILITY AND OF FITNESS FOR A PARTICULAR PURPOSE. IN PARTICULAR, IBsolution GmbH DOES NOT WARRANT THAT DEPENDENCIES WILL BE AVAILABLE, ERROR FREE, INTEROPERABLE WITH THE IBsolution GmbH MATERIALS, SUITABLE FOR ANY PARTICULAR PURPOSE OR NON-INFRINGING. YOU ASSUME ALL RISKS ASSOCIATED WITH THE USE OF DEPENDENCIES, INCLUDING WITHOUT LIMITATION RISKS RELATING TO QUALITY, AVAILABILITY, PERFORMANCE, DATA LOSS, UTILITY IN A PRODUCTION ENVIRONMENT, AND NON-INFRINGEMENT. IN NO EVENT WILL IBsolution GmbH BE LIABLE DIRECTLY OR INDIRECTLY IN RESPECT OF ANY USE OF DEPENDENCIES BY YOU.

## Installation

Add module depency by executing this command inside your project folder:

```
npm install --save-dev github:ibsolution-de/-types-hana-client
```

## Usage

Basic example how to start using @sap/hana-client in Typescript:

```
import { ConnectionOptions, createConnection } from '@sap/hana-client';

const options: ConnectionOptions = {
    host    : 'myserver',
    port    : '30015',
    uid     : 'system',
    pwd     : 'manager'
};

const connection = createConnection();
connection.connect(options, err => {
    if (err) {
        throw new Error(err);
    }

    // do something

    // and disconnect
    connection.disconnect(err => {
        if (err) {
            throw new Error(err);
        }
    });
});
```

## Support

If you are interested to get support from us, please feel free to contact us or repository maintainer with email.
