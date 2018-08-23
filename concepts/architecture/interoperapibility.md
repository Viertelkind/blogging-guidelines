# Interoperapibility

## INTEGRATIONS

### Content Management is about Integration

We understand that you are dealing with an existing enterprise architecture. Rather than trying to be a solution for everything, Hippo CMS is designed to be the web content management piece that will fit in your existing puzzle. You are in control of the puzzle and we make sure our piece fits in by providing the required [integration points](https://www.onehippo.org/library/concepts/integration/introduction.html). This gives you web content management and relevant multi-channel content delivery and allows you to integrate them with and leverage your existing solutions for everything else - solutions you carefully selected for good reasons.

### Content Integration

Content integration is a common requirement in today’s web content management. Your enterprise architecture may include several content-related systems such as Document Management and Digital Asset Management Systems, E-Commerce Product Catalogs and Product Information Systems. Perhaps legacy content needs to be taken into account as well. Hippo CMS’s architecture provides integration points at all relevant places where content is created, managed, published, processed or otherwise handled.

#### ![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/content-integration-points.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/content-integration-points.png)RESTful Services

Hippo CMS’s delivery tier provides a higher level integration point through its [support for the Java API for RESTful Services \(JAX-RS\)](https://www.onehippo.org/library/concepts/rest/restful-jax-rs-component-support-in-hst-2.html) and Java Architecture for XML Binding \(JAXB\) open standards, enabling content to be exposed as well as created or imported through REST endpoints. This opens up almost unlimited possibilities including Content-as-a-Service scenarios.

#### Search Platform Integration

In addition, the delivery tier provides integration points at framework level for [enterprise search platforms](https://www.onehippo.org/library/search-engine-integration/external-search-engine-integration.html) such as Solr or Elasticsearch, enabling seamless aggregation and delivery of content from  _any_ source inside your enterprise architecture.

#### Event Bus

The content repository provides an [Event Bus](https://www.onehippo.org/library/concepts/hippo-services/event-bus.html), which allows any application to subscribe to workflow events, for example to trigger updating your enterprise search platform of choice whenever content is published or taken offline.

#### JCR 2.0 API

Finally, Hippo CMS’s content repository exposes the full [JCR 2.0 API](https://www.onehippo.org/library/concepts/content-repository/jcr-interface.html), providing low-level access to content structures. This is, in fact, the interface used by the Hippo CMS authoring application and delivery tier. However, for integrations, we recommend using one of the higher-level integration points described above.

#### Example

A simple but powerful example content integration using some of the integration points described above is presented in our [Elasticsearch Lab](https://www.onehippo.org/labs/integrating-hippo-cms-with-elastic-search-engine.html).

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/content-integration-example.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/content-integration-example.png)

### Data Integration

A key strength of Hippo CMS is relevant content delivery, achieved through collecting and analyzing visitor data. This process is designed to integrate with your existing enterprise architecture and leverage any data you have about your customers and leads in your CRM, Marketing Automation, E-commerce or any other systems.

#### Relevance Collectors

The main data integration point provided by Hippo CMS’s delivery tier is the [Relevance Collector](https://www.onehippo.org/library/enterprise/enterprise-features/targeting/collectors.html) interface. Collectors collect data about visitors while they browse your sites. The data is aggregated into visitor profiles and matched to personas used to configure relevant content delivery.

Collectors can use any data source that is available during request processing, including external web services. This enables matching of the visitor profile against other data about customers and leads that are available in your enterprise architecture, further enriching the profile and optimizing control over relevance and conversion.

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/data-integration.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/data-integration.png)

#### REST Endpoint

All data collected about your visitors is available to your other applications via a secure RESTful web service. This is, in fact, the interface used by the CMS application to render the Experience Optimizer.

#### Example

A simple but powerful example of data integration using a relevance collector for the Pardot marketing automation platform is presented in our [Marketing Automation Lab](https://www.onehippo.org/labs/integrating-hippo-cms-with-marketing-automation.html).

### Frontend Integration

Web frontend technology is evolving fast. Hippo CMS’s powerful delivery tier offers extreme flexibility in this area. In addition to native content aggregation and page rendering capabilities, it also provides all the necessary integration points to enable the use of other frontend technologies and frameworks.

#### RESTful Services

Our delivery tier’s support for CaaS-based content delivery through [RESTful services](https://www.onehippo.org/library/concepts/rest/restful-jax-rs-component-support-in-hst-2.html) using the JAX-RS and JAXB open standards practically enables integration with any frontend technology or framework.

Your frontend framework of choice - whether it is a modern Single-Page Application design using client-side technology such as AngularJS, a classic server-side architectures like PHP or .NET, or a native mobile app - has full access to all content and CMS features through REST. It is entirely up to the framework how to aggregate and render content, whether it’s server-side, client-side, or a hybrid solution.

This enables you to leverage both your organization’s existing stack and expertise as well as the powerful features of Hippo CMS’s delivery tier, with a scalable architecture that is ready for future generations of frontend technologies too.

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/frontend-integration.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/frontend-integration.png)

#### Container Level Integration

Hippo CMS’s delivery tier also provides [container level integration](https://www.onehippo.org/library/concepts/integration/hst-container-integration-with-other-web-application-frameworks.html) with almost any other Java-based web application framework including Spring Web MVC, Struts, Tiles, and Wicket or even very basic servlets. This type of integration enables leveraging useful features of the delivery tier such as URL-content mappings, content beans, link rewriting, session pooling and the query API, while leaving the content aggregation and page rendering to the framework of choice.

This type of integration is particularly suited to hybrid solutions where Hippo CMS provides individual parts of larger aggregated web pages.

#### Example

Two simple but powerful examples of frontend integration using content delivery through RESTful services are presented in our [Angular JS](https://www.onehippo.org/labs/creating-your-first-angularjs-app-with-hippo-cms.html) and [Mobile](https://www.onehippo.org/labs/mobile/building-a-mobile-app-with-cordova-ionic-and-hippo-cms.html) Labs.

