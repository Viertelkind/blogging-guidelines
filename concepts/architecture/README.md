# Architecture

## HIPPO CMS APPLICATION ARCHITECTURE

Hippo CMS is a Java-based open source _web content management platform_. It uses modern web architectures, open standards and open source components throughout. In all layers of the architecture, open and extensible [APIs](https://www.onehippo.org/library/about/javadoc.html) are available for [integrating](https://www.onehippo.org/library/concepts/integration/introduction.html) Hippo CMS into your existing application architecture.

The Hippo CMS architecture is highly modular. This modular and clean architecture has several technical benefits such as ease of integration and great scalability, and also functional benefits such as content reuse. In the next sections, details are provided on each module in the Hippo CMS stack. We highlight the three modules listed in the diagram below; _Content Repository_, _CMS_ and _Delivery Tier_ \(also known as HST\).

### High Level Component Overview

![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/architecture/uml/why-hippo/open-platform-2.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/architecture/uml/why-hippo/open-platform-2.png)

At high level Hippo CMS's architecture consists of three major components:

* Content repository \("Hippo Repository"\)
* Authoring application \("Hippo CMS"\)
* Delivery tier \("HST"\)

The diagram on the right shows how they are interconnected. The following sections describe each component in more detail.

#### Content Repository

The core of Hippo CMS is the Hippo Repository. All content, metadata and configuration is stored in this central component. In addition to providing a storage layer, the repository is also responsible for the base content management services such as meta-data and workflow, content searching, processing, scheduling, transformation and aggregation, and the orchestration thereof.

Hippo Repository is based on [Apache JackRabbit](http://jackrabbit.apache.org/), an open source implementation of the  [JSR-170](https://jcp.org/ja/jsr/detail?id=170) and [JSR-283](https://jcp.org/en/jsr/detail?id=283) Java specifications. All content management functionality is exposed through a standard set of API interfaces. This allows your application or process to integrate with Hippo CMS for automatic creation, import, export and publication of content, in addition to the web based authoring application.

An important feature of Hippo CMS is that it strictly separates content and content management from the context of its usage. Hippo CMS does not maintain content in a “page-oriented" manner, but stores and manages metadata that is context-dependent separately. This allows for reuse, search and filtering of content across different contexts, channels and devices. Especially within a large enterprise environment this is an important feature supporting reuse, integration and interoperability with other applications.

#### Authoring

The Hippo CMS authoring application provides a web-based user interface through which teams can collaborate to create and manage their content. All from within the same user interface, web masters, marketers, editors and authors can perform functions such as the creation of new sub-sites, editing of page templates, menu structures or content, creation of different page templates for different targeted personas, and so on.

Depending on the role within the organization, certain functions or content can be hidden or made read-only for certain groups of users through centralized access management and workflow systems.

The authoring application is fully customizable through a GUI plugin architecture based on the [Apache Wicket](https://wicket.apache.org/) web application framework.

#### Delivery

Hippo CMS's delivery tier \(also known as HST\) provides the framework and tools for rapid development of websites and other channels such as REST endpoints or RSS feeds. It can be used to quickly create multi-site and multi-channel front-ends through a combination of configuration and development. It provides functionality for creation of page templates, which can be further refined by webmasters in the authoring application.

Features include a templating engine which is easily configurable through the authoring appliciation's user interface, and a tag library and expression language to accommodate the development of a JSP or Freemarker-based view layer. Hippo CMS's delivery tier also has built-in caching and page diagnostics to ensure great performance.

### Quality Attributes

Hippo CMS's architectural design is driven by the following quality attributes:

* [Interoperability](https://www.onehippo.org/library/about/why-hippo/integrations.html) The ability of a system to work together with other systems.
* [Extensibility](https://www.onehippo.org/library/about/why-hippo/extensibility.html) The ability to extend a system and the level of effort required to implement the extension.
* [Scalability](https://www.onehippo.org/library/about/why-hippo/scalability.html) The ability of a system to handle a growing amount of work in a capable manner or its ability to be enlarged to accommodate that growth.
* [Performance](https://www.onehippo.org/library/about/why-hippo/performance.html) The amount of work accomplished by a system compared to the time and resources used.
* [Availability](https://www.onehippo.org/library/about/why-hippo/availability.html) The proportion of time a system is in a functioning condition.
* [Security](https://www.onehippo.org/library/about/why-hippo/security-features.html) The ability of a system to reliably control, monitor, and audit who can access the system and who can perform what actions on which resources, and the ability to detect and recover from failures in security mechanisms.

### Further Reading

* [System Architecture](https://www.onehippo.org/library/deployment/system-architecture.html)
* [A Bird's Eye Hippo CMS Architectural View Part 1: 10,000 foot view](https://www.bloomreach.com/en/blog/2013/07/hippo-cms-a-birds-eye-architectural-tour.html) blog by Ard Schrijvers
* [A Bird's Eye Hippo CMS Architectural View Part 2: 1,000 foot view on the HST](https://www.bloomreach.com/en/blog/2014/01/hippo-cms-a-birds-eye-architectural-view-on-hst.html) blog by Ard Schrijvers

