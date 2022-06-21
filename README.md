# Transport SFTP

Transport for ApiOpenStudio output over the SFTP protocol.

# Adding to your project

## Composer

    $ composer require apiopenstudio/transport_sftp

# Configuration

Add a remote output processor to your resource.

The output section example below will return the output in the response as well
as upload the response to a server using SFTP:

    output:
        -
            processor: xml_remote
            id: example XML Remote output
            filename: example.xml
            transport: ApiOpenStudio\Plugins\TransportSftp
            parameters:
                host:
                username:
                root_path:
                password:
                private_key:
                passphrase:
                port:
                user_agent:
                timeout:
                max_tries:
                fingerprint_string:
        - 
            response

**Note:** the value for the transport is the full namespace path.

## Parameters

### Required

- host
- username
- root_path

### Optional

- password
- private_key
- passphrase
- port
- user_agent
- timeout
- max_tries
- fingerprint_string

# Further information

See [FlySystem documentation][flysystem-docs] and
[The League GitHub][flysystem-github] for more details.

[flysystem-github]: https://github.com/thephpleague/flysystem-sftp-v3

[flysystem-docs]: https://flysystem.thephpleague.com/docs/adapter/sftp-v3/
