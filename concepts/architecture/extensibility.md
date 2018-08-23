# Extensibility

## EXTENSIBILITY

Content delivery is a dynamic space. You want a platform that can accommodate the unique requirements of any CMS implementation. Therefore extensibility is a key quality attribute of any content delivery architecture. Hippo CMS does not aim to solve every problem but rather provides an extensible platform that enables you to adapt it to your needs.

### Extension Pattern

Hippo CMS’s delivery tier has extension points designed into all relevant areas of its architecture. All major components have interfaces, abstract base classes and various standard implementations which are extensible. Following the inversion of control design they are substitutable either through Spring configuration or even on-the-fly through configuration stored in the content repository.

### Extension Points

#### MVC Components

Our delivery tier uses the [Hierarchical Model-View-Controller pattern](https://www.onehippo.org/library/concepts/hst-configuration-model/pages-components-abstractpages-and-templates.html) for page rendering. Both models - called ['content beans'](https://www.onehippo.org/library/concepts/content-beans/creating-content-beans.html) - and controllers - called ['components'](https://www.onehippo.org/library/concepts/component-development/hst-2-component-development.html) - are interface-based and are extensible and substitutable. Many use cases can be implemented by using or extending one of the many [standard components](https://www.onehippo.org/library/setup/hst-components/overview.html) provided. If needed they can be written from scratch.

Views can be rendered by different templating engines, with [Freemarker](https://www.onehippo.org/library/concepts/web-application/hst-freemarker-support.html) and JSP implementations provided out-of-the-box. A standard tag library is provided and can be extended as well.

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/content-beans-extensibility.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/content-beans-extensibility.png)

_HMVC model extension using the HippoBean interface._

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/components-extensibility.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/components-extensibility.png)

_HMVC controller standard components extension._

#### Request Handling

Both the matching and the processing phases of the [request handling](https://www.onehippo.org/library/concepts/request-handling/hst-2-request-handling.html) by Hippo CMS’s deliver tier are extensible.

In the [matching](https://www.onehippo.org/library/concepts/request-handling/hst-2-request-matching.html) phase URLs are matched to a so-called sitemap item, which defines the page component configuration and content to render. This behavior can be extended using [sitemap item handlers](https://www.onehippo.org/library/concepts/hst-configuration-model/advanced/sitemapitem-handlers.html) to e.g. modify request attributes, add response headers or cookies, return a different sitemap item or even delegate the request to a different servlet.

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/sitemapitemhandlers-extensibility.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/sitemapitemhandlers-extensibility.png)

_Request matching extension using the HstSiteMapItemHandler interface._

The [processing](https://www.onehippo.org/library/concepts/request-handling/hst-2-request-processing.html) phase is performed using a processing pipeline consisting of valves. Each individual valve has exactly one responsibility, e.g. security, localization, content retrieval, component rendering, page aggregation and caching. Standard pipelines for HMVC-based web page rendering and for JAX-RS based RESTful services are provided out-of-the-box. Pipelines use inversion of control and are assembled through Spring configuration. The request processing can be extended by inserting [custom valves](https://www.onehippo.org/library/concepts/hst-spring/hst-orderable-valve-support.html) at any point in the pipeline.

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/valves-extensibility.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/valves-extensibility.png)

_Request processing extension using the OrderableValve interface._

#### RESTful Services

The delivery tier’s [support for JAX-RS](https://www.onehippo.org/library/concepts/rest/restful-jax-rs-component-support-in-hst-2.html) provides extensibility through custom REST endpoints. This opens up many possibilities including complex content integrations and CaaS-like scenarios.

