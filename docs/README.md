# Documentation for MailSlurp API

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://api.mailslurp.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AliasControllerApi* | [**createAlias**](Apis/AliasControllerApi.md#createalias) | **POST** /aliases | Create an email alias
*AliasControllerApi* | [**createAnonymousAlias**](Apis/AliasControllerApi.md#createanonymousalias) | **POST** /aliases/anonymous | Create an anonymous email alias
*AliasControllerApi* | [**deleteAlias**](Apis/AliasControllerApi.md#deletealias) | **DELETE** /aliases/{aliasId} | Delete an owned alias
*AliasControllerApi* | [**getAlias**](Apis/AliasControllerApi.md#getalias) | **GET** /aliases/{aliasId} | Get an email alias
*AliasControllerApi* | [**getAliases**](Apis/AliasControllerApi.md#getaliases) | **GET** /aliases | Get all email aliases
*AliasControllerApi* | [**updateAlias**](Apis/AliasControllerApi.md#updatealias) | **PUT** /aliases/{aliasId} | Update an owned alias
*AttachmentControllerApi* | [**uploadAttachment**](Apis/AttachmentControllerApi.md#uploadattachment) | **POST** /attachments | Upload an attachment for sending
*AttachmentControllerApi* | [**uploadMultipartForm**](Apis/AttachmentControllerApi.md#uploadmultipartform) | **POST** /attachments/multipart | Upload an attachment for sending using Multipart Form
*BulkActionsControllerApi* | [**bulkCreateInboxes**](Apis/BulkActionsControllerApi.md#bulkcreateinboxes) | **POST** /bulk/inboxes | Bulk create Inboxes (email addresses)
*BulkActionsControllerApi* | [**bulkDeleteInboxes**](Apis/BulkActionsControllerApi.md#bulkdeleteinboxes) | **DELETE** /bulk/inboxes | Bulk Delete Inboxes
*BulkActionsControllerApi* | [**bulkSendEmails**](Apis/BulkActionsControllerApi.md#bulksendemails) | **POST** /bulk/send | Bulk Send Emails
*CommonActionsControllerApi* | [**createNewEmailAddress**](Apis/CommonActionsControllerApi.md#createnewemailaddress) | **POST** /createInbox | Create new random inbox
*CommonActionsControllerApi* | [**createNewEmailAddress1**](Apis/CommonActionsControllerApi.md#createnewemailaddress1) | **POST** /newEmailAddress | Create new random inbox
*CommonActionsControllerApi* | [**emptyInbox**](Apis/CommonActionsControllerApi.md#emptyinbox) | **DELETE** /emptyInbox | Delete all emails in an inbox
*CommonActionsControllerApi* | [**sendEmailSimple**](Apis/CommonActionsControllerApi.md#sendemailsimple) | **POST** /sendEmail | Send an email
*ContactControllerApi* | [**createContact**](Apis/ContactControllerApi.md#createcontact) | **POST** /contacts | Create a contact
*ContactControllerApi* | [**deleteContact**](Apis/ContactControllerApi.md#deletecontact) | **DELETE** /contacts/{contactId} | Delete contact
*ContactControllerApi* | [**getAllContacts**](Apis/ContactControllerApi.md#getallcontacts) | **GET** /contacts/paginated | Get all contacts
*ContactControllerApi* | [**getContact**](Apis/ContactControllerApi.md#getcontact) | **GET** /contacts/{contactId} | Get contact
*ContactControllerApi* | [**getContacts**](Apis/ContactControllerApi.md#getcontacts) | **GET** /contacts | Get all contacts
*DomainControllerApi* | [**createDomain**](Apis/DomainControllerApi.md#createdomain) | **POST** /domains | Create Domain
*DomainControllerApi* | [**deleteDomain**](Apis/DomainControllerApi.md#deletedomain) | **DELETE** /domains/{id} | Delete a domain
*DomainControllerApi* | [**getDomain**](Apis/DomainControllerApi.md#getdomain) | **GET** /domains/{id} | Get a domain
*DomainControllerApi* | [**getDomains**](Apis/DomainControllerApi.md#getdomains) | **GET** /domains | Get domains
*EmailControllerApi* | [**deleteAllEmails**](Apis/EmailControllerApi.md#deleteallemails) | **DELETE** /emails | Delete all emails
*EmailControllerApi* | [**deleteEmail**](Apis/EmailControllerApi.md#deleteemail) | **DELETE** /emails/{emailId} | Delete an email
*EmailControllerApi* | [**downloadAttachment**](Apis/EmailControllerApi.md#downloadattachment) | **GET** /emails/{emailId}/attachments/{attachmentId} | Get email attachment bytes
*EmailControllerApi* | [**forwardEmail**](Apis/EmailControllerApi.md#forwardemail) | **POST** /emails/{emailId}/forward | Forward email
*EmailControllerApi* | [**getAttachmentMetaData**](Apis/EmailControllerApi.md#getattachmentmetadata) | **GET** /emails/{emailId}/attachments/{attachmentId}/metadata | Get email attachment metadata
*EmailControllerApi* | [**getAttachments**](Apis/EmailControllerApi.md#getattachments) | **GET** /emails/{emailId}/attachments | Get all email attachment metadata
*EmailControllerApi* | [**getEmail**](Apis/EmailControllerApi.md#getemail) | **GET** /emails/{emailId} | Get email content
*EmailControllerApi* | [**getEmailHTML**](Apis/EmailControllerApi.md#getemailhtml) | **GET** /emails/{emailId}/html | Get email content as HTML
*EmailControllerApi* | [**getEmailsPaginated**](Apis/EmailControllerApi.md#getemailspaginated) | **GET** /emails | Get all emails
*EmailControllerApi* | [**getRawEmailContents**](Apis/EmailControllerApi.md#getrawemailcontents) | **GET** /emails/{emailId}/raw | Get raw email string
*EmailControllerApi* | [**getRawEmailJson**](Apis/EmailControllerApi.md#getrawemailjson) | **GET** /emails/{emailId}/raw/json | Get raw email in JSON
*EmailControllerApi* | [**getUnreadEmailCount**](Apis/EmailControllerApi.md#getunreademailcount) | **GET** /emails/unreadCount | Get unread email count
*EmailControllerApi* | [**validateEmail**](Apis/EmailControllerApi.md#validateemail) | **POST** /emails/{emailId}/validate | Validate email
*FormControllerApi* | [**submitForm**](Apis/FormControllerApi.md#submitform) | **POST** /forms | Submit a form to be parsed and sent as an email to an address determined by the form fields
*GroupControllerApi* | [**addContactsToGroup**](Apis/GroupControllerApi.md#addcontactstogroup) | **PUT** /groups/{groupId}/contacts | Add contacts to a group
*GroupControllerApi* | [**createGroup**](Apis/GroupControllerApi.md#creategroup) | **POST** /groups | Create a group
*GroupControllerApi* | [**deleteGroup**](Apis/GroupControllerApi.md#deletegroup) | **DELETE** /groups/{groupId} | Delete group
*GroupControllerApi* | [**getAllGroups**](Apis/GroupControllerApi.md#getallgroups) | **GET** /groups/paginated | Get all Contact Groups in paginated format
*GroupControllerApi* | [**getGroup**](Apis/GroupControllerApi.md#getgroup) | **GET** /groups/{groupId} | Get group
*GroupControllerApi* | [**getGroupWithContacts**](Apis/GroupControllerApi.md#getgroupwithcontacts) | **GET** /groups/{groupId}/contacts | Get group and contacts belonging to it
*GroupControllerApi* | [**getGroupWithContactsPaginated**](Apis/GroupControllerApi.md#getgroupwithcontactspaginated) | **GET** /groups/{groupId}/contacts-paginated | Get group and paginated contacts belonging to it
*GroupControllerApi* | [**getGroups**](Apis/GroupControllerApi.md#getgroups) | **GET** /groups | Get all groups
*GroupControllerApi* | [**removeContactsFromGroup**](Apis/GroupControllerApi.md#removecontactsfromgroup) | **DELETE** /groups/{groupId}/contacts | Remove contacts from a group
*InboxControllerApi* | [**createInbox**](Apis/InboxControllerApi.md#createinbox) | **POST** /inboxes | Create an Inbox (email address)
*InboxControllerApi* | [**deleteAllInboxes**](Apis/InboxControllerApi.md#deleteallinboxes) | **DELETE** /inboxes | Delete all inboxes
*InboxControllerApi* | [**deleteInbox**](Apis/InboxControllerApi.md#deleteinbox) | **DELETE** /inboxes/{inboxId} | Delete inbox
*InboxControllerApi* | [**getAllInboxes**](Apis/InboxControllerApi.md#getallinboxes) | **GET** /inboxes/paginated | List Inboxes Paginated
*InboxControllerApi* | [**getEmails**](Apis/InboxControllerApi.md#getemails) | **GET** /inboxes/{inboxId}/emails | Get emails in an Inbox
*InboxControllerApi* | [**getInbox**](Apis/InboxControllerApi.md#getinbox) | **GET** /inboxes/{inboxId} | Get Inbox
*InboxControllerApi* | [**getInboxEmailsPaginated**](Apis/InboxControllerApi.md#getinboxemailspaginated) | **GET** /inboxes/{inboxId}/emails/paginated | Get inbox emails paginated
*InboxControllerApi* | [**getInboxSentEmails**](Apis/InboxControllerApi.md#getinboxsentemails) | **GET** /inboxes/{inboxId}/sent | Get Inbox Sent Emails
*InboxControllerApi* | [**getInboxTags**](Apis/InboxControllerApi.md#getinboxtags) | **GET** /inboxes/tags | Get inbox tags
*InboxControllerApi* | [**getInboxes**](Apis/InboxControllerApi.md#getinboxes) | **GET** /inboxes | List Inboxes / Email Addresses
*InboxControllerApi* | [**sendEmail**](Apis/InboxControllerApi.md#sendemail) | **POST** /inboxes/{inboxId} | Send Email
*InboxControllerApi* | [**setInboxFavourited**](Apis/InboxControllerApi.md#setinboxfavourited) | **PUT** /inboxes/{inboxId}/favourite | Set inbox favourited state
*InboxControllerApi* | [**updateInbox**](Apis/InboxControllerApi.md#updateinbox) | **PATCH** /inboxes/{inboxId} | Update Inbox
*MailServerControllerApi* | [**describeMailServerDomain**](Apis/MailServerControllerApi.md#describemailserverdomain) | **POST** /mail-server/describe/domain | Get DNS Mail Server records for a domain
*MailServerControllerApi* | [**verifyEmailAddress**](Apis/MailServerControllerApi.md#verifyemailaddress) | **POST** /mail-server/verify/email-address | Verify the existence of an email address at a given mail server.
*SentEmailsControllerApi* | [**getSentEmail**](Apis/SentEmailsControllerApi.md#getsentemail) | **GET** /sent/{id} | Get sent email receipt
*SentEmailsControllerApi* | [**getSentEmails**](Apis/SentEmailsControllerApi.md#getsentemails) | **GET** /sent | Get all sent emails in paginated form
*TemplateControllerApi* | [**createTemplate**](Apis/TemplateControllerApi.md#createtemplate) | **POST** /templates | Create a Template
*TemplateControllerApi* | [**deleteTemplate**](Apis/TemplateControllerApi.md#deletetemplate) | **DELETE** /templates/{TemplateId} | Delete Template
*TemplateControllerApi* | [**getAllTemplates**](Apis/TemplateControllerApi.md#getalltemplates) | **GET** /templates/paginated | Get all Templates in paginated format
*TemplateControllerApi* | [**getTemplate**](Apis/TemplateControllerApi.md#gettemplate) | **GET** /templates/{TemplateId} | Get Template
*TemplateControllerApi* | [**getTemplates**](Apis/TemplateControllerApi.md#gettemplates) | **GET** /templates | Get all Templates
*WaitForControllerApi* | [**waitFor**](Apis/WaitForControllerApi.md#waitfor) | **POST** /waitFor | Wait for conditions to be met
*WaitForControllerApi* | [**waitForEmailCount**](Apis/WaitForControllerApi.md#waitforemailcount) | **GET** /waitForEmailCount | Wait for and return count number of emails 
*WaitForControllerApi* | [**waitForLatestEmail**](Apis/WaitForControllerApi.md#waitforlatestemail) | **GET** /waitForLatestEmail | Fetch inbox's latest email or if empty wait for an email to arrive
*WaitForControllerApi* | [**waitForMatchingEmail**](Apis/WaitForControllerApi.md#waitformatchingemail) | **POST** /waitForMatchingEmails | Wait or return list of emails that match simple matching patterns
*WaitForControllerApi* | [**waitForNthEmail**](Apis/WaitForControllerApi.md#waitfornthemail) | **GET** /waitForNthEmail | Wait for or fetch the email with a given index in the inbox specified
*WebhookControllerApi* | [**createWebhook**](Apis/WebhookControllerApi.md#createwebhook) | **POST** /inboxes/{inboxId}/webhooks | Attach a WebHook URL to an inbox
*WebhookControllerApi* | [**deleteWebhook**](Apis/WebhookControllerApi.md#deletewebhook) | **DELETE** /inboxes/{inboxId}/webhooks/{webhookId} | Delete and disable a Webhook for an Inbox
*WebhookControllerApi* | [**getAllWebhooks**](Apis/WebhookControllerApi.md#getallwebhooks) | **GET** /webhooks/paginated | List Webhooks Paginated
*WebhookControllerApi* | [**getWebhook**](Apis/WebhookControllerApi.md#getwebhook) | **GET** /webhooks/{webhookId} | Get a webhook for an Inbox
*WebhookControllerApi* | [**getWebhooks**](Apis/WebhookControllerApi.md#getwebhooks) | **GET** /inboxes/{inboxId}/webhooks | Get all Webhooks for an Inbox
*WebhookControllerApi* | [**sendTestData**](Apis/WebhookControllerApi.md#sendtestdata) | **POST** /webhooks/{webhookId}/test | Send webhook test data


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Alias](.//Models/Alias.md)
 - [AttachmentMetaData](.//Models/AttachmentMetaData.md)
 - [BasicAuthOptions](.//Models/BasicAuthOptions.md)
 - [BulkSendEmailOptions](.//Models/BulkSendEmailOptions.md)
 - [ContactDto](.//Models/ContactDto.md)
 - [ContactProjection](.//Models/ContactProjection.md)
 - [CreateAnonymousAliasOptions](.//Models/CreateAnonymousAliasOptions.md)
 - [CreateContactOptions](.//Models/CreateContactOptions.md)
 - [CreateDomainOptions](.//Models/CreateDomainOptions.md)
 - [CreateGroupOptions](.//Models/CreateGroupOptions.md)
 - [CreateOwnedAliasOptions](.//Models/CreateOwnedAliasOptions.md)
 - [CreateTemplateOptions](.//Models/CreateTemplateOptions.md)
 - [CreateWebhookOptions](.//Models/CreateWebhookOptions.md)
 - [DescribeDomainOptions](.//Models/DescribeDomainOptions.md)
 - [DescribeMailServerDomainResult](.//Models/DescribeMailServerDomainResult.md)
 - [DomainDto](.//Models/DomainDto.md)
 - [DomainPreview](.//Models/DomainPreview.md)
 - [Email](.//Models/Email.md)
 - [EmailAnalysis](.//Models/EmailAnalysis.md)
 - [EmailPreview](.//Models/EmailPreview.md)
 - [EmailProjection](.//Models/EmailProjection.md)
 - [EmailVerificationResult](.//Models/EmailVerificationResult.md)
 - [ForwardEmailOptions](.//Models/ForwardEmailOptions.md)
 - [GroupContactsDto](.//Models/GroupContactsDto.md)
 - [GroupDto](.//Models/GroupDto.md)
 - [GroupProjection](.//Models/GroupProjection.md)
 - [HTMLValidationResult](.//Models/HTMLValidationResult.md)
 - [Inbox](.//Models/Inbox.md)
 - [InboxProjection](.//Models/InboxProjection.md)
 - [MatchOption](.//Models/MatchOption.md)
 - [MatchOptions](.//Models/MatchOptions.md)
 - [NameServerRecord](.//Models/NameServerRecord.md)
 - [PageAlias](.//Models/PageAlias.md)
 - [PageContactProjection](.//Models/PageContactProjection.md)
 - [PageEmailPreview](.//Models/PageEmailPreview.md)
 - [PageEmailProjection](.//Models/PageEmailProjection.md)
 - [PageGroupProjection](.//Models/PageGroupProjection.md)
 - [PageInboxProjection](.//Models/PageInboxProjection.md)
 - [PageSentEmailProjection](.//Models/PageSentEmailProjection.md)
 - [PageTemplateProjection](.//Models/PageTemplateProjection.md)
 - [PageWebhookProjection](.//Models/PageWebhookProjection.md)
 - [Pageable](.//Models/Pageable.md)
 - [RawEmailJson](.//Models/RawEmailJson.md)
 - [SendEmailOptions](.//Models/SendEmailOptions.md)
 - [SentEmailDto](.//Models/SentEmailDto.md)
 - [SentEmailProjection](.//Models/SentEmailProjection.md)
 - [SetInboxFavouritedOptions](.//Models/SetInboxFavouritedOptions.md)
 - [SimpleSendEmailOptions](.//Models/SimpleSendEmailOptions.md)
 - [Sort](.//Models/Sort.md)
 - [TemplateDto](.//Models/TemplateDto.md)
 - [TemplateProjection](.//Models/TemplateProjection.md)
 - [TemplateVariable](.//Models/TemplateVariable.md)
 - [UnreadCount](.//Models/UnreadCount.md)
 - [UpdateGroupContacts](.//Models/UpdateGroupContacts.md)
 - [UpdateInboxOptions](.//Models/UpdateInboxOptions.md)
 - [UploadAttachmentOptions](.//Models/UploadAttachmentOptions.md)
 - [ValidationDto](.//Models/ValidationDto.md)
 - [ValidationMessage](.//Models/ValidationMessage.md)
 - [VerifyEmailAddressOptions](.//Models/VerifyEmailAddressOptions.md)
 - [WaitForConditions](.//Models/WaitForConditions.md)
 - [WebhookDto](.//Models/WebhookDto.md)
 - [WebhookProjection](.//Models/WebhookProjection.md)
 - [WebhookTestRequest](.//Models/WebhookTestRequest.md)
 - [WebhookTestResponse](.//Models/WebhookTestResponse.md)
 - [WebhookTestResult](.//Models/WebhookTestResult.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="API_KEY"></a>
### API_KEY

- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header

