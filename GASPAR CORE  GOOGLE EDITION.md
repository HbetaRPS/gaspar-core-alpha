\# GASPAR CORE | GOOGLE EDITION



MASTER DEVELOPMENT DIRECTIVE — CLAUDE FREE



La versión de Google debe conservar exactamente la misma filosofía de GASPAR CORE: una aplicación de escritorio propietaria, compilada, modular y extensible mediante plugins independientes.



La diferencia principal será que, en lugar de Microsoft Graph y Outlook, utilizará las APIs de Google para conectarse con Gmail.



No queremos construir una aplicación de Google Workspace llena de módulos. Queremos construir otra instancia del CORE, con conectividad real a Gmail y una arquitectura preparada para desarrollos independientes.



\# GASPAR CORE | GOOGLE



CORE ONLY



\[Gmail Ends POP3 and Gmailify Support from January 2026](https://images.openai.com/static-rsc-4/okdvMRCY6-WhD8RgvxA6Iiyk7NpCiQgmllTfYp4vMY31TdjuYt\_qYLiWBJ9CNq7PboPKy6de3CcEsj9eeAAzRmMZDhoa5-c3\_lpnwlndMjdIpbBeBQ9i0JbF\_nYEpufMw0m5GqbHekLHPmzaU-rTx3GT77CqEfrBm13diD2ryOw?purpose=inline)



Gmail API



Email infrastructure



\[Google Drive could soon start locking your files | TechRadar](https://images.openai.com/static-rsc-4/D8QJZtyXc17EBtRJYzWEDlNFjBd5jGxMuIAMOaV4aGkG2OYrd\_bMfDwrjMO5EjieqcgfBJE21-cMQaQvw0vfN9Tjm3zTICJLAoM5fOGA\_umFR\_8riflaR5z3npba68lpTU0R7WpH-0rDuGLP9AQe9\_Wj\_Gk2SamNG04R3UPqzZw?purpose=inline)



Google Workspace



Future-compatible infrastructure



Mismo producto conceptual, distinto proveedor de correo.



\## Diferencias técnicas importantes frente a Microsoft



Hay cuatro decisiones que Claude debe respetar:



1\\. Autenticación: Google utiliza OAuth 2.0 para aplicaciones de escritorio, con navegador externo, redirección local y PKCE. No debe implementar un login falso ni guardar contraseñas de Gmail.\&#x20;



\[image](https://www.google.com/s2/favicons?domain=https://developers.google.com\\\&sz=32)



Google for Developers







2\\. Permisos: Para leer mensajes completos, el alcance apropiado es `gmail.readonly`. Google lo clasifica como restringido, por lo que hay requisitos de verificación para distribuir públicamente la aplicación. Para desarrollo personal y pruebas existen excepciones sujetas a las condiciones de Google.\&#x20;



\[image](https://www.google.com/s2/favicons?domain=https://developers.google.com\\\&sz=32)



Google for Developers+1







3\\. Sincronización: Gmail dispone de `messages.list`, `messages.get` y `history.list`. La sincronización incremental debe aprovechar `historyId`, con sincronización completa de recuperación cuando el identificador haya expirado.\&#x20;



\[image](https://www.google.com/s2/favicons?domain=https://developers.google.com\\\&sz=32)



Google for Developers+2







4\\. Sincronización en tiempo real: Gmail admite notificaciones mediante `watch` y Google Cloud Pub/Sub, pero esto requiere infraestructura adicional. Queda fuera del MVP; comenzaremos con sincronización inicial e incremental.\&#x20;



\[image](https://www.google.com/s2/favicons?domain=https://developers.google.com\\\&sz=32)



Google for Developers







\# Instrucciones completas para Claude



\# GASPAR CORE — GOOGLE EDITION



\# MASTER DEVELOPMENT DIRECTIVE



\## PRIVATE MODULAR EMAIL PLATFORM — GMAIL CORE ONLY



\*\*PROJECT OWNER:\*\* Hamilton R. Betancourt\\

\*\*DEVELOPMENT AGENT:\*\* Claude\\

\*\*PROJECT DATE:\*\* November 19, 2026\\

\*\*TARGET:\*\* Windows 10 / Windows 11\\

\*\*DELIVERY:\*\* Compiled Windows Desktop Application\\

\*\*DEVELOPMENT ENVIRONMENT:\*\* Claude Free\\

\*\*PRIORITY:\*\* Complete, functional MVP TODAY\\

\*\*SCOPE:\*\* CORE FOUNDATION ONLY\\

\*\*EMAIL PROVIDER:\*\* GOOGLE GMAIL



\---



\# 00. EXECUTIVE MISSION



Develop GASPAR CORE — GOOGLE EDITION.



This is a proprietary Chromium-based Windows desktop application that connects to Google Gmail through the official Gmail API.



Its purpose is to establish a stable, extensible software foundation upon which developers can independently develop, install, update, and maintain custom plugins.



The intended development philosophy resembles Obsidian.



\- GASPAR CORE is the compiled desktop application.

\- Gmail provides the underlying email infrastructure.

\- The CORE provides the application runtime.

\- The CORE exposes a standardized, versioned API.

\- Plugins are independently developed.

\- Plugins can be installed, updated, enabled, disabled, and removed.

\- Plugin development does not require modifying CORE source code.

\- Plugin updates do not require recompiling GASPAR.exe.

\- The application remains functional without installed plugins.



The CORE must provide actual Gmail authentication, mailbox connectivity, message synchronization, persistent local storage, a usable desktop workspace, and a functioning plugin architecture.



\*\*YOU ARE BUILDING THE FOUNDATION, NOT THE FUTURE BUSINESS APPLICATIONS.\*\*



\# 01. MANDATORY SCOPE LOCK



This section is absolute and takes precedence over all other development suggestions.



\## 01.1 Authorized scope



You are authorized to implement ONLY:



1\. Windows desktop application.

2\. Chromium-based interface.

3\. Google OAuth 2.0 authentication.

4\. Gmail API connectivity.

5\. Gmail inbox synchronization.

6\. Local SQLite database.

7\. Basic email navigation and viewing.

8\. Standardized application API.

9\. Plugin host.

10\. Plugin manager.

11\. Basic plugin lifecycle management.

12\. Customizable workspace foundation.

13\. Basic themes and layouts.

14\. Developer SDK.

15\. Hello World demonstration plugin.

16\. Windows executable packaging.

17\. Required testing and documentation.



\## 01.2 Prohibited scope expansion



DO NOT develop:



\- Email merge systems.

\- Individualized email sending.

\- Custom MergeFields.

\- Attachment intelligence.

\- Attachment classification.

\- Excel reporting.

\- CASO ID extraction.

\- CRM systems.

\- Advanced contact management.

\- Contact-specific notes.

\- Automated note-taking.

\- RESA platform integration.

\- Automated RESA classification.

\- Automated notifications.

\- Advanced email automation.

\- Advanced smart folders.

\- Google Drive integration.

\- Google Calendar integration.

\- Google Docs integration.

\- Google Sheets integration.

\- Google Workspace automation.

\- Plugin marketplace.

\- Plugin hot-loading.

\- Advanced analytics.

\- Custom business workflows.

\- Additional applications.



These features are explicitly deferred.



Their potential usefulness does not authorize their implementation.



\## 01.3 Mandatory scope correction



If you identify an opportunity to implement a feature outside the authorized scope:



1\. STOP.

2\. Do not implement it.

3\. Do not spend resources designing it.

4\. Do not expand the architecture for speculative functionality.

5\. Return immediately to the unfinished CORE acceptance criteria.



Use this mandatory development instruction:



"STOP. This feature is outside the GASPAR CORE development scope. Return immediately to the current acceptance criteria and prioritize completing the compiled executable."



If a technical dependency genuinely prevents a CORE requirement from working, implement only the minimum necessary dependency.



\## 01.4 No unsolicited feature proposals



Do not interrupt development with proposals for future modules.



Do not repeatedly recommend additional integrations.



Do not replace implementation with architectural redesign.



Do not expand the assignment.



The objective is delivery.



\# 02. DEVELOPMENT STRATEGY



Claude Free resources are limited.



Complete the MVP using the simplest reliable architecture.



Requirements:



\- Prefer stable, established libraries.

\- Minimize dependencies.

\- Avoid unnecessary abstraction layers.

\- Avoid separate backend runtimes.

\- Avoid unnecessary services.

\- Avoid premature optimization.

\- Avoid excessive interface polishing.

\- Do not implement optional functionality.

\- Do not sacrifice the executable to build unnecessary infrastructure.



A functioning, compact implementation is preferable to an elaborate unfinished framework.



\# 03. TECHNOLOGY STACK



Use:



| Component            | Technology                          |

| -------------------- | ----------------------------------- |

| Desktop runtime      | Electron                            |

| Rendering            | Chromium                            |

| Frontend             | HTML / CSS / JavaScript             |

| Application logic    | TypeScript                          |

| Email infrastructure | Gmail API                           |

| Authentication       | Google OAuth 2.0                    |

| OAuth flow           | Desktop application + PKCE          |

| Google API client    | Official Google APIs Node.js client |

| Database             | SQLite                              |

| Configuration        | JSON                                |

| Plugin manifests     | JSON                                |

| Packaging            | Electron Builder                    |

| Operating system     | Windows 10 / 11                     |



Use one primary runtime.



Do not introduce a separate Python backend unless technically necessary.



Use compatible, stable package versions.



Commit the dependency lockfile.



\# 04. APPLICATION ARCHITECTURE



Maintain strict separation between CORE functionality and independently developed plugins.



Recommended structure:



GASPAR\_CORE\_GOOGLE/\\

|\\

+-- package.json\\

+-- package-lock.json\\

+-- electron-builder.yml\\

+-- tsconfig.json\\

+-- README.md\\

|\\

+-- src/\\

\\|   |\\

\\|   +-- main/\\

\\|   |   +-- main.ts\\

\\|   |   +-- application.ts\\

\\|   |   +-- window-manager.ts\\

\\|   |   +-- security.ts\\

\\|   |\\

\\|   +-- preload/\\

\\|   |   +-- preload.ts\\

\\|   |\\

\\|   +-- core/\\

\\|   |   +-- api/\\

\\|   |   +-- events/\\

\\|   |   +-- database/\\

\\|   |   +-- google/\\

\\|   |   +-- gmail/\\

\\|   |   +-- synchronization/\\

\\|   |   +-- plugins/\\

\\|   |   +-- configuration/\\

\\|   |\\

\\|   +-- renderer/\\

\\|       +-- index.html\\

\\|       +-- styles/\\

\\|       +-- scripts/\\

\\|       +-- components/\\

|\\

+-- plugins/\\

\\|   +-- hello-world/\\

|\\

+-- data/\\

|\\

+-- logs/\\

|\\

+-- SDK/\\

|\\

+-- tests/\\

|\\

+-- build/



Simplify this structure when appropriate.



Do not create unnecessary files or subsystems.



The essential requirement is separation between the compiled CORE and external plugin packages.



\# 05. GOOGLE CLOUD CONFIGURATION



Implement the application using an actual Google Cloud project and Gmail API.



The user will provide the required OAuth credentials.



Document the following configuration process:



1\. Access Google Cloud Console.

2\. Create a Google Cloud project.

3\. Enable Gmail API.

4\. Configure Google Auth Platform.

5\. Configure the OAuth consent screen.

6\. Select the appropriate audience.

7\. Add the user's Google account as a test user when applicable.

8\. Create an OAuth Client ID.

9\. Select Desktop application as the client type.

10\. Download the OAuth credentials JSON.

11\. Configure the application to locate the credentials securely.



Do not hardcode credentials.



Do not invent client IDs.



Do not invent client secrets.



Do not require the user to provide their Gmail password.



The application must be capable of operating once valid Google credentials have been configured.



\## 05.1 OAuth client architecture



Use the official Google OAuth 2.0 desktop application flow.



Requirements:



\- Open the user's default system browser.

\- Generate a PKCE code verifier and challenge.

\- Use a local loopback redirect listener.

\- Receive the authorization response.

\- Exchange the authorization code.

\- Acquire access and refresh tokens where granted.

\- Renew access tokens.

\- Handle denied authorization.

\- Handle expired or revoked credentials.



Desktop applications are public clients.



Do not rely on a bundled client secret being confidential.



Never expose authentication tokens to plugins.



Never store credentials inside plugin directories.



Reference:\\

\[https://developers.google.com/identity/protocols/oauth2/native-app](https://developers.google.com/identity/protocols/oauth2/native-app)



\# 06. GMAIL API AUTHENTICATION



Implement real Google authentication.



For the initial read-only email application, request:



\[https://www.googleapis.com/auth/gmail.readonly](https://www.googleapis.com/auth/gmail.readonly)



This permission is necessary for retrieving message contents and metadata.



Do not request:



\- gmail.modify

\- gmail.send

\- mail.google.com

\- Google Drive permissions.

\- Google Calendar permissions.

\- Google Sheets permissions.



The initial application does not send, delete, modify, or classify messages.



Use the minimum necessary authorization.



\## 06.1 Google verification considerations



Gmail readonly is classified as a restricted OAuth scope.



Document the implications:



\- Development and personal testing may qualify for applicable verification exceptions.

\- Testing-mode applications may require explicitly registered test users.

\- Public distribution may require Google verification.

\- Restricted-scope applications may have additional security assessment requirements depending on their architecture and use.



Do not attempt to bypass Google verification.



Do not claim that the application is publicly approved.



For this initial private development environment, prioritize a working authorized test configuration.



Reference:\\

\[https://developers.google.com/workspace/gmail/api/auth/scopes](https://developers.google.com/workspace/gmail/api/auth/scopes)



\# 07. GMAIL CONNECTOR



Implement the minimum necessary Gmail API services.



Required functionality:



\- Identify the authenticated Google account.

\- Retrieve the authenticated account's email address.

\- Retrieve Gmail inbox messages.

\- Retrieve message metadata.

\- Retrieve message headers.

\- Retrieve sender information.

\- Retrieve recipient information.

\- Retrieve subject.

\- Retrieve received timestamp.

\- Retrieve message body.

\- Retrieve message snippet.

\- Retrieve Gmail labels.

\- Retrieve conversation/thread identifiers.

\- Retrieve basic attachment metadata.



Use the official Gmail API.



Implement:



\- Pagination.

\- Request timeout handling.

\- Network recovery.

\- API error handling.

\- Rate-limit handling.

\- Authentication recovery.

\- Logging.



Do not simulate connectivity.



Do not use mock email records as proof of functionality.



\# 08. MASTER INBOX



The master inbox is the canonical local representation of synchronized Gmail messages.



Implement persistent SQLite storage.



Minimum message fields:



\- Internal record ID.

\- Gmail message ID.

\- Gmail thread ID.

\- Account email address.

\- Subject.

\- Sender.

\- Recipients.

\- Received timestamp.

\- Internal Gmail timestamp.

\- Snippet.

\- Body content or managed body reference.

\- Gmail label IDs.

\- Attachment indicator.

\- Synchronization timestamp.



Use Gmail's stable message identifiers.



Use the Gmail thread ID to retain the original conversation relationship.



Do not duplicate messages for individual interface views.



\## 08.1 Inbox behavior



Implement:



\- Inbox messages.

\- All locally synchronized messages.

\- Newest-first sorting.

\- Pagination.

\- Basic local search.

\- Message selection.

\- Message viewing.

\- Read/unread presentation.

\- Attachment indicators.

\- Persistent synchronization state.



Use Gmail's INBOX label to identify inbox messages.



Do not assume Gmail labels are equivalent to Outlook folders.



The local application views must be independent filters over the master repository.



Do not modify the user's Gmail mailbox merely to organize the local interface.



\# 09. MESSAGE RETRIEVAL



Use the appropriate Gmail endpoints:



\- users.messages.list

\- users.messages.get

\- users.threads.get

\- users.labels.list



Use messages.list to retrieve message identifiers.



Use messages.get to retrieve the necessary message content.



Request the appropriate message format.



Parse MIME content safely.



Support:



\- Plain text.

\- HTML body.

\- Multipart messages.

\- Common MIME headers.

\- Encoded message content.



For the MVP, display HTML email in a restricted viewer.



Do not execute arbitrary scripts contained in email HTML.



Sanitize untrusted message content.



Do not download or process attachments beyond basic metadata.



Attachment intelligence and downloading are deferred.



\# 10. INCREMENTAL SYNCHRONIZATION



Implement two synchronization modes.



\## 10.1 Initial synchronization



\- Retrieve Gmail inbox messages.

\- Follow pagination.

\- Retrieve the necessary message details.

\- Store messages in SQLite.

\- Record the latest available history identifier.

\- Preserve local data.



Avoid unnecessary duplicate retrieval.



\## 10.2 Incremental synchronization



Use Gmail's:



users.history.list



Use the stored historyId to retrieve changes since the previous synchronization.



Process:



\- New messages.

\- Deleted messages.

\- Relevant label changes.

\- Message changes needed to maintain local state.



Update the local database.



Persist the latest valid history identifier.



If Gmail returns HTTP 404 because the history identifier is no longer valid, perform a controlled full synchronization.



Do not discard the local database unnecessarily.



Use the official synchronization documentation:



\[https://developers.google.com/workspace/gmail/api/guides/sync](https://developers.google.com/workspace/gmail/api/guides/sync)



Do not implement Google Cloud Pub/Sub notifications or Gmail watch in this release.



A reliable initial and incremental synchronization process is sufficient.



\# 11. BASIC EMAIL WORKSPACE



Implement a functional Gmail-connected workspace.



\## LEFT SIDEBAR



\- INBOX

\- ALL MESSAGES

\- SEARCH

\- PLUGINS

\- SETTINGS



\## MESSAGE LIST



Display:



\- Sender.

\- Subject.

\- Preview.

\- Received date.

\- Read/unread indicator.

\- Attachment indicator.



\## MESSAGE VIEWER



Display:



\- Subject.

\- Sender.

\- Recipients.

\- Received date.

\- Message body.

\- Attachment metadata.



\## TOP TOOLBAR



Display:



\- Application identity.

\- Google account identity.

\- Connection status.

\- Synchronization status.

\- Workspace controls.



The initial application is read-only.



Do not implement sending, deleting, archiving, labeling, or modifying Gmail messages.



\# 12. PLUGIN ARCHITECTURE



The plugin system is a mandatory CORE capability.



The application must remain functional without plugins.



Plugins must be independent packages.



Implement:



\- Plugin discovery.

\- Manifest validation.

\- Local installation.

\- Activation.

\- Deactivation.

\- Removal.

\- Version identification.

\- CORE compatibility validation.

\- API compatibility validation.

\- Basic dependencies.

\- Permission declarations.

\- Plugin error logging.

\- Plugin lifecycle management.



Plugins load during application startup.



Restarting the application after plugin changes is acceptable.



Plugin hot-loading is explicitly deferred.



Updating a plugin must not require recompiling GASPAR.exe.



Do not embed future business logic into the compiled CORE.



Do not expose unrestricted Electron or Node.js privileges to plugins.



\# 13. STANDARDIZED PLUGIN API



Create a versioned application API.



The initial API must expose:



\- Application information.

\- Plugin information.

\- Notifications.

\- Logging.

\- Workspace panel registration.

\- Workspace tab registration.

\- Event subscriptions.

\- Plugin configuration.

\- Controlled Gmail mailbox access.

\- Controlled database services.



A conceptual interface:



interface GasparPlugin {\\

id: string;\\

version: string;



```

activate(api: GasparAPI): Promise<void>;



deactivate?(): Promise<void>;

```



}



The actual implementation may differ.



The API must be documented.



Plugins must not access Google OAuth tokens directly.



Plugins must not have unrestricted Gmail API access.



All privileged operations must pass through controlled CORE services.



For this release, expose read-only Gmail capabilities.



\# 14. PLUGIN MANIFEST



Use a standardized JSON manifest.



Example:



{\\

"id": "hello-world",\\

"name": "Hello World",\\

"version": "1.0.0",\\

"description": "GASPAR demonstration plugin",\\

"author": "Developer",\\

"main": "index.js",\\

"minimumCoreVersion": "1.0.0",\\

"apiVersion": "1.0",\\

"permissions": \[\\

"notifications"\\

]\\

}



Validate:



\- Manifest syntax.

\- Plugin ID.

\- Version.

\- Entry point.

\- API compatibility.

\- CORE compatibility.

\- Declared permissions.



Reject malformed packages.



\# 15. HELLO WORLD PLUGIN



Deliver one working demonstration plugin.



It must:



1\. Exist independently of CORE source.

2\. Be discoverable.

3\. Have a valid manifest.

4\. Install successfully.

5\. Activate successfully.

6\. Access the public plugin API.

7\. Display a Hello World notification or panel.

8\. Deactivate successfully.

9\. Uninstall successfully.



Modify the plugin's message or version.



Reinstall it.



Demonstrate that the updated plugin works without rebuilding GASPAR.exe.



Do not create additional demonstration business modules.



\# 16. CUSTOMIZABLE CHROMIUM WORKSPACE



Create a basic professional desktop interface.



Required:



\- Navigation sidebar.

\- Main workspace.

\- Tabs.

\- Basic panels.

\- Toolbar.

\- Plugin manager.

\- Settings.

\- Light theme.

\- Dark theme.

\- Persistent appearance preference.

\- Basic layout persistence.

\- Account status.

\- Synchronization status.



The workspace must support plugin-created panels and tabs through the standardized API.



Do not build a complete Obsidian clone.



Do not build an elaborate visual editor.



The objective is an extensible workspace foundation.



\# 17. DATABASE



Use SQLite.



Implement:



\- Database creation.

\- Database initialization.

\- Schema versioning.

\- Migrations.

\- Gmail message persistence.

\- Gmail synchronization state.

\- Account configuration.

\- Plugin registry.

\- Plugin configuration.



Keep plugin-owned data logically separate from internal CORE data.



Expose controlled database services.



Do not permit arbitrary modification of internal CORE tables.



\# 18. SECURITY



Implement:



\- Electron context isolation.

\- Renderer Node integration disabled.

\- Controlled preload bridge.

\- Content Security Policy.

\- Restricted navigation.

\- Controlled IPC.

\- Secure OAuth token storage.

\- Permission validation.

\- Plugin error isolation.

\- Authentication data protection.

\- HTML email sanitization.



Use Windows-supported secure storage where appropriate.



Do not store Google account passwords.



Do not expose tokens to plugins.



Do not include OAuth credentials or token files in the executable distribution.



Do not claim complete sandboxing unless implemented and tested.



Document known limitations.



\# 19. COMPILED WINDOWS DELIVERY



Use Electron Builder.



Generate a Windows distribution.



Deliver:



\- GASPAR CORE GOOGLE executable or installer.

\- Complete source code.

\- Dependency lockfile.

\- Build configuration.

\- Plugin SDK.

\- Hello World plugin.

\- Configuration example.

\- Google Cloud configuration guide.

\- Gmail authentication guide.

\- Installation instructions.

\- Reproducible build instructions.



The compiled application must operate outside the development environment.



Do not confuse development execution with compiled delivery.



\# 20. TESTING AND VERIFICATION



Execute actual tests.



Required:



TEST 1 — Application initialization.



TEST 2 — Window creation.



TEST 3 — Chromium interface.



TEST 4 — Database initialization.



TEST 5 — Database persistence.



TEST 6 — OAuth flow.



TEST 7 — Actual Google account authentication.



TEST 8 — Actual Gmail API connection.



TEST 9 — Initial inbox synchronization.



TEST 10 — Message retrieval.



TEST 11 — Local persistence.



TEST 12 — Incremental synchronization.



TEST 13 — Restart and persistence verification.



TEST 14 — Plugin discovery.



TEST 15 — Plugin installation.



TEST 16 — Plugin activation.



TEST 17 — Plugin deactivation.



TEST 18 — Plugin removal.



TEST 19 — Independent plugin update.



TEST 20 — Windows executable build.



TEST 21 — Compiled application launch.



Report each test as:



\- PASS — executed and successful.

\- FAIL — executed and unsuccessful.

\- BLOCKED — external configuration or dependency unavailable.

\- NOT TESTED — not executed.



Never claim a successful Google authentication without an actual authenticated request.



Never claim Gmail synchronization works using mock data.



If credentials are unavailable, implement the real authentication flow and clearly identify live verification as pending user configuration.



\# 21. DEVELOPMENT PRIORITY



Follow this exact order:



PRIORITY 1 — Electron application and Chromium GUI.



PRIORITY 2 — SQLite initialization.



PRIORITY 3 — Google OAuth implementation.



PRIORITY 4 — Actual Gmail API connectivity.



PRIORITY 5 — Initial message synchronization.



PRIORITY 6 — Local message persistence.



PRIORITY 7 — Incremental synchronization.



PRIORITY 8 — Basic email workspace.



PRIORITY 9 — Plugin host.



PRIORITY 10 — Plugin manager.



PRIORITY 11 — Hello World plugin.



PRIORITY 12 — Windows executable compilation.



PRIORITY 13 — Acceptance testing.



PRIORITY 14 — Final delivery and documentation.



Do not reorder priorities to pursue optional improvements.



\# 22. DEFERRED FUNCTIONALITY



The following are outside this release:



\- Email merge.

\- Individualized sending.

\- Attachment reporting.

\- Excel integration.

\- CASO ID extraction.

\- Contact-centric communications.

\- CRM.

\- RESA integration.

\- Automated classification.

\- Automated notes.

\- Automated notifications.

\- Google Drive.

\- Google Calendar.

\- Google Sheets.

\- Google Docs.

\- Advanced automation.

\- Plugin marketplace.

\- Plugin hot-loading.

\- Advanced workspace customization.



These may be developed independently after the CORE is delivered.



Do not implement them now.



\# 23. MANDATORY DELIVERY REPORT



At completion, provide:



APPLICATION:



\- Product name.

\- Version.

\- Build date.

\- Technology stack.



DELIVERY:



\- Executable location.

\- Installer location, if generated.

\- Source location.

\- SDK location.

\- Plugin location.



FUNCTIONALITY:



\- Implemented features.

\- Features requiring user configuration.

\- Deferred features.



TESTING:



\- Actual test results.

\- PASS / FAIL / BLOCKED / NOT TESTED.

\- Runtime verification.

\- Google OAuth verification.

\- Gmail synchronization verification.

\- Build verification.



LIMITATIONS:



\- Outstanding issues.

\- Required Google Cloud configuration.

\- OAuth verification limitations.

\- Known compatibility issues.

\- Security limitations.



Do not invent paths.



Do not claim files exist without verifying them.



Do not claim functionality that was not implemented.



\# 24. FINAL AND ABSOLUTE DEVELOPMENT DIRECTIVE



You are not authorized to expand the project scope.



You are not authorized to develop future business modules.



You are not authorized to replace the immediate delivery objective with additional architectural proposals.



If you identify an opportunity to expand functionality, IGNORE IT.



If you begin designing a future module, STOP.



If you identify a feature that is not necessary for the acceptance criteria, DEFER IT.



If a technical obstacle appears, solve only what is necessary to complete the CORE.



If resources become constrained, simplify implementation rather than expanding the project.



The only authorized objective is:



DELIVER A FUNCTIONING, COMPILED WINDOWS APPLICATION THAT AUTHENTICATES WITH GOOGLE, CONNECTS TO GMAIL, SYNCHRONIZES EMAIL, STORES DATA, AND PROVIDES A WORKING FOUNDATION FOR INDEPENDENT PLUGIN DEVELOPMENT.



The CORE must be independent.



The Gmail connection must work.



The plugin architecture must work.



The executable must be delivered.



NO SCOPE EXPANSION.



NO BUSINESS MODULES.



NO UNNECESSARY COMPLEXITY.



FINISH THE GOOGLE CORE TODAY.



\## Configuración que tendrás que realizar en Google



\[File:Google Cloud Console logo.png - Wikimedia Commons](https://images.openai.com/static-rsc-4/oCpJF9oc0TimdPI1mgArhSmYtvWRPlzh1vVotja2GQSmwKqYHg0o7SMg-ooJs1Fh1kyEIOzMCNm02foaAriKytXaMl9BbF-\_9H-CxxxMaY9tdHDQdjNJZ0ZqCtgGE7j\_jIx5Er3Udc5KWPYGTuehEZWOVCCYojTyT5uZ8ByvmRU?purpose=inline)



Google Cloud Console



1\. \[Abrir Google Cloud Console](https://console.cloud.google.com/?utm\_source=chatgpt.com).

2\. Crear un proyecto GASPAR CORE GOOGLE.

3\. Activar Gmail API.

4\. Configurar Google Auth Platform y la pantalla de consentimiento.

5\. Añadir tu cuenta como usuario de prueba cuando corresponda.

6\. Crear OAuth Client ID de tipo Desktop App.

7\. Descargar el archivo de credenciales JSON.



&#x20;  \[Harga gmail Terbaru Sep 2025 | BigGo Indonesia](https://images.openai.com/static-rsc-4/xffW511H-NU3nqbvxpNuKu6vtZ38PUMiZAbFwuqB9xscbLsNshiRW-neCF5cYPZghj4zawMVw4jyImEjpW0NQr41SIcGiU23BV2M2rnh4BKUW7PldvIEeLjfgiGnmmz2Vy0mUzJEvstZDHLMboTH\_8dAZ0TzSVsvoB276OkU7jU?purpose=inline)



&#x20;  Gmail API



&#x20;  \[Documentación oficial de Gmail API](https://developers.google.com/workspace/gmail/api?utm\_source=chatgpt.com)\[OAuth para aplicaciones de escritorio](https://developers.google.com/identity/protocols/oauth2/native-app?utm\_source=chatgpt.com)



Nota: El permiso `gmail.readonly` es restringido. Una aplicación privada de pruebas puede estar sujeta a excepciones, pero no debe asumirse que cualquier distribución pública estará autorizada automáticamente.\&#x20;



\[image](https://www.google.com/s2/favicons?domain=https://developers.google.com\\\&sz=32)



Google for Developers+1







\## Resultado esperado



GASPAR CORE — OUTLOOK



Microsoft Graph



GASPAR CORE — GOOGLE



Gmail API



Mi recomendación arquitectónica es mantener ambas ediciones como productos independientes, pero con una filosofía de plugins equivalente. No intentes fusionarlas hoy ni crear una tercera capa de abstracción compartida: primero entrega y valida cada CORE.



Así tendrás dos aplicaciones compiladas, dos conexiones reales y dos plataformas preparadas para recibir desarrollos independientes.

