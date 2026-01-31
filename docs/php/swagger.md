# OpenAPI and Swagger UI

## Configuration {#config}
Swagger is available at the `/swagger` route, even if no routes have been annotated to be included in Swagger. The following
entries would probably have been added to your `.env` file on project initialization. Change these values to suit your project
```
[Open API]
SWAGGER_TITLE=Tina4 Project
SWAGGER_DESCRIPTION=Edit your .env file to change this description
SWAGGER_VERSION=1.0.0
```
## Annotations {#annotations}
The following annotations are used to create the swagger page
| Annotation | Description |
|------------|-------------|
| @summary | Short form description that remains visible even when collapsed |
| @description | Long form description that is only visible when expanded |
| @secure | Secures the route, which forces authentication to use the swagger endpoint |
| @tags | Groups endpoints together. If not used endpoints will be collected into the `default` group |
| @params | ? |
| @example | Provides the ability to document request and response examples |
| @example_request | ? |
| @example_response | ? |

## Usage {#usage}

### @summary and @description
These annotations are simple string inputs. The summary should be a tagline. The description, an explanation giving the user
enough information to decide to use the endpoint.
```php
/**
 * @summary A short form tag line
 * @description A long form explanation of the endpoint
 */
```

### @secure
The use of this is discussed in detail in the [routing section](basic-routing.md#route-security), and this is recommended reading.
For the purposes of swagger, secure routes will need authorization to be able to use them.