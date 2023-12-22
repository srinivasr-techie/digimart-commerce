# Digi Retail

https://help.sap.com/docs/SAP_COMMERCE_COMPOSABLE_STOREFRONT/cfcf687ce2544bba9799aa6c8314ecd0/bf31098d779f4bdebb7a2d0591917363.html

**Softwares:**
SAP JDK 17.08
Node JS - Version 16.13.0 or a newer 16.x version, or else version 18.10.0 or a newer 18.x version.
npm - Version 8.0 or newer.
Angular CL - Version 15.2.4 is the minimum required. The most recent 15.x version is strongly recommended.

**SAP Commerce:**
Spartacus 6.3
SAP Commerce 2211

# Impex import after system update
INSERT_UPDATE OAuthClientDetails;clientId[unique=true] ;resourceIds ;scope  ;authorizedGrantTypes  ;authorities ;clientSecret ;registeredRedirectUri
                                ;client-side              ;hybris            ;basic        ;implicit,client_credentials                                  ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_implicit_callback;
                                ;mobile_android           ;hybris            ;basic        ;authorization_code,refresh_token,password,client_credentials    ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_callback;
# To test aboove import
curl -k -d "client_id=mobile_android&client_secret=secret&grant_type=client_credentials" -X POST https://localhost:9002/authorizationserver/oauth/token

INSERT_UPDATE CorsConfigurationProperty;key[unique=true];value;context[default=commercewebservices,unique=true]
        ;allowedOrigins;http://localhost:4200 https://localhost:4200
        ;allowedOriginPatterns;*
        ;allowedMethods;GET HEAD OPTIONS PATCH PUT POST DELETE
        ;allowedHeaders;origin content-type accept authorization cache-control x-anonymous-consents x-profile-tag-debug x-consent-reference occ-personalization-id occ-personalization-time
        ;allowCredentials;true
        ;exposedHeaders;x-anonymous-consents occ-personalization-id occ-personalization-time
        
# Swagger UI URL
https://localhost:9002/occ/v2/swagger-ui/index.html
