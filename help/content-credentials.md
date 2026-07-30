---
title: Content Credentials for generative AI transparency
description: Learn how Adobe automatically attaches Content Credentials to GenAI-generated and GenAI-edited content across Adobe CX Enterprise applications.
---

# Content Credentials for generative AI transparency

This page covers details about how Adobe handles automatic attachment of Content Credentials across Adobe CX Enterprise applications.

New regulations will go into effect requiring providers of generative AI technologies to support durable, machine-readable disclosures associated with GenAI-generated and GenAI-assisted content workflows for expanded transparency.

As a tool provider, Adobe is automatically attaching machine-readable metadata (Content Credentials) to GenAI-generated and GenAI-edited content using Adobe technologies (including supported third-party generative AI models within Adobe workflows).

Content Credentials are a tamper evident metadata based on the C2PA open standard. Downstream platforms and services that support Content Credentials may use this information to display transparency indicators to end users.

>[!IMPORTANT]
>
>Customers can choose to customize Content Credentials with additional metadata such as name, social media handle, or edit history in certain applications including [Photoshop](https://helpx.adobe.com/photoshop/desktop/save-and-export/metadata-content-credentials/use-content-credentials.html), [Premiere](https://helpx.adobe.com/x-productkb/content-credentials.html), [Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/assets-view/content-credentials), and others. This optional addition of customized metadata in Content Credentials is **distinct** from the use noted above, in which Content Credentials will be applied automatically and indicate limited information about the content, including that GenAI was used in its creation or editing. As noted above, Adobe automatically attaches Content Credentials to qualifying GenAI content. This functionality cannot be disabled.

## What's changing

Starting August 3, 2026, Adobe is releasing Content Credentials support across Adobe CX Enterprise applications.

This release includes:

* Automatic attachment of Content Credentials to supported GenAI-generated and GenAI-edited content.
* Support for content types, including images, video, audio, and text.
* Preservation of Content Credentials throughout supported Adobe workflows.

No additional action is required to attach Content Credentials to qualifying generative AI content.

>[!NOTE]
>
>Content Credentials will not impact the appearance of your content. Content Credentials and visible watermarks serve different purposes. Content Credentials provide machine-readable provenance information, while visible watermarks provide a visual disclosure. You may choose to add visible watermarks to your content.

## What details are added as part of Content Credentials

Automatically attached Content Credentials may include information such as:

* Name and version information of the AI system used (for example, Adobe GenStudio, Adobe Firefly)
* AI model used (for example, Adobe Firefly)
* Usage: Whether it was generated or edited using GenAI
* Time and date of content creation and/or modification with generative AI tools
* Unique identifier (that can be used to distinguish each use of Generative AI)

By default, automatically attached Content Credentials do not include personally identifiable information (PII).

## Content Credentials across the content supply chain

Content Credentials are designed to remain associated with supported content as it moves between Adobe applications and compatible third-party platforms.

As content is published, distributed, or shared, platforms that support Content Credentials or related provenance technologies may read attached metadata and display transparency information to users.

Adobe does not control how external services interpret, display, or use Content Credentials after content leaves Adobe applications. Customers should consult the documentation for individual publishing platforms to understand how Content Credentials are handled.

## Visible watermarking

In some circumstances and in certain geographies, organizations may choose or be required to visibly identify GenAI-generated or GenAI-edited content.

Adobe provides [guidance](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html) on using existing watermarking capabilities supported via Adobe applications. Whether visible watermarking is required depends on an organization's business requirements and the applicable laws and regulations in the jurisdictions where content is published.

>[!NOTE]
>
>Content Credentials and visible watermarks serve different purposes. Content Credentials provide machine-readable provenance information, while visible watermarks provide a visual disclosure that organizations may choose to apply.

## Availability & releases

These features are available beginning **August 3, 2026** across supported Adobe CX Enterprise workflows.

The release includes:

### Automatic Content Credentials

Content Credentials are automatically attached to supported GenAI-generated and GenAI-edited content. This functionality is enabled by default and cannot be disabled.

Where applicable, all Adobe CX Enterprise applications continue to preserve existing Content Credentials as supported assets move through Adobe workflows. This helps maintain the integrity of provenance information throughout the content supply chain.

### Watermark guidance

Adobe provides [documentation](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html) describing how to use existing watermarking features available in supported Adobe applications for organizations that choose or need to apply visible labels.

## Supported applications across Adobe CX Enterprise {#supported-applications}

The following Adobe applications and services provide additional information about Content Credentials within certain CX Enterprise apps.

However, where applicable, all Adobe CX Enterprise applications continue to preserve existing Content Credentials as supported assets move through Adobe workflows. This helps maintain the integrity of provenance information throughout the content supply chain.

>[!NOTE]
>
>The release notes or guidance for each of the applications listed below will be made available on Experience League in their respective application product page sections. The table will be updated with the links as they become available. Refer to the latest product sections on Experience League.

| Application/Solution | Release Notes/Guidance |
|---|---|
| Advertising Cloud | |
| Adobe Experience Manager (AEM) | |
| AI Assistant for Content Generation (feature in Adobe Journey Optimizer / Adobe Campaign) | |
| Adobe Journey Optimizer B2B Ultimate | |
| Adobe Journey Optimizer B2B Prime | |
| Adobe Journey Optimizer B2C | |
| Adobe Campaign | |
| Adobe Commerce | |
| Adobe CX Enterprise Coworker Campaigns (formerly HALO) | |
| GenStudio for Performance Marketing | |
| Adobe Marketo | |
| Adobe Workfront | |

## Related links

* [Visible Watermark Guide](https://helpx.adobe.com/creative-cloud/apps/generative-ai/ai-content-watermarks-faq.html)
* [Content Authenticity Initiative](https://contentauthenticity.adobe.com/)
* [Adobe Inspect](https://contentauthenticity.adobe.com/inspect)

## Frequently asked questions

**Which Adobe apps apply Content Credentials to generative AI edited or created content?**

Supported Adobe CX Enterprise applications automatically attach Content Credentials to qualifying GenAI-generated and GenAI-edited content. Refer to the [Supported applications](#supported-applications) section for more details regarding Adobe CX Enterprise applications.

**Which content types does Adobe add Content Credentials to?**

Broadly, images, audio, video, and text are in scope. However, please refer to the documentation in the [Supported applications](#supported-applications) section to find how each application supports Content Credentials across different products and content types.

**Which applications in Adobe CX preserve Content Credentials throughout editing and publishing?**

All Adobe CX Enterprise applications are designed to preserve Content Credentials as content moves through compatible Adobe workflows. Preservation outside Adobe applications depends on whether external platforms support Content Credentials.

**What happens when multiple GenAI-generated images are combined into a single image?**

The resulting Content Credentials depend on the application and workflow used. Where supported, Adobe preserves provenance information throughout the editing process. Refer to the [Supported applications](#supported-applications-across-adobe-cx-enterprise) section for the documentation for workflow-specific behavior in each app.

**What happens when GenAI-generated images from Adobe and non-Adobe applications are combined?**

Adobe preserves Content Credentials that are available and supported within the workflow. Wherever applicable, Adobe will update the underlying metadata with the latest information whenever applicable content (image, audio, video, text) is edited or created using GenAI within Adobe workflows. When you combine several sources into one new asset, their credentials are not replaced or lost. Instead, the new asset gets its own Content Credential, and the details from each source are kept inside it. If a source already had its own Content Credentials--whether it came from an Adobe or a non-Adobe tool--that history stays attached to it. This means the final asset carries a complete picture: its own record of being created or edited with GenAI, plus the individual history of each piece that went into it.

**Do GenAI-edited and GenAI-created workflows in Adobe CX applications automatically attach Content Credentials?**

Yes. For supported generative AI workflows, Adobe automatically attaches Content Credentials that identify whether content was GenAI-generated or GenAI-edited together with other provenance information, such as timestamps, AI system information, and unique identifiers.

**How are Content Credentials maintained throughout the content supply chain?**

Content Credentials are durable metadata designed to remain associated with supported content as it moves between compatible Adobe applications and supporting third-party platforms. External services determine how attached provenance information is displayed after publication.

**How can organizations add their own authenticated information without breaking the provenance chain?**

Some Adobe applications allow creators and organizations to add additional authenticated information to existing Content Credentials while preserving provenance. Availability varies by application.

**Will it be possible to turn off automatic attachment of Content Credentials?**

No. New generative AI transparency laws require companies that provide generative AI tools, including Adobe, to attach durable metadata to qualifying content generated or edited with generative AI. Automatic attachment of Content Credentials cannot be turned off.

**What happens to content created/edited with generative AI before the August release?**

Content created or edited with generative AI tools before the August 3, 2026 release will not have automatic Content Credentials attached. However, content created in Firefly web and other apps where Content Credentials were previously applied will continue to have them attached.

**How can a customer check if content has Content Credentials attached?**

Customers can check whether content has Content Credentials attached by uploading it to the [Adobe Inspect](https://contentauthenticity.adobe.com/inspect) page.

**How do external platforms display Content Credentials once content is published or shared?**

As content moves across publishing platforms, social media channels, email services, and other digital ecosystems, downstream services that support Content Credentials, or related provenance technologies, may be able to read attached metadata and may choose to display disclosures or indicators based on that information. Adobe does not control how external platforms display, interpret, or apply disclosures associated with attached Content Credentials. For the most current information on how a specific platform handles provenance information, customers should check that platform's guidelines directly.

**Will these changes increase the cost of Adobe products or subscriptions?**

No. This will not impact the cost of Adobe products.
