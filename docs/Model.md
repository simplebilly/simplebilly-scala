

# Model


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backupCodes** | **Seq&lt;String&gt;** |  | 
**createdAt** | **OffsetDateTime** |  | 
**deletedAt** | **OffsetDateTime** |  |  [optional]
**email** | **String** |  | 
**emailVerified** | **Boolean** |  | 
**id** | **UUID** |  | 
**isActive** | **Boolean** |  | 
**isTotpEnabled** | **Boolean** |  | 
**lastLogin** | **OffsetDateTime** |  |  [optional]
**name** | **String** |  | 
**oauthId** | **String** |  |  [optional]
**oauthProvider** | **String** |  |  [optional]
**passwordChangedAt** | **OffsetDateTime** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. |  [optional]
**passwordHash** | **String** |  | 
**picture** | **String** |  |  [optional]
**privacyAcceptedAt** | **OffsetDateTime** | When the user accepted the data privacy policy (GDPR consent record). |  [optional]
**totpSecret** | **String** |  |  [optional]
**updatedAt** | **OffsetDateTime** |  | 



