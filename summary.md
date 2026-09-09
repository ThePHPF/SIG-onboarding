# ShiPHP It

*A feature-first builder's guide to Laravel, Symfony, WordPress, TYPO3, API Platform, Nextcloud, and the rest of the modern PHP ecosystem*

## Who this is for

You're not here for the language. You have a feature to ship, a client waiting, or a deadline that doesn't care what's running on the server. This book assumes you already know how to code and just need to know: *what's the fastest, least-regrettable way to ship this specific thing?*

Every chapter is a feature you might be asked to build, not a piece of syntax. Each one walks through two to four real ecosystems that can ship it, roughly ordered from "fastest to a demo" to "best fit if this needs to last." Pick the one that matches your stack, your client, or your curiosity, and skip the rest.

A short **"Under the hood"** box closes most sections. It's optional, always skippable, and exists for one reason: the engine underneath all of this has gotten genuinely good, and if you ever want to know *why* a one-line attribute or a `readonly` property is doing so much work for you, that box tells you in thirty seconds. If you never open one of these boxes, you will still finish this book able to ship.

This book doesn't care about license purity, only about the fastest honest path to shipping. That means a few names here are paid products or SaaS, not open source, because they're genuinely the pragmatic choice for that feature. Every one of them is marked with a **`$`** right in its title, so you know before you commit a client's budget to it, and there's always at least one open-source path sitting next to it in the same chapter.

---

[Ship It](title-page.md)
[Foreword: You Don't Need to Love the Engine to Drive the Car](foreword.md)
[How This Book Works](ch00-00-how-this-book-works.md)

- [Choosing Your Stack in Five Minutes](ch01-00-choosing-your-stack.md)
  *Framework, CMS, or headless API? A decision guide, not a religion.*
  - [Framework, CMS, or Headless: What Are You Actually Building?](ch01-01-framework-cms-or-headless.md)
  - [Scaffolding a First Project in Under a Minute](ch01-02-scaffolding-a-first-project.md)
    *Laravel (`laravel new`), Symfony (`symfony new`), WordPress (`wp core download` / Local), API Platform (`composer create-project`)*

- [Shipping Without a Framework: Standalone Components](ch02-00-standalone-components.md)
  *Sometimes the fastest way to ship isn't picking a framework at all, it's `composer require`-ing the one library built for exactly this job. Every package below is genuinely independent: no framework underneath, nothing to configure beyond the one thing it does.*
  - [Command-Line Tools: Symfony/Console](ch02-01-symfony-console-standalone.md)
    *The same component that runs Composer itself and powers Laravel's Artisan commands, used completely on its own for an import script, a cron job, or an internal tool. No Symfony framework required.*
  - [Talking to Other APIs: Guzzle](ch02-02-guzzle-http-client.md)
    *A dependency-light HTTP client for calling third-party APIs from any script, with no framework in the request path.*
  - [Templating Without a Framework: League/Plates](ch02-03-league-plates-standalone.md)
    *Native-PHP templating with layouts and escaping, for whenever you need safe, reusable HTML output and nothing else attached.*
  - [Logging That Just Works: Monolog](ch02-04-monolog-standalone.md)
    *The de facto PSR-3 logger almost every framework wraps internally, wired up directly with zero framework overhead.*
  - [Validating Input: Respect/Validation](ch02-05-respect-validation.md)
    *Readable, chainable validation rules for a form or an API payload, with nothing else attached.*
  - [File Storage Without Buying Into a Framework: League/Flysystem](ch02-06-league-flysystem-standalone.md)
    *The same abstraction Laravel's Storage facade is built on, used directly to read and write local disks, S3, or FTP from any script.*

- [Shipping a Content Site](ch03-00-shipping-a-content-site.md)
  *Marketing pages, blogs, and editor-friendly sites that don't need custom app logic.*
  - [WordPress: Block Themes and the Site Editor](ch03-01-wordpress-block-themes.md)
  - [TYPO3: Structured Content at Enterprise Scale](ch03-02-typo3-structured-content.md)
  - [Statamic ($ for commercial use): A Flat-File CMS Built on Laravel](ch03-03-statamic-flat-file-cms.md)
  - [Craft CMS ($): A Licensed CMS Built for Editorial Control](ch03-04-craft-cms.md)

- [Shipping User Accounts](ch04-00-shipping-user-accounts.md)
  *Sign-up, login, password resets, and "who is this person" without writing auth from scratch.*
  - [Laravel: Breeze, Fortify, and Jetstream](ch04-01-laravel-breeze-fortify.md)
  - [Symfony: The Security Bundle](ch04-02-symfony-security-bundle.md)
  - [WordPress: Roles, Capabilities, and Application Passwords](ch04-03-wordpress-roles-capabilities.md)

- [Shipping an Admin Back Office](ch05-00-shipping-an-admin-back-office.md)
  *The internal screen where someone non-technical manages the data.*
  - [Laravel: Filament in an Afternoon](ch05-01-laravel-filament.md)
  - [Symfony: EasyAdmin and Sonata](ch05-02-symfony-easyadmin.md)
  - [API Platform: An Admin Generated From Your API](ch05-03-api-platform-auto-admin.md)
  - [WordPress: Custom Post Types and ACF as a CRUD Engine](ch05-04-wordpress-cpt-as-crud.md)
  - [Laravel Nova ($): The Official, Supported Alternative to Filament](ch05-05-laravel-nova.md)

- [Shipping an API Other Teams Can Use](ch06-00-shipping-an-api.md)
  *REST, GraphQL, and OpenAPI docs, without hand-writing controllers for every resource.*
  - [API Platform: A Full API From One PHP Class](ch06-01-api-platform-from-one-class.md)
  - [Laravel: Sanctum, Resources, and API Versioning](ch06-02-laravel-sanctum-resources.md)
  - [WordPress: The Built-In REST API](ch06-03-wordpress-rest-api.md)

- [Shipping Real-Time Features](ch07-00-shipping-real-time-features.md)
  *Live notifications, presence, chat, and "the page just updated itself."*
  - [Laravel: Reverb and Livewire Without Writing JavaScript](ch07-01-laravel-reverb-livewire.md)
  - [Symfony: UX Turbo and Mercure](ch07-02-symfony-ux-turbo-mercure.md)
  - [Nextcloud Talk: Real-Time Built Into a Larger Platform](ch07-03-nextcloud-talk.md)
  - [Pusher ($): Managed WebSockets Without Running Your Own Server](ch07-04-pusher-managed-websockets.md)

- [Shipping File Storage and Collaboration](ch08-00-shipping-file-storage.md)
  *Uploads, sharing, versioning, and "our own Dropbox, please."*
  - [Nextcloud: A Ready-Made Drive, Not a DIY Project](ch08-01-nextcloud-ready-made-drive.md)
  - [Laravel: Filesystem Abstraction and S3-Compatible Storage](ch08-02-laravel-filesystem-s3.md)
  - [WordPress: The Media Library at Scale](ch08-03-wordpress-media-library.md)

- [Shipping a Storefront](ch09-00-shipping-a-storefront.md)
  *Products, carts, checkout, and taking real payments.*
  - [WooCommerce: E-Commerce on Top of WordPress](ch09-01-woocommerce.md)
  - [Sylius: A Symfony-Based E-Commerce Framework](ch09-02-sylius.md)
  - [Laravel: Cashier and Stripe ($) for Custom Checkouts](ch09-03-laravel-cashier-stripe.md)

- [Shipping Search That Feels Instant](ch10-00-shipping-search.md)
  *Typeahead, filtering, and search that doesn't feel like a `LIKE '%...%'` query.*
  - [Laravel: Scout With Meilisearch or Algolia ($)](ch10-01-laravel-scout-meilisearch.md)
  - [TYPO3: Solr and Elasticsearch Integration](ch10-02-typo3-solr-elasticsearch.md)
  - [WordPress: Search Plugins and When to Reach for Elasticsearch](ch10-03-wordpress-search-plugins.md)

- [Shipping Background Work](ch11-00-shipping-background-work.md)
  *Sending the email later, processing the upload later, running the report at 2 a.m.*
  - [Laravel: Queues and Horizon](ch11-01-laravel-queues-horizon.md)
  - [Symfony: The Messenger Component](ch11-02-symfony-messenger.md)
  - [WordPress: WP-Cron and the Action Scheduler](ch11-03-wordpress-wp-cron-action-scheduler.md)

- [Shipping an AI Feature This Sprint](ch12-00-shipping-an-ai-feature.md)
  *A support chatbot, a content assistant, or a smart search box, added to an existing app.*
  - [Laravel: Prism and the OpenAI/Anthropic PHP Clients](ch12-01-laravel-prism-llm-clients.md)
  - [Symfony: The AI Bundle](ch12-02-symfony-ai-bundle.md)
  - [WordPress: AI Plugins and When to Call an API Instead](ch12-03-wordpress-ai-plugins.md)

- [Shipping Multi-Language, Multi-Site](ch13-00-shipping-multi-language-multi-site.md)
  *One codebase, several languages, several markets, one client with a lot of national subsidiaries.*
  - [TYPO3: Multilingual Content Trees Done Properly](ch13-01-typo3-multilingual-trees.md)
  - [WordPress: Multisite and WPML](ch13-02-wordpress-multisite-wpml.md)
  - [Symfony: The Translation Component](ch13-03-symfony-translation-component.md)

- [Shipping Confidence](ch14-00-shipping-confidence.md)
  *Tests, static analysis, and security checks are a feature too: the one where the bug gets caught before your user finds it.*
  - [Laravel: Pest, Larastan, and `composer audit`](ch14-01-laravel-pest-larastan.md)
    *Tests that read like plain English, static analysis that catches bugs before runtime, dependency scanning that flags a known vulnerability before it ships.*
  - [Symfony: PHPUnit, PHPStan/Psalm, and Rector](ch14-02-symfony-phpunit-phpstan-rector.md)
    *Symfony's own test bridge, static analysis at whatever strictness level you choose, and Rector for safe, automated upgrades.*
  - [WordPress: PHPUnit, PHPCS/WPCS, and WPScan](ch14-03-wordpress-phpunit-phpcs-wpscan.md)
    *Testing against WordPress's own test suite, coding-standard and security linting with the WordPress ruleset, vulnerability scanning for plugins and themes.*
  - [Cross-Ecosystem: SAST, Dependency Scanning, and CI Gates](ch14-04-cross-ecosystem-sast-ci-gates.md)
    *PHPStan/Psalm as lightweight SAST, GitHub CodeQL and Dependabot, Snyk ($), and wiring all of it into CI so a broken or vulnerable build never reaches production.*
  - [Catching It in Production: Sentry and Flare ($)](ch14-05-sentry-flare-error-tracking.md)
    *Real-time error tracking and stack traces from wherever the app actually runs, so "confidence" doesn't stop at the deploy button.*

- [Shipping It Fast, At Scale](ch15-00-shipping-fast-at-scale.md)
  *When "it works" stops being enough and "it works under load" becomes the job.*
  - [FrankenPHP and Laravel Octane: Worker Mode Performance](ch15-01-frankenphp-laravel-octane.md)
  - [TYPO3: The Built-In Caching Framework](ch15-02-typo3-caching-framework.md)
  - [Nextcloud: Scaling a Self-Hosted Platform](ch15-03-nextcloud-scaling.md)
  - [Blackfire ($): Finding the Actual Bottleneck](ch15-04-blackfire-profiling.md)

- [Shipping to Production](ch16-00-shipping-to-production.md)
  *Getting it live, keeping it live, and not being the reason it went down.*
  - [Laravel: Forge and Vapor ($)](ch16-01-laravel-forge-vapor.md)
  - [Cloud Hosting: AWS, GCP, and Azure the Pragmatic Way](ch16-02-cloud-hosting-aws-gcp-azure.md)
    *When the client already has a cloud contract: Elastic Beanstalk/App Runner, Cloud Run, and Azure App Service, without hand-rolling infrastructure you don't need.*
  - [Platform.sh ($): One Deploy Story for Several Frameworks](ch16-03-platform-sh.md)
  - [WordPress: Managed Hosting Done Right (Kinsta, WP Engine $)](ch16-04-wordpress-managed-hosting.md)
  - [Nextcloud: All-in-One Docker Deployment](ch16-05-nextcloud-aio-docker.md)

- [Where to Go From There](ch17-00-where-to-go-from-there.md)
  - [Evaluating a New Stack in a Day](ch17-01-evaluating-a-new-stack-in-a-day.md)
  - [Communities Worth Joining](ch17-02-communities-worth-joining.md)
  - [If You Get Curious About What's Underneath](ch17-03-if-you-get-curious.md)
    *A bridge to [The PHP Book](../phpbook/src/SUMMARY.md), for whenever "just ship it" turns into "wait, how does this actually work?"*

- [Appendix](appendix-00.md)
  - [A - The Stack Cheat Sheet](appendix-01-stack-cheat-sheet.md)
    *One page: use case on the left, recommended pick on the right, `$` marking anything that isn't open source.*
  - [B - Glossary of Ecosystem Terms](appendix-02-glossary.md)
    *ORM, service container, hooks/filters, bundle, resource, and friends, defined by what they do for you.*
  - [C - Index of "Under the Hood" Boxes](appendix-03-under-the-hood-index.md)
    *Every modern-PHP feature quietly showcased in this book (property hooks, enums, attributes, readonly properties, Fibers, worker mode), indexed by chapter for the curious.*
