[Home](/) - [Getting Started](/getting-started) - [Developers](/developers)

## Getting Started

To begin using DebitDirect you require to have development skills integrating to json/rest based services. DebitDirect can only be integrated as an API and does not offer interface based managemeent. You need to have tools and knowledge of handling webhooks, API integration and master your development language of choice. DebitDirect does offer Swagger documentation of our API, and NuGet packages for Microsoft .NET Framework.

To start testing DebitDirect, sign up for an account. All sign up begin with a 30 day trial period.

Upon obtaining your account, you will receive your initial API token. Please keep this token securely and **DO NOT SHARE THIS EXTERNALLY**.

Any merchant trial is running in test mode. No real payments are processed, however mandates may or may not be processed against the scheme. When you are ready to go live, please ensure to sign a merchant agreement with the scheme provider at least 7 days before and once completed, activate your DebitDirect merchant account (see API).

### Supported schemes
DebitDirect support NETS LeverandørService (NETS-LS).

#### NETS - LeverandørService (NETS-LS)

LeverandørService is a B2B only payment service. LeverandørService offer businesses to debit and credit payments using instructed mandates. 

**Mandates.** Mandates are controlled and offered by end-customers either by signing up using a web form provided by NETS, by signing up using their bank or by using the DebitDirect API to initiate a mandate. Mandates may be revoked by end-customers either directly to the merchant, by managing a merchant agreement using the NETS [LeverandørService portal](https://leverandoerservice.nets.eu) or by contacting the merchant bank.

**Getting a Merchant Agreement with Nets.** Follow [this link](https://leverandoerservice.nets.eu/) to begin requesting an agreement with Nets. Complete the agreement, and provide the following number when selecting an external data provider to handle the Nets settlements and integration: 38558862. Completing this step, will enable enable the legal agreement under which DebitDirect can process payments and settlements - including completing a full flow test.

**More information.** Read more about [LeverandørService here](https://www.nets.eu/dk-da/l%C3%B8sninger/Fakturering%20og%20opkr%C3%A6vning/Leverand%C3%B8rservice).
