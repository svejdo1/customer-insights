---
title: Install and manage Customer Insights
description: How to install, uninstall, and manage Dynamics 365 Customer Insights environments.
ms.date: 09/22/2023 
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Install and manage Dynamics 365 Customer Insights

[!INCLUDE[consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

This article explains how to access and use the installation management area for Customer Insights. In this one-stop experience, you can manage to install and uninstall the Customer Insights - Journeys and Customer Insights - Data applications.

All of your Dataverse environments are listed in the installation management area by type (**Production** or **Trial**). You can see where Customer Insights – Journeys and Customer Insights – Data are installed and take action to install or uninstall.

## Prerequisites and requirements

To install Customer Insights, you must meet all the following requirements:

- You must already have a Microsoft 365 tenant.
- To install the Customer Insights - Journeys or Customer Insights - Data applications, you must have a Dynamics 365 Customer Insights, Dynamics 365 Marketing, or Dynamics 365 Customer Insights – Standalone license on your tenant.
- You must sign into your tenant with a user account that has all the following:
   - A security role (such as _Global admin_ or [_Service support admin_](/power-platform/admin/use-service-admin-role-manage-tenant)) that allows you to modify the target Dynamics 365 environment. (If you're reinstalling Customer Insights on an environment where Customer Insights was previously installed, then _Service support admin_ users [_Dynamics 365 administrator_ or _Power Platform administrator_] must use the same user ID as was used for the initial install. If you're not sure which ID was used for the initial install, or if you're getting errors, then try to install as a _Global admin_.)
   - Permissions to register applications in Azure. The global administrator always has this right, but other accounts can also have it. See [Do I have permissions to register applications on Azure?](setup-troubleshooting.yml#register-apps-azure) for information about how to confirm this setting for your account.
   - A Dynamics 365 license with the _System Administrator_ security role assigned on your target Dynamics 365 environment. (The Customer Insights license agreement doesn't legally require the installing user to have this license, but a known technical issue currently makes it necessary.)
- You must be located in a country/region where the product is supported. To read the latest list of countries/regions where you can use Customer Insights, download the [Microsoft Dynamics 365 International Availability](https://go.microsoft.com/fwlink/p/?linkid=875097) document (PDF).
- Close all other browser windows and tabs before starting.
- Clear your browser cache before starting.

If you run into trouble while installing, see the [Administration and setup FAQ](setup-troubleshooting.yml) for some possible solutions.

> [!IMPORTANT]
> Your system is constrained by certain limits and quotas that apply to the number of contacts you can market to, monthly email messages you can send, Litmus previews you can view, and more. Please familiarize yourself with the terms and limits of the product before you begin to use it. The limits are different based on whether you are running a trial or subscribed version of the product.
> 
> - For subscribed (paid) versions, please download the [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/p/?linkid=866544) and visit the [Fair use policy](fair-use-policy.md) page.
> - For trials, see [Dynamics 365 Customer Insights limits for trials](trial-preview-limits.md).
> 
> You can monitor your usage levels by going to  **Settings**  >  **Advanced settings**  >  **Other settings**  >  **Quota limits**  in Customer Insights. More information: [Quota limits](quota-management.md)

## Add Customer Insights to your Microsoft 365 tenant

There are several ways to get a Customer Insights license. You can purchase it from the [Dynamics 365 Customer Insights overview page](https://dynamics.microsoft.com/marketing/overview/), or by going to **Billing** > **Purchase services** in your Microsoft 365 admin center, or by contacting your Microsoft sales representative or channel partner. After you've purchased a license and it's been added to your tenant, you’ll find it in the Power Platform Admin Center under **Resources** > **Dynamics 365 apps**.

You can have any number of Customer Insights licenses available on your tenant. You can access the installation management experience for any of these licenses in the Power Platform Admin Center under **Resources** > **Dynamics 365 apps**.

## Install, uninstall, or update Customer Insights

After purchasing your Customer Insights license, you can access the installation management page and choose where you want to install Customer Insights – Journeys and Customer Insights – Data.

> [!NOTE]
> If you own the legacy Dynamics 365 Marketing license, the application installation entitlement from that business model applies, which allows one application installation per license purchased. If you own the new Dynamics 365 Customer Insights license, it entitles you to install the Customer Insights - Journeys and Customer Insights - Data applications each four times on your existing Dataverse environments.

To set up a new Customer Insights environment:

1.If you have not installed other Dynamics 365 apps on the [Microsoft Power Platform admin center](/power-platform/admin/), go to [**admin.powerplatform.microsoft.com**](https://admin.powerplatform.microsoft.com) to create an environment of the desired type (production, sandbox, developer, or trial). Learn more: [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment).
1. On [**admin.powerplatform.microsoft.com**](https://admin.powerplatform.microsoft.com), find the Dynamics 365 apps list in the left-hand site map and select **Resources**.
    - Whether you have the legacy, standalone Dynamics 365 Customer Insights app or Dynamics 365 Marketing licenses (available to customers who purchased before September 2023) or the new, combined Dynamics 365 Customer Insights license that entitles you to install both the Customer Insights - Journeys and Customer Insights - Data applications, you can find them listed in admin.powerplatform.microsoft.com under **Dynamics 365 apps** > **Resources**.

1. To open the installation management area, select the three dots dropdown ("**...**") then select **Manage**.

1. In the installation management area, you'll see your available environments listed and can choose where you want to install Customer Insights - Journeys or Customer Insights - Data.

    > [!div class="mx-imgBorder"]
    > ![Installation management area screenshot.](media/new-installation.png "Installation management area screenshot")

1. After you've installed the Customer Insights - Journeys and Customer Insights - Data apps on the same environment, you need to finish connecting them. To connect the apps, go to **Customer Insights - Journeys** then go to **Settings** > **Data Management** > **Customer Insights** and select the **Connect'** button. This completes the data sync for segmentation between the two applications.

## Maintain or update your installation

In addition to helping you install Customer Insights for the first time, you can access the installation management area to modify, maintain, or update your installation. You can do all of the following:

- Check for and apply [updates](apply-updates.md)
- Fix installation issues
- Connect a disconnected instance to marketing services
- Clean up after a [copy or restore operation](copy-or-restore.md)
- [Uninstall](uninstall.md) Customer Insights - Journeys

## Privacy notice

[!INCLUDE[cc-privacy-marketing-fre](./includes/cc-privacy-marketing-fre.md)]

[!INCLUDE[footer-include](./includes/footer-banner.md)]