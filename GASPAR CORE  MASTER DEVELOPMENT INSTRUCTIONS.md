\# GASPAR CORE | MASTER DEVELOPMENT SPECIFICATION







SCOPE LOCKED



CLAUDE FREE



COMPILED MVP TODAY







This is the consolidated, complete development assignment. The scope-control rules are integrated into the instructions themselves. Claude must not treat them as optional recommendations.



\# GASPAR CORE



\# MASTER DEVELOPMENT DIRECTIVE



\## PRIVATE MODULAR EMAIL PLATFORM — CORE ONLY



\*\*PROJECT OWNER:\*\* Hamilton R. Betancourt\\

\*\*DEVELOPMENT AGENT:\*\* Claude\\

\*\*PROJECT DATE:\*\* November 19, 2026\\

\*\*TARGET:\*\* Windows 10 / Windows 11\\

\*\*DELIVERY:\*\* Compiled Windows Desktop Application\\

\*\*DEVELOPMENT ENVIRONMENT:\*\* Claude Free\\

\*\*PRIORITY:\*\* Complete, functional MVP TODAY\\

\*\*SCOPE:\*\* CORE FOUNDATION ONLY



\---



\# 00. EXECUTIVE MISSION



Develop GASPAR CORE: a proprietary, Chromium-based Windows desktop application that connects to Microsoft Outlook through Microsoft Graph.



The application establishes a permanent, extensible software foundation for future independently developed plugins.



The intended development philosophy resembles Obsidian:



\- The CORE is the compiled desktop application.

\- The CORE provides the application runtime and standardized API.

\- Plugins are independently developed.

\- Plugins can be installed, updated, enabled, and disabled.

\- Plugin development does not require modifying CORE source code.

\- Plugin updates do not require recompiling the CORE executable.

\- The application remains functional without installed plugins.



The CORE must provide actual Outlook connectivity, message synchronization, persistent local storage, a usable desktop workspace, and a working plugin architecture.



\*\*You are building the foundation, not the future business applications.\*\*



\# 01. MANDATORY SCOPE LOCK



This section is an absolute development restriction and takes precedence over any suggestion, opportunity, or feature idea encountered during implementation.



\## 01.1 Authorized scope



You are authorized to implement ONLY:



1\. Windows desktop runtime.

2\. Chromium-based interface.

3\. Microsoft Graph authentication.

4\. Outlook mailbox connection.

5\. Master inbox synchronization.

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



You MUST NOT develop:



\- Email merge systems.

\- Individualized email sending.

\- Custom MergeFields.

\- Attachment intelligence.

\- Attachment classification.

\- Excel reporting.

\- CASO ID extraction.

\- Contact-centric CRM.

\- Contact-specific notes.

\- Automated note-taking.

\- RESA platform integration.

\- RESA classification.

\- LITIGIO or PARALIZACION classification.

\- RIESGO DE DEMANDA workflows.

\- Advanced email automation.

\- Advanced smart folders.

\- Plugin marketplaces.

\- Plugin hot-loading.

\- Advanced analytics.

\- Custom business workflows.

\- Additional applications.

\- Future business modules.



These are explicitly outside the current development authorization.



Their usefulness does not justify their implementation.



\## 01.3 Mandatory scope correction



If you identify a feature that is outside the authorized scope:



1\. Do not implement it.

2\. Do not spend time designing it.

3\. Do not expand the architecture to accommodate speculative requirements.

4\. Continue with the next unfinished CORE acceptance criterion.



Use this mandatory internal development directive:



"STOP. This feature is outside the GASPAR CORE development scope. Return immediately to the current acceptance criteria and prioritize completing the compiled executable."



If you encounter a technical dependency that genuinely prevents a CORE requirement from working, address only the minimum necessary dependency.



Do not use dependencies as justification for introducing unrelated functionality.



\## 01.4 No unsolicited feature proposals



Do not repeatedly recommend future modules during development.



Do not interrupt implementation to suggest additional capabilities.



Do not replace completed development work with architectural redesigns.



Maintain a concise record of deferred ideas only when necessary, without implementing them.



The immediate objective is delivery.



\# 02. DEVELOPMENT STRATEGY



The development environment has limited resources.



Use a focused MVP implementation strategy.



Rules:



\- Prefer existing stable libraries.

\- Minimize dependencies.

\- Avoid unnecessary abstraction.

\- Avoid multiple backend runtimes.

\- Avoid unnecessary services.

\- Avoid premature optimization.

\- Avoid unnecessary visual sophistication.

\- Do not implement optional features before mandatory requirements.

\- Do not spend excessive time generating architectural documentation instead of working software.



A simple, functioning implementation is preferable to an elaborate unfinished framework.



\# 03. TECHNOLOGY STACK



Use the following preferred stack:



| Component             | Technology                       |

| --------------------- | -------------------------------- |

| Desktop runtime       | Electron                         |

| Rendering             | Chromium                         |

| Frontend              | HTML / CSS / JavaScript          |

| Application logic     | TypeScript                       |

| Database              | SQLite                           |

| Microsoft integration | Microsoft Graph API              |

| Authentication        | Microsoft Authentication Library |

| Configuration         | JSON                             |

| Plugin manifests      | JSON                             |

| Packaging             | Electron Builder                 |

| Operating system      | Windows 10 / 11                  |



Use a single primary runtime.



Do not introduce a separate Python backend unless an essential technical requirement makes it necessary.



Select stable compatible package versions and commit the dependency lockfile.



\# 04. APPLICATION ARCHITECTURE



Maintain strict separation between CORE functionality and independently developed plugins.



Recommended structure:



GASPAR\_CORE/\\

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

\\|   |   +-- graph/\\

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



This structure is a starting point.



Simplify wherever appropriate.



Do not create files or subsystems without a concrete purpose.



The essential requirement is separation of the compiled CORE from external plugin packages.



\# 05. MICROSOFT GRAPH AUTHENTICATION



Implement actual Microsoft Graph authentication.



Use a Microsoft application registration configured by the user.



Support delegated authentication with only the permissions needed for the MVP.



Expected permissions:



\- User.Read

\- Mail.Read

\- offline\_access, where supported by the chosen authentication flow.



Do not request Mail.ReadWrite unless actual implemented functionality requires it.



Implement:



1\. Microsoft sign-in.

2\. Token acquisition.

3\. Token renewal.

4\. Account identification.

5\. Mailbox connection.

6\. Connection status.

7\. Authentication error handling.

8\. Secure token storage.



Use MSAL and Microsoft Graph.



Do not hardcode client secrets or credentials.



Do not expose access tokens to plugins.



Do not log authentication tokens.



The application must distinguish:



\- Not configured.

\- Not authenticated.

\- Authenticating.

\- Connected.

\- Synchronizing.

\- Connection interrupted.

\- Authentication expired.

\- Error.



A connection must only be marked successful after an actual authenticated Graph request succeeds.



If the user has not configured Azure credentials, deliver the real authentication implementation and provide setup instructions. Do not substitute simulated authentication.



\# 06. OUTLOOK CONNECTOR



Implement all necessary Graph services.



Required:



\- Identify authenticated mailbox.

\- Retrieve inbox messages.

\- Retrieve message metadata.

\- Retrieve message body.

\- Retrieve sender and recipient information.

\- Retrieve conversation IDs.

\- Retrieve received timestamps.

\- Retrieve attachment indicators and basic attachment metadata.

\- Handle pagination.

\- Handle network interruptions.

\- Handle Graph throttling.

\- Handle expired tokens.



Implement incremental synchronization using Microsoft Graph delta queries where supported.



Persist the necessary synchronization cursor.



Do not repeatedly download the entire mailbox when incremental synchronization is available.



If subscriptions and webhook notifications cannot be implemented reliably within the MVP, defer them.



Reliable initial synchronization and incremental synchronization take priority.



\# 07. MASTER INBOX



The master inbox is the canonical local representation of synchronized Outlook messages.



Implement SQLite persistence.



Minimum message fields:



\- Internal ID.

\- Graph message ID.

\- Immutable Graph message ID where supported.

\- Mailbox ID.

\- Conversation ID.

\- Subject.

\- Sender.

\- Recipients.

\- Received date.

\- Sent date.

\- Preview.

\- Body content or managed body reference.

\- Read/unread state.

\- Attachment indicator.

\- Synchronization timestamp.



Implement:



\- Newest-first sorting.

\- Pagination.

\- Basic search.

\- Message selection.

\- Message viewer.

\- Read/unread presentation.

\- Persistent synchronization metadata.



Do not duplicate messages for different interface views.



The database must survive application restarts.



\# 08. BASIC EMAIL WORKSPACE



Implement only the basic email functionality necessary to demonstrate that GASPAR CORE is a working connected email platform.



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



\## TOOLBAR



Display:



\- Application identity.

\- Account identity.

\- Connection status.

\- Synchronization status.

\- Workspace controls.



Do not implement advanced email management features.



\# 09. PLUGIN ARCHITECTURE



The plugin system is a mandatory CORE capability.



The application must operate independently of installed plugins.



Plugins must be independently developed packages.



Implement:



\- Plugin discovery.

\- Manifest validation.

\- Local plugin installation.

\- Plugin activation.

\- Plugin deactivation.

\- Plugin removal.

\- Version identification.

\- CORE compatibility verification.

\- API compatibility verification.

\- Basic dependency declarations.

\- Permission declarations.

\- Plugin error handling.

\- Plugin logging.



Plugins load during application startup.



Application restart after plugin installation or modification is acceptable.



\*\*Plugin hot-loading is explicitly deferred.\*\*



Updating a plugin must not require recompiling GASPAR.exe.



Do not place future business logic inside the compiled application.



Do not expose unrestricted Electron or Node.js privileges to plugins.



Use a controlled execution environment and a restricted public API.



\# 10. STANDARDIZED PLUGIN API



Create a versioned application API.



Initial API capabilities:



\- Application information.

\- Plugin metadata.

\- Notifications.

\- Logging.

\- Workspace panel registration.

\- Workspace tab registration.

\- Application event subscriptions.

\- Plugin configuration.

\- Controlled mailbox access.

\- Controlled database services.



Use an interface conceptually similar to:



interface GasparPlugin {\\

id: string;\\

version: string;



```

activate(api: GasparAPI): Promise<void>;



deactivate?(): Promise<void>;

```



}



The actual implementation may vary.



The API must be documented.



The API must not expose unrestricted access to privileged processes.



Do not expose authentication tokens.



Do not permit plugins to directly modify internal CORE database tables.



All privileged functionality must be mediated by the CORE.



\# 11. PLUGIN MANIFEST



Implement a standardized JSON manifest.



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



Reject invalid packages.



\# 12. HELLO WORLD PLUGIN



Deliver one working plugin.



Its only purpose is to demonstrate the plugin architecture.



It must:



1\. Be stored independently of the CORE source.

2\. Be discoverable by the plugin manager.

3\. Have a valid manifest.

4\. Install successfully.

5\. Activate successfully.

6\. Access the public plugin API.

7\. Display a Hello World notification or panel.

8\. Deactivate successfully.

9\. Uninstall successfully.



Demonstrate an independent plugin update.



Modify the plugin's message or version, reinstall it, and verify that the change works without rebuilding GASPAR.exe.



Do not add additional sample business plugins.



\# 13. CUSTOMIZABLE CHROMIUM GUI



Create a basic professional desktop workspace.



Required:



\- Navigation sidebar.

\- Main workspace.

\- Tabs.

\- Basic panel architecture.

\- Toolbar.

\- Plugin manager.

\- Settings.

\- Light theme.

\- Dark theme.

\- Persistent appearance selection.

\- Basic layout persistence.

\- Account status.

\- Synchronization status.



The workspace must support plugin-created panels and tabs through the public API.



Do not build a complete Obsidian clone.



Do not build an elaborate visual layout editor.



The objective is a usable and extensible interface foundation.



\# 14. DATABASE



Use SQLite.



Implement:



\- Database creation.

\- Database initialization.

\- Schema versioning.

\- Migrations.

\- Message persistence.

\- Synchronization state.

\- Application configuration.

\- Plugin registry.

\- Plugin configuration.



Keep plugin-owned data logically separate from internal CORE data.



Expose controlled database services.



Do not permit arbitrary modification of internal database structures.



\# 15. APPLICATION SECURITY



Implement:



\- Electron context isolation.

\- Renderer Node integration disabled.

\- Controlled preload bridge.

\- Content Security Policy.

\- Restricted navigation.

\- Controlled IPC.

\- Secure token storage.

\- Permission verification.

\- Plugin error isolation.

\- Authentication data protection.



Do not claim complete sandboxing unless the actual implementation supports it.



Document known limitations.



\# 16. COMPILED WINDOWS DELIVERY



Use Electron Builder.



Generate a Windows distribution.



The application must run outside the development environment.



Deliver:



\- GASPAR CORE executable or installer.

\- Complete source code.

\- Dependency lockfile.

\- Build configuration.

\- Plugin SDK.

\- Hello World plugin.

\- Configuration example.

\- Microsoft Graph setup guide.

\- Installation instructions.

\- Reproducible build instructions.



The compiled application must not depend on the developer's source directory or IDE.



Do not confuse development execution with compiled delivery.



\# 17. TESTING AND VERIFICATION



Execute actual tests.



Required:



1\. Application initialization.

2\. Window creation.

3\. Database initialization.

4\. Database persistence.

5\. Authentication flow.

6\. Actual Graph connection.

7\. Inbox synchronization.

8\. Message retrieval.

9\. Local persistence.

10\. Restart verification.

11\. Plugin discovery.

12\. Plugin installation.

13\. Plugin activation.

14\. Plugin deactivation.

15\. Plugin removal.

16\. Independent plugin update.

17\. Windows build.

18\. Compiled application launch.



Report each test as:



\- PASS — executed and successful.

\- FAIL — executed and unsuccessful.

\- BLOCKED — external requirement unavailable.

\- NOT TESTED — not executed.



Never claim a successful live Graph connection without an authenticated request.



Never claim a compiled executable was tested if only the development version was launched.



\# 18. DEVELOPMENT PRIORITY



Follow this exact order:



PRIORITY 1 — Establish the Electron application and Chromium GUI.



PRIORITY 2 — Initialize SQLite.



PRIORITY 3 — Implement Microsoft authentication.



PRIORITY 4 — Establish actual Graph connectivity.



PRIORITY 5 — Synchronize real Outlook messages.



PRIORITY 6 — Persist messages locally.



PRIORITY 7 — Implement the basic email workspace.



PRIORITY 8 — Implement the plugin host.



PRIORITY 9 — Implement the plugin manager.



PRIORITY 10 — Implement Hello World.



PRIORITY 11 — Compile the Windows application.



PRIORITY 12 — Execute acceptance tests.



PRIORITY 13 — Deliver source, executable, documentation, and test report.



Do not reorder priorities to pursue optional improvements.



\# 19. DEFERRED FUNCTIONALITY



The following are not part of this release:



\- Email merge.

\- Attachment reporting.

\- Excel integrations.

\- CASO ID extraction.

\- Contact-centric communications.

\- Advanced contact management.

\- CRM.

\- RESA.

\- Automated case classification.

\- Automated notes.

\- Automated email notifications.

\- Advanced workflow automation.

\- Plugin marketplace.

\- Hot-loading.

\- Advanced customization tools.



They may be developed independently after the CORE is delivered.



Do not implement them.



\# 20. MANDATORY DELIVERY REPORT



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

\- Graph verification.

\- Build verification.



LIMITATIONS:



\- Outstanding issues.

\- Required Microsoft configuration.

\- Known compatibility limitations.

\- Security limitations.



Do not invent paths or claim files exist without verifying them.



Do not claim functionality that was not implemented.



\# 21. FINAL AND ABSOLUTE DEVELOPMENT DIRECTIVE



You are not authorized to expand the project scope.



You are not authorized to develop future business modules.



You are not authorized to replace the immediate delivery objective with additional architecture proposals.



If you encounter an opportunity to expand functionality, IGNORE IT.



If you begin designing a future module, STOP.



If you identify a feature that is not necessary for the acceptance criteria, DEFER IT.



If a technical obstacle appears, solve only what is necessary to complete the CORE.



If resources become constrained, simplify implementation rather than expanding the project.



The only authorized objective is:



DELIVER A FUNCTIONING, COMPILED WINDOWS APPLICATION THAT CONNECTS TO OUTLOOK, SYNCHRONIZES EMAIL, STORES DATA, AND PROVIDES A WORKING FOUNDATION FOR INDEPENDENT PLUGIN DEVELOPMENT.



The CORE must be independent.



The plugin architecture must work.



The executable must be delivered.



\*\*NO SCOPE EXPANSION.\*\*



\*\*NO BUSINESS MODULES.\*\*



\*\*NO UNNECESSARY COMPLEXITY.\*\*



\*\*FINISH THE CORE TODAY.\*\*



\## Final operating rule



If Claude reaches a point where it wants to expand the project, the scope lock in section 01 overrides that impulse. If it encounters a genuine technical blocker, it should report the blocker and continue with everything else that can be completed.



The acceptance target is three things working together:



1\. Outlook connection and real message synchronization.

2\. A compiled, usable GASPAR desktop application.

3\. A plugin system that demonstrably works independently of the executable.



Everything else is deferred.

