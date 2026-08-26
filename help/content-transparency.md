---
title: Generative AI content transparency
description: Learn how Adobe automatically attaches C2PA metadata to GenAI-generated and GenAI-edited content across Adobe CX Enterprise applications.
---

# Generative AI content transparency

Throughout August 2026, Adobe is gradually rolling out C2PA metadata support across Adobe Creative Cloud, Adobe Document Cloud, Adobe Firefly, and Adobe CX Enterprise applications. 

>[!NOTE]
>
>Following the rollout, future workflows that involve content being created or edited using AI will automatically have C2PA metadata support.

This page covers details about how Adobe handles automatic attachment of C2PA metadata across Adobe CX Enterprise applications.

New regulations require providers of generative AI technologies to support durable, machine-readable disclosures associated with GenAI-generated and GenAI-edited content workflows for expanded transparency.

As a tool provider, Adobe is automatically attaching machine-readable C2PA metadata to GenAI-generated and GenAI-edited content using Adobe technologies (including supported third-party generative AI models within Adobe workflows). [Learn more about C2PA](https://c2pa.org/).

## What's changing

Rolling out in August 2026, Adobe will introduce C2PA metadata support across Adobe Creative Cloud, Adobe Document Cloud, Adobe Firefly, and Adobe CX Enterprise applications. 

This release includes:

* Automatic attachment of C2PA metadata to supported GenAI-generated and GenAI-edited content.
* Support for content types, including images, video, audio, and text.
* Preservation of C2PA metadata throughout supported Adobe workflows.

No additional action is required to attach C2PA metadata to qualifying generative AI content.

>[!NOTE]
>
>C2PA metadata will not impact the appearance of your content. C2PA metadata and visible watermarks serve different purposes. C2PA metadata provides machine-readable provenance information, while visible watermarks provide visual disclosure. You may choose to add visible watermarks to your content based on business needs and the legal requirements of each applicable jurisdiction.

## What details are added as part of C2PA metadata

Automatically attached C2PA metadata may include information such as:

* Name and version information of the AI system used (for example, Adobe GenStudio, Adobe Firefly)
* AI model used (for example, Adobe Firefly)
* Usage: Whether it was generated or edited using GenAI
* Time and date of content creation and/or modification with generative AI tools
* Unique identifier (that can be used to distinguish each use of Generative AI)

## C2PA metadata across the content supply chain

C2PA metadata is designed to remain associated with supported content as it moves between Adobe applications and compatible third-party platforms.

As content is published, distributed, or shared, platforms that support C2PA metadata or related provenance technologies may read attached metadata and display transparency information to users.

Adobe does not control how external services interpret, display, or use C2PA metadata after content leaves Adobe applications. Customers should consult the documentation for individual publishing platforms to understand how C2PA metadata is handled.

## Visible watermarking

In some circumstances and in certain geographies, organizations may choose or be required to visibly identify GenAI-generated or GenAI-edited content.

Adobe provides [guidance](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html) on using existing watermarking capabilities supported via Adobe applications. Whether visible watermarking is required depends on an organization's business requirements and the applicable laws and regulations in the jurisdictions where content is published.

>[!NOTE]
>
>C2PA metadata and visible watermarks serve different purposes. C2PA metadata provides machine-readable provenance information, while visible watermarks provide a visual disclosure that organizations may choose to apply.

## Availability & releases

These features are rolling out throughout **August 2026** across supported Adobe CX Enterprise workflows.

>[!NOTE]
>
>Following the rollout, future workflows that involve content being created or edited using AI will automatically have C2PA metadata support.

The release includes:

### Automatic C2PA metadata

C2PA metadata is automatically attached to supported GenAI-generated and GenAI-edited content. This functionality is enabled by default and cannot be disabled.

### Watermark guidance

Adobe provides [documentation](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html) describing how to use existing watermarking features available in supported Adobe applications for organizations that choose or need to apply visible labels.

## Supported applications across Adobe CX Enterprise {#supported-applications}

The following Adobe applications and services provide additional information about how and when C2PA metadata is attached to qualifying content within certain CX Enterprise apps.

However, where applicable, all Adobe CX Enterprise applications continue to preserve existing C2PA metadata as supported assets move through Adobe workflows. This helps maintain the integrity of provenance information throughout the content supply chain.

>[!NOTE]
>
>The release notes or guidance for each of the applications listed below will be made available on Experience League in their respective application product page sections. The table will be updated with the links as they become available. Refer to the latest product sections on Experience League.

| Application/Solution | Release Notes/Guidance |
|---|---|
| Adobe Advertising Cloud | [Documentation](https://experienceleague.adobe.com/en/docs/advertising/creative/creative-studio/creative-studio-content-credentials) |
| Adobe Experience Manager (AEM) | [Documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/c2pa-metadata-dynamic-media-openapi) |
| AI Assistant for Content Generation (feature in Adobe Journey Optimizer / Adobe Campaign) | [Documentation](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/generate-content/generative-c2pa-metadata) |
| Adobe Journey Optimizer B2B Ultimate | [Documentation](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/content-management/assets/c2pa-metadata) |
| Adobe Journey Optimizer B2B Prime (aka Adobe Marketo Optimizer) | [Documentation](https://experienceleague.adobe.com/en/docs/marketo-optimizer/user/content/assets/c2pa-metadata) |
| Adobe Journey Optimizer B2C | |
| Adobe Campaign | |
| Adobe Commerce | [Documentation](https://experienceleague.adobe.com/en/docs/commerce/optimizer/manage-results/success-metrics#c2pa-metadata-on-exported-reports) |
| GenStudio for Performance Marketing | [Documentation](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/content-credentials) |
| Adobe Marketo Engage | [Documentation](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/images-and-files/c2pa-metadata) |
| Adobe Workfront | [Documentation](https://experienceleague.adobe.com/en/docs/workfront/using/documents/c2pa-metadata-overview) |
| CX Enterprise Coworker Campaigns (formerly HALO) | [Documentation](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/campaigns/c2pa-metadata) |

## Related links

* [Visible Watermark Guide](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html)
* [Adobe Inspect](https://contentauthenticity.adobe.com/inspect)
* [Overview of the Adobe GenAI Labeling Compliance Initiative](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-labeling-faq.html)

## Frequently asked questions

**Which Adobe apps apply C2PA metadata to generative AI edited or created content?**

Supported Adobe CX Enterprise applications automatically attach C2PA metadata to qualifying GenAI-generated and GenAI-edited content. Refer to the [Supported applications](#supported-applications) section for more details regarding Adobe CX Enterprise applications.

**Which content types does Adobe add C2PA metadata to?**

Broadly, images, audio, video, documents, and text are in scope. However, please refer to the documentation in the [Supported applications](#supported-applications) section to find how each application supports C2PA metadata across different products and content types.

**Which applications in Adobe CX preserve C2PA metadata throughout editing and publishing?**

All Adobe CX Enterprise applications are designed to preserve C2PA metadata as content moves through compatible Adobe workflows. Preservation outside Adobe applications depends on whether external platforms support C2PA metadata.

**What happens when multiple GenAI-generated images are combined into a single image?**

The resulting C2PA metadata depend on the application and workflow used. Where supported, Adobe preserves provenance information throughout the editing process. Refer to the [Supported applications](#supported-applications-across-adobe-cx-enterprise) section for the documentation for workflow-specific behavior in each app.

**What happens when GenAI-generated images from Adobe and non-Adobe applications are combined?**

Adobe preserves C2PA metadata that are available and supported within the workflow. Wherever applicable, Adobe will update the underlying metadata with the latest information whenever applicable content (image, audio, video, text) is edited or created using GenAI within Adobe workflows. When you combine several sources into one new asset, their underlying metadata is not replaced or lost. Instead, the new asset gets its own C2PA metadata, and the details from each source are kept inside it. If a source already had its own C2PA metadata--whether it came from an Adobe or a non-Adobe tool--that history stays attached to it. This means the final asset carries a complete picture: its own record of being created or edited with GenAI, plus the individual history of each piece that went into it. 

**Do GenAI-edited and GenAI-created workflows in Adobe CX applications automatically attach C2PA metadata?**

Yes. For supported generative AI workflows, Adobe automatically attaches C2PA metadata that identify whether content was GenAI-generated or GenAI-edited together with other provenance information, such as timestamps, AI system information, and unique identifiers.

**How are C2PA metadata maintained throughout the content supply chain?**

C2PA metadata is durable metadata designed to remain associated with supported content as it moves between compatible Adobe applications and supporting third-party platforms. External services determine how attached provenance information is displayed after publication.

**How can organizations add their own authenticated information without breaking the provenance chain?**

Some Adobe applications allow creators and organizations to add additional authenticated information to existing C2PA metadata while preserving provenance. Availability varies by application.

**Is it possible to turn off automatic attachment of C2PA metadata?**

No. New generative AI transparency laws require companies that provide generative AI tools, including Adobe, to attach durable metadata to qualifying content generated or edited with generative AI. Automatic attachment of C2PA metadata cannot be turned off.

**What happens to content created/edited with generative AI before the August release?**

Content created or edited with generative AI tools before the August 2026 release does not have automatic C2PA metadata attached. However, content created in Firefly web and other apps where C2PA metadata were previously applied continue to have them attached.

**How can a customer check if content has C2PA metadata attached?**

Customers can check whether content has C2PA metadata attached by uploading it to the [Adobe Inspect](https://contentauthenticity.adobe.com/inspect) page.

**How do external platforms display C2PA metadata once content is published or shared?**

As content moves across publishing platforms, social media channels, email services, and other digital ecosystems, downstream services that support C2PA metadata, or related provenance technologies, may be able to read attached metadata and choose to display disclosures or indicators based on that information. Adobe does not control how external platforms display, interpret, or apply disclosures associated with attached C2PA metadata. For the most current information on how a specific platform handles provenance information, customers should check that platform's guidelines directly.

**Do these changes increase the cost of Adobe products or subscriptions?**

No. C2PA metadata does not impact the cost of Adobe products.
