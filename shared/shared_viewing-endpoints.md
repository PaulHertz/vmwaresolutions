---

copyright:

  years:  2021

lastupdated: "2021-09-23"

keywords: VMware Solutions Shared view private network endpoint

subcollection: vmwaresolutions

---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Viewing a private network endpoint for a virtual data center
{: #shared_viewing-endpoints}

You can view the details of a private network endpoint for a virtual data center.

## Procedure to view a private network endpoint for a virtual data center
{: #shared_viewing-endpoints-procedure}

1. From the {{site.data.keyword.vmwaresolutions_short}} console, click **Resources** from the left navigation pane.
2. In the **VMware Solutions Shared** table, click a virtual data center name.
3. View the **Private network endpoint** details. Expand **Allow listed IPs and subnets** to view the list of IP addresses and subnets that you added when you ordered the private network endpoint.

| Item          | Description   |
|:------------- |:------------- |
| Device type | The multi-tenant or dedicated device and size. |
| Service network IP | The IP address for the service network. |
| Private network IP | The IP address for the private network. |
| Service address | The IP address that your virtual data center is allocated for {{site.data.keyword.cloud_notm}} access. |
| Allow listed IPs and subnets | The list of all allow listed IP addresses and subnets for the virtual data center. |
{: caption="Table 1. Private network endpoint items" caption-side="top"}

The **Service address** is available only when you select the *Dedicated 1 Gbps uplinks* or *Dedicated 10 Gbps uplinks* **Device type** when you order the private network endpoint.
{: note}

The private network endpoint can have different statuses.

| Status        | Description   |
|:------------- |:------------- |
| Creating | The private network endpoint is being created. |
| Ready to use | The private network endpoint is operating. |
| Deleting | The private network endpoint is being deleted. |
| Deleted | The private network endpoint is deleted. |
{: caption="Table 2. Status descriptions for a private network endpoint" caption-side="top"}

## Related links
{: #shared_viewing-endpoints-related}

* [Operating VMware Solutions Shared](/docs/vmwaresolutions?topic=vmwaresolutions-shared_vcd-ops-guide)
* [VMware Solutions Shared pricing](/docs/vmwaresolutions?topic=vmwaresolutions-shared_pricing)
* [Creating a private network endpoint](/docs/vmwaresolutions?topic=vmwaresolutions-shared_creating-endpoints)
* [Modifying a private network endpoint for a virtual data center](/docs/vmwaresolutions?topic=vmwaresolutions-shared_modifying-endpoints)
* [Deleting a private network endpoint from a virtual data center](/docs/vmwaresolutions?topic=vmwaresolutions-shared_deleting-endpoints)
