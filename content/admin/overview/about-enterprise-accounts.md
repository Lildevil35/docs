---
title: About enterprise accounts
intro: 'With {% data variables.product.product_name %}, you can use an enterprise account to {% ifversion ghec %}enable collaboration between your organizations, while giving{% elsif ghes or ghae %}give{% endif %} administrators a single point of visibility and management.'
redirect_from:
  - /articles/about-github-business-accounts
  - /articles/about-enterprise-accounts
  - /enterprise/admin/installation/about-enterprise-accounts
  - /enterprise/admin/overview/about-enterprise-accounts
  - /github/setting-up-and-managing-your-enterprise-account/about-enterprise-accounts
  - /github/setting-up-and-managing-your-enterprise/about-enterprise-accounts
  - /github/setting-up-and-managing-your-enterprise/managing-your-enterprise-account/about-enterprise-accounts
versions:
  ghec: '*'
  ghes: '*'
type: overview
topics:
  - Accounts
  - Enterprise
  - Fundamentals
---

## About enterprise accounts on {% ifversion ghec %}{% data variables.product.prodname_ghe_cloud %}{% else %}{% data variables.product.product_name %}{% endif %}

{% ifversion ghec %}

Your enterprise account on {% data variables.product.prodname_dotcom_the_website %} allows you to manage multiple organizations. Your enterprise account must have a handle, like an organization or user account on {% data variables.product.prodname_dotcom %}.

{% elsif ghes or ghae %}

The enterprise account on {% ifversion ghes %}{% data variables.location.product_location_enterprise %}{% elsif ghae %}{% data variables.product.product_name %}{% endif %} allows you to manage the organizations{% ifversion ghes %} on{% elsif ghae %} owned by{% endif %} your {% ifversion ghes %}{% data variables.product.prodname_ghe_server %} instance{% elsif ghae %}enterprise{% endif %}.

{% endif %}

Organizations are shared accounts where enterprise members can collaborate across many projects at once. Organization owners can manage access to the organization's data and projects with sophisticated security and administrative features. For more information, see "[AUTOTITLE](/organizations/collaborating-with-groups-in-organizations/about-organizations)."

{% ifversion ghec %}
In the enterprise settings, enterprise owners can invite existing organizations to join your enterprise account, transfer organizations between enterprise accounts, or create new organizations. For more information, see "[AUTOTITLE](/admin/user-management/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise)."
{% endif %}

Your enterprise account allows you to manage and enforce policies for all the organizations owned by the enterprise. {% data reusables.enterprise.about-policies %} For more information, see "[AUTOTITLE](/admin/policies/enforcing-policies-for-your-enterprise/about-enterprise-policies)."

{% ifversion ghec %}

{% data reusables.enterprise.create-an-enterprise-account %} For more information, see "[AUTOTITLE](/admin/managing-your-enterprise-account/creating-an-enterprise-account)."

{% endif %}

## About administration of your enterprise account

{% ifversion ghes or ghae %}

From your enterprise account on {% ifversion ghae %}{% data variables.product.product_name %}{% elsif ghes %}a {% data variables.product.prodname_ghe_server %} instance{% endif %}, administrators can view{% ifversion remove-enterprise-members %} and manage{% endif %} enterprise membership{% ifversion enterprise-owner-join-org %}, manage their own membership in organizations owned by the enterprise,{% endif %} and manage the following for the {% ifversion ghes %}{% data variables.product.prodname_ghe_server %} instance{% elsif ghae %}enterprise on {% data variables.product.prodname_ghe_managed %}{% endif %}.

{% ifversion ghes %}
- License usage{% endif %}
- Security ({% ifversion ghae %}single sign-on, IP allow lists, {% endif %}SSH certificate authorities, two-factor authentication)
- Enterprise policies for organizations owned by the enterprise account

{% endif %}

{% ifversion ghes %}
{% note %}

**Notes:**

- Changing the enterprise display name in the settings for {% data variables.location.product_location %} will not change the enterprise name in {% data variables.location.product_location %} URL. The enterprise name in your instance's URL is generated based on the customer name in the {% data variables.product.prodname_ghe_server %} license file.
- There is only one default enterprise account for {% data variables.product.prodname_ghe_server %}. You cannot create additional enterprise accounts.

{% endnote %}

### About administration of your enterprise account on {% data variables.product.prodname_ghe_cloud %}

{% endif %}

{% ifversion ghec or ghes %}When you try or purchase {% data variables.product.prodname_enterprise %}, you can{% ifversion ghes %} also{% endif %} create an enterprise account for {% data variables.product.prodname_ghe_cloud %} on {% data variables.product.prodname_dotcom_the_website %}. Administrators for the enterprise account on {% data variables.product.prodname_dotcom_the_website %} can view {% ifversion remove-enterprise-members %} and manage{% endif %} enterprise membership{% ifversion enterprise-owner-join-org %}, manage their own membership in organizations owned by the enterprise,{% endif %} and manage the following for the enterprise account{% ifversion ghes %} on {% data variables.product.prodname_dotcom_the_website %}{% endif %}.

- Billing and usage (services on {% data variables.product.prodname_dotcom_the_website %}, {% data variables.product.prodname_GH_advanced_security %}, user licenses)
- Security (single sign-on, IP allow lists, SSH certificate authorities, two-factor authentication)
- Enterprise policies for organizations owned by the enterprise account

If you use both {% data variables.product.prodname_ghe_cloud %} and {% data variables.product.prodname_ghe_server %}, you can also manage the following for {% data variables.product.prodname_ghe_server %} from your enterprise account on {% data variables.product.prodname_dotcom_the_website %}.

- Billing and usage for {% data variables.product.prodname_ghe_server %} instances
- Requests and support bundle sharing with {% data variables.contact.enterprise_support %}

You can also connect the enterprise account on {% data variables.location.product_location_enterprise %} to your enterprise account on {% data variables.product.prodname_dotcom_the_website %} to see license usage details for your {% data variables.product.prodname_enterprise %} subscription from {% data variables.product.prodname_dotcom_the_website %}. For more information, see {% ifversion ghec %}"[AUTOTITLE](/enterprise-server@latest/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud)" in the {% data variables.product.prodname_ghe_server %} documentation.{% elsif ghes %}"[AUTOTITLE](/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud)."{% endif %}

For more information about the differences between {% data variables.product.prodname_ghe_cloud %} and {% data variables.product.prodname_ghe_server %}, see "[AUTOTITLE](/get-started/learning-about-github/githubs-plans)." {% data reusables.enterprise-accounts.to-upgrade-or-get-started %}

{% endif %}

## About billing for your enterprise account

The bill for your enterprise account includes the monthly cost for each member of your enterprise. The bill includes {% ifversion ghec %}any paid licenses in organizations outside of your enterprise account, subscriptions to apps in {% data variables.product.prodname_marketplace %}, {% endif %}{% ifversion ghec or ghae %}additional paid services for your enterprise{% ifversion ghec %} like data packs for {% data variables.large_files.product_name_long %},{% endif %} and{% endif %} usage for {% data variables.product.prodname_GH_advanced_security %}.

{% ifversion ghec %}

For more information about billing for your {% data variables.product.prodname_ghe_cloud %} subscription, see "[AUTOTITLE](/billing/managing-the-plan-for-your-github-account/viewing-the-subscription-and-usage-for-your-enterprise-account)" and "[AUTOTITLE](/billing/managing-your-github-billing-settings/about-billing-for-your-enterprise)."

{% elsif ghes %}

{% data reusables.enterprise-accounts.enterprise-accounts-billing %}

For more information about billing for {% ifversion ghec %}{% data variables.product.prodname_ghe_cloud %}{% else %}{% data variables.product.product_name %}{% endif %}, see "[AUTOTITLE](/billing/managing-your-github-billing-settings/about-billing-for-your-enterprise)."

{% endif %}

{% ifversion ghec or ghes %}

{% ifversion ghec %}

{% data variables.product.prodname_enterprise %} offers two deployment options. In addition to {% data variables.product.prodname_ghe_cloud %}, you can use {% data variables.product.prodname_ghe_server %} to host development work for your enterprise in your data center or supported cloud provider. {% endif %}Enterprise owners on {% data variables.product.prodname_dotcom_the_website %} can use an enterprise account to manage payment and licensing for {% data variables.product.prodname_ghe_server %} instances. For more information, see "[AUTOTITLE](/get-started/learning-about-github/githubs-plans#github-enterprise)" and "[AUTOTITLE](/billing/managing-your-license-for-github-enterprise)."

{% endif %}

## Further reading

- "[AUTOTITLE](/graphql/guides/managing-enterprise-accounts)" in the GraphQL API documentation
