# Milestone 1. Kickoff

{% hint style="info" %}
**Let's get started!**

As we move through the integration process, each milestone starts with a quick summary of what we already did. Look for a yellow box like this one. If you see something in the summary that you don't remember doing, then let your BloomReach TPM know.
{% endhint %}

## Contents {#Milestone1.Kickoff-Contents}

* [What happens in this milestone?](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff#Milestone1.Kickoff-Whathappensinthismilestone?)
* [Kickoff meeting](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff#Milestone1.Kickoff-Kickoffmeeting)
* [Integration package](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff#Milestone1.Kickoff-integrationpackageIntegrationpackage)
* [Scope definition](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff#Milestone1.Kickoff-scopedefinitionScopedefinition)
* [What's next?](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff#Milestone1.Kickoff-What'snext?)

## What happens in this milestone? {#Milestone1.Kickoff-Whathappensinthismilestone?}

| What you need to do | What BloomReach needs to do | What we need to do together |
| :--- | :--- | :--- |
| You walk us through your site, giving in-depth details on parts that affect integration.Bring your stakeholders to the kickoff meeting. | We give you an integration package, which contains items that are customized to help you get started. | We map out the integration process, including a timeline and milestones. |

## Kickoff meeting {#Milestone1.Kickoff-Kickoffmeeting}

Your integration process starts with a kickoff meeting during which the process is scoped and milestones are mapped.

Here are the stakeholders who need to attend the integration kickoff meeting:

| From your company | From BloomReach |
| :--- | :--- |
| Business sponsorsSEO and marketing managersDevelopment and infrastructure managersFrontend and backend developersUI and UX managersOther stakeholders at your discretion | Technical Project Manager \(TPM\)Customer Success Manager \(CSM\)Account Executive |

## Integration package {#Milestone1.Kickoff-integrationpackageIntegrationpackage}

Before the kickoff meeting, your BloomReach TPM gives you an integration package to help you with the process. This package includes the following items:

* Your account ID and authentication credentials
* A JavaScript tracking pixel for traffic and conversion tracking

## Scope definition {#Milestone1.Kickoff-scopedefinitionScopedefinition}

You and the BloomReach integration team kick off the integration process by defining the scope of the integration project. You guide us through an in-depth walkthrough of your site, including infrastructure topics such as firewalls, caching, and proxies. Together, we review the integration process in detail, then map a timeline for the integration with milestone dates.

There are two parts to the scope definition meeting. The first part of the meeting starts with a high-level scoping session during which your BloomReach TPM introduces and discusses the following topics:

* BloomReach technology
* Overview of technical and resource requirements
* Server-side and client-side integration
* Product ranking and personalization features

The second part of the meeting gets into the details of the scope of your integration. You meet with the BloomReach integration team to give them an in-depth understanding of your site, especially the following parts:

* Products
* Brands
* Subdomains
* Data restrictions
* UI and UX overview

### Scope session agenda items {#Milestone1.Kickoff-Scopesessionagendaitems}

Here are some common agenda items for the scope session. Your own agenda might have different or additional items. Your BloomReach integration team delves into the specifics of the agenda with you. 

#### Endpoints and environments {#Milestone1.Kickoff-Endpointsandenvironments}

We ask you questions about your testing and staging environments. We need to know the endpoints for your testing and staging environments, and we need login credentials.

#### Site information {#Milestone1.Kickoff-Siteinformation}

Upon initial launch of BloomReach Personalization on your site, we conduct a test to demonstrate lift by running on about 50% of your pages, leaving your other 50% as your control group. If you have 1000 URLs, then we run BloomReach Personalization on 500 of them. To make sure that we understand all the unique aspects of your site, we gather some information from you about your site that can affect this test. Here's a sample set of questions to give you an idea of what we need to know.

| Sample question | Why we ask |
| :--- | :--- |
| Is your site a tail site? | A tail site has many product pages, but doesn't have a lot of traffic. We ask this question because if your answer is yes, then we need approximately 14 days to fetch data from your site so that we have a good pipeline. |
| Does your site have a high rate of product churn? | If the rate of your site's product churn is high, then we might need to make some adjustments to the control phase, such as the following:Adjust the length of the control period.Target URLs for out of stock items. |
| Which URL parameters do you use to track promotional campaign traffic, such as paid searches and email? | During analysis of the control phase, we need to delineate between lift caused by BloomReach Personalization and lift caused by promotions. |

#### Organic widgets {#Milestone1.Kickoff-Organicwidgets}

Organic widgets contain Related Categories, Related Items and Related Products on your site's pages. Together, we establish the location and appearance of these widgets on your pages.

There are a maximum of five links in the Related Categories and Related Items widget. 

Typically, there are four products in the Related Products widget. You can't display fewer than four products. Let your BloomReach TPM know if you want to display more than four products.

Widgets must be integrated on your mobile pages. BloomReach supports widgets on mobile devices if your mobile URL structure after the domain name is the same as the structure for your desktop URLs. If you have a separate mobile site, then ensure widgets are integrated on that separate site as well as your desktop site.

#### Thematic pages {#Milestone1.Kickoff-Thematicpages}

Thematic pages are customized, category-like landing pages that are created and launched by the BloomReach Thematic Pages feature. These pages are focused on long-tail themes with products matched through BloomReach’s matching technology.  

We help you determine the appearance and general contents of thematic pages on your site. The specific contents of thematic pages are automatically curated with BloomReach matching technology.

We ask how you handle the different devices that your customers use when landing on your site. What happens to the URL? For example, the letter _m_ is commonly appended to a URL for sites that make a distinction between desktops and mobile devices.

We confirm that it's okay for BloomReach to launch your new thematic pages automatically after they pass QA.![](https://help.bloomreach.com/images/icons/emoticons/lightbulb_on.png) **Automatic launch protects your integration schedule**

We recommend this automatic approach for launching thematic pages because setting and following an approval process often creates bottlenecks in the integration process, which in turn can cause your timeline to slip unpredictably. However, if you prefer to approve thematic pages before launch, then we can work with you to define the approval chain with approvers and alternate approvers. You need to manage the approval process within your company, making sure that approvers are both available and knowledgeable about their role in the integration process.

Based on your decision during the sales process to use JSON-powered Thematic Pages or HTML, we help you determine which parts of the API deployment milestone are relevant to your needs.

We discuss the XML sitemap for thematic pages, which helps search engines find your pages quickly and reliably.

#### Browsers {#Milestone1.Kickoff-Browsers}

We ask which browsers your site supports. The most common browsers are Chrome, Safari, Edge, Firefox, and Internet Explorer.

#### Products {#Milestone1.Kickoff-Products}

We ask many questions about your products to ensure that we target the right pages and products. Here's a sample set of these questions:

* How many products are on your site?
* How many SKUs are on your site?
* How often do prices change on your site?
* How many category pages are on your site?
* How many brand-specific pages are on your site?
* How often do products go out of stock?
* How do you flag out of stock products on your site?
* Do you include out of stock products in your product feed?  If so, how do you denote them?
* Do you always put out of stock products on backorder?
* Do you have products that can't be backordered when they go out of stock?
* What is your process for discontinued products, both before they go out of stock and after they go out of stock?

#### Scope of pages {#Milestone1.Kickoff-Scopeofpages}

Together, we determine which of your pages are in or out of scope for your integration project. Here's a sample list of pages that are usually in or out of scope. Your own pages might be different.

| Usually in scope | Usually out of scope |
| :--- | :--- |
| High-level category pagesSubcategory pagesProduct feed URLsProduct family pagesProduct detail pagesBrand pagesManufacturer pagesPromotional and sale pages | Out of stock pagesUnavailable pagesDiscontinued product pagesAbout pageFAQ and similar pages |

#### Site crawling {#Milestone1.Kickoff-Sitecrawling}

BloomReach continually crawls your site to keep the content of your thematic pages and widgets for Related Categories, Related Items and Related Products current and valuable.

We ask you questions about the number of queries per second \(QPS\) that you want us to crawl, and we have some environment questions. Here's a sample set of questions:

* What's the maximum QPS that you want BloomReach to use when crawling your site?
* What are your IP addresses? We ask this question to ensure that we don't count your own company's site visits.

We don't crawl your mobile URLs.

## What's next? {#Milestone1.Kickoff-What'snext?}

Continue to the next milestone: [Pixel deployment](https://help.bloomreach.com/display/BRINT/Milestone+2.+Pixel+deployment).

1. [Kickoff](https://help.bloomreach.com/display/BRINT/Milestone+1.+Kickoff)
2. [Pixel deployment](https://help.bloomreach.com/display/BRINT/Milestone+2.+Pixel+deployment)
3. [Feed delivery](https://help.bloomreach.com/display/BRINT/Milestone+3.+Feed+delivery)
4. [API deployment](https://help.bloomreach.com/display/BRINT/Milestone+4.+API+deployment)
5. [Listen and tune](https://help.bloomreach.com/display/BRINT/Milestone+5.+Listen+and+tune)
6. [Data deployment](https://help.bloomreach.com/display/BRINT/Milestone+6.+Data+deployment)
7. [Day zero](https://help.bloomreach.com/display/BRINT/Milestone+7.+Day+zero)

