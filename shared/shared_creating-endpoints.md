---

copyright:

  years:  2021

lastupdated: "2021-09-23"

keywords: VMware Solutions Shared create private network endpoint

subcollection: vmwaresolutions

---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Creating a private network endpoint
{: #shared_creating-endpoints}

{{site.data.keyword.cloud}} for VMware® Solutions Shared now supports both public and private network endpoints. The public network endpoints that are provisioned by default are the five public IP addresses that are displayed in the VMware Solutions Shared virtual data center detail page. A private network endpoint allows a customer's {{site.data.keyword.cloud_notm}} account devices or resources to connect to their virtual data centers by using the {{site.data.keyword.cloud}} private network. The **Private network endpoint** service is available and ready-to-use in all provisioned virtual data centers. After it is configured, the service allows your {{site.data.keyword.cloud_notm}} account resources to connect to virtual machines (VMs) in your virtual data center over the {{site.data.keyword.cloud_notm}} private network.

Connections to private network endpoints do not require public internet access. A private network endpoint provides a unique IP address that is accessible to you without a VPN connection. Private network endpoints support one-way traffic from {{site.data.keyword.cloud_notm}} account resources to the VMs in your virtual data center.

Service charges are incurred only if you choose to use the service.
{: note}

## Before you create a private network endpoint
{: #shared_creating-endpoints-prereq}

* If you have an {{site.data.keyword.cloud_notm}} Direct Link on your account, you must establish a tunnel between the cross-connect router and the customer edge to have access to the virtual data center.
* You can order only one private network endpoint per virtual data center.
* If you want to change the device type of your private network endpoint, you must first delete the existing private network endpoint. Then, create a new private network endpoint with the new device type.
* You can simultaneously make resource updates to your virtual data center while you create or delete a private network endpoint.

## System settings
{: #shared_creating-endpoints-sys-settings}

When you create a private network endpoint, you must specify the following settings.

### Device type
{: #shared_creating-endpoints-sys-settings-device}

Select from the following device type options:

* Multi-tenant
* Dedicated with 1 Gbps uplinks
* Dedicated with 10 Gbps uplinks

You are not charged for the multi-tenant option.
{: note}

### Allowlisted IP addresses and subnets
{: #shared_creating-endpoints-sys-settings-ip-subnet}

Add the IP addresses or subnets you want to have access to the private network endpoint.

## Monthly cost
{: #shared_creating-endpoints-cost}

Based on your selected configuration for the private network endpoint, the estimated monthly cost is instantly generated and displayed.

You can also add the provisioned resources to the {{site.data.keyword.cloud_notm}} estimate tool, by clicking **Add to estimate**. The tool is useful if you want to estimate the price of the selected VMware Solutions Shared resources together with other {{site.data.keyword.cloud_notm}} resources that you might consider purchasing.

## Procedure to create a private network endpoint for a virtual data center
{: #shared_creating-endpoints-add-procedure}

1. From the {{site.data.keyword.vmwaresolutions_short}} console, click **Resources** from the left navigation pane.
2. In the **VMware Solutions Shared** table, click the virtual data center where you want to create a private network endpoint.
3. Under **Private network endpoint** on the virtual data center details page, click **Create a private network endpoint**.
4. Complete the following configuration in the **Create new private network endpoint** pane.
   1. Select the device type.
   2. Provide the IP addresses or subnets to allowlist.
   3. Click **Create**.

For more information about creating a private network endpoint and to review an example of a successful configuration, see [Order a Private Network Endpoint (PNE) to connect your IBM account to your IBM VMWare Solutions Shared virtual datacenter](https://mlwiles.github.io/vmwaresolutions/vcd/order-pne/){: external}.

## Results after you create a private network endpoint for a virtual data center
{: #shared_creating-endpoints-add-procedure-results}

1. The status of the private network endpoint is changed to **Creating**.
2. When the private network endpoint is created, the status changes to **ReadyToUse**.
3. After you create a private network endpoint for your virtual data center, you can use the private network endpoint to create an IPsec tunnel between your IBM account and the virtual data center. For more information, see [IPsec Tunnel over IBM Private Network Endpoint (PNE)](https://mlwiles.github.io/vmwaresolutions/vcd/ipsec-pne/){: external}.

## Related links
{: #shared_creating-endpoints-related}

* [Operating VMware Solutions Shared](/docs/vmwaresolutions?topic=vmwaresolutions-shared_vcd-ops-guide)
* [VMware Solutions Shared pricing](/docs/vmwaresolutions?topic=vmwaresolutions-shared_pricing)
* [Viewing a private network endpoint for a virtual data center](/docs/vmwaresolutions?topic=vmwaresolutions-shared_viewing-endpoints)
* [Modifying a private network endpoint for a virtual data center](/docs/vmwaresolutions?topic=vmwaresolutions-shared_modifying-endpoints)
* [Deleting a private network endpoint from a virtual data center](/docs/vmwaresolutions?topic=vmwaresolutions-shared_deleting-endpoints)

