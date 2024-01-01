# 👩‍🏭 Admin Dashboard

The admin dashboard should be checked every morning, ensuring data accuracy and integrity. This comprehensive guide is designed to assist Salesforce Admins in conducting thorough daily checks using the Admin Dashboard. The dashboard features four key areas:

{% content-ref url="general-overview.md" %}
[General Overview Dashboard](general-overview.md)
{% endcontent-ref %}
{% content-ref url="faulty-records.md" %}
[Faulty Records Dashboard](faulty-records.md)
{% endcontent-ref %}
{% content-ref url="faulty-applicant-records.md" %}
[Faulty Applicant Records Dashboard](faulty-applicant-records.md)
{% endcontent-ref %}
{% content-ref url="faulty-partner-records.md" %}
[Faulty Partner Records Dashboard](faulty-partner-records.md)
{% endcontent-ref %}

Each section includes specific reports with detailed steps for resolution, ensuring that all aspects of the system function optimally.

## Additional Information

### Helpful links component

{% content-ref url="helpful-links-component.md" %}
[helpful-links-component.md](helpful-links-component.md)
{% endcontent-ref %}

### Auto-Refresh Configuration

* **Faulty Records Dashboard and Faulty Applicant Records Dashboard**
  * These dashboards are configured to auto-refresh every morning at 8 AM.
  * The auto-refresh ensures the data presented is up-to-date for the Admin's daily check.
  * Importance: Prevents working with outdated information, which could lead to overlooked issues.
* **General Overview Dashboard and Faulty Partner Records Dashboard**
  * Require manual refreshing to view the most current data.
  * The Admin must remember to manually refresh these dashboards each morning.
  * This step is crucial as these dashboards do not update automatically due to org limitations on dashboard subscriptions.
  * Consequence: Neglecting this step could result in reviewing stale data and missing new critical issues.

***

## Conclusion

Daily checks are vital for a Salesforce Admin to maintain system health and ensure data accuracy. This detailed guide provides step-by-step instructions for resolving issues highlighted in the Admin Dashboard reports, thereby enhancing the overall efficiency of the Salesforce environment.
