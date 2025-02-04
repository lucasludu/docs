---
title: Secret scanning partners
intro: 'Lists of supported secrets and the partners that {% data variables.product.company_short %} works with to prevent fraudulent use of secrets that were committed accidentally.'
product: '{% data reusables.gated-features.secret-scanning %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: reference
topics:
  - Secret scanning
  - Advanced Security
---

{% data reusables.secret-scanning.beta %}
{% data reusables.secret-scanning.enterprise-enable-secret-scanning %}

{% ifversion fpt or ghec %}
## List of supported secrets for public repositories

{% data variables.product.product_name %} 当前会扫描公共仓库，查找以下服务提供商发布的密码。

{% data reusables.secret-scanning.partner-secret-list-public-repo %}
{% endif %}

{% ifversion fpt %}
Organizations using {% data variables.product.prodname_ghe_cloud %} with {% data variables.product.prodname_GH_advanced_security %} can run {% data variables.product.prodname_secret_scanning %} on private repositories. For more information, see the [{% data variables.product.prodname_ghe_cloud %} documentation](/enterprise-cloud@latest/code-security/secret-scanning/secret-scanning-partners).
{% endif %}

{% ifversion ghec or ghae or ghes %}
## List of supported secrets {% ifversion ghec %}for private repositories{% endif %}

{% ifversion ghes > 3.1 or ghae or ghec %}
{% note %}

**Note:** You can also define custom {% data variables.product.prodname_secret_scanning %} patterns that only apply to your repository or organization. 更多信息请参阅“[定义 {% data variables.product.prodname_secret_scanning %} 的自定义模式](/code-security/secret-security/defining-custom-patterns-for-secret-scanning)”。

{% endnote %}
{% endif %}

{% data variables.product.prodname_dotcom %}  目前扫描{% ifversion ghec %}私有{% endif %}仓库，以检查由以下服务提供者颁发的密码。

{% data reusables.secret-scanning.partner-secret-list-private-repo %}
{% endif %}

## 延伸阅读

- "[保护您的仓库](/code-security/getting-started/securing-your-repository)"
- "[保护帐户和数据安全](/github/authenticating-to-github/keeping-your-account-and-data-secure)"
{%- ifversion fpt or ghec %}
- "[{% data variables.product.prodname_secret_scanning_caps %} partner program](/developers/overview/secret-scanning-partner-program)"
{%- else %}
- "[{% data variables.product.prodname_secret_scanning_caps %} partner program](/free-pro-team@latest/developers/overview/secret-scanning-partner-program)" in the {% data variables.product.prodname_ghe_cloud %} documentation
{% endif %}
