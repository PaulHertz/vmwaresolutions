---

copyright:

  years:  2020, 2021

lastupdated: "2021-09-23"

keywords: VMware Solutions Shared delete instance, delete VMware Solutions Shared, remove VMware Solutions Shared

subcollection: vmwaresolutions

---

{:tip: .tip}
{:note: .note}
{:important: .important}

# Deleting virtual data centers
{: #shared_deletinginstance}

You can delete a virtual data center when it's in the **Ready To Use** state.

Before you delete your virtual data center, ensure that any items that you created within the are removed. Items might include the following artifacts:

* vApps, vApp templates, and virtual machines (VMs). You must remove these items even if they are stopped.
* Organization networks that are removed or unshared from the virtual data center
* Organization catalogs
* DHCP pools created within the Organization virtual data center edge gateway
* Custom routes that are defined on the Organization virtual data center edge gateway distributed router
* Load balancer custom configurations defined on the Organization virtual data center edge gateway
* VPN custom configurations defined on the Organization virtual data center edge gateway

## Considerations when you delete virtual data centers
{: #shared_deletinginstance-considerations}

All of the virtual data center VM restore points in Veeam are automatically deleted when you delete a {{site.data.keyword.cloud}} for VMware® Solutions Shared virtual data center.
{: important}

Any job that includes instructions to backup the VM fails when the VM restore points in Veeam are deleted. However, the existing VMs in the job are still backed up, the job status is marked as failed. To remove the failed status, you must manually edit the job to remove the instruction to back up the now deleted VMs.

## Procedure to delete virtual data centers from the Resources page
{: #shared_deletinginstance-procedure1}

1. From the {{site.data.keyword.vmwaresolutions_full}} console, click **Resources** from the left navigation pane.
2. In the **VMware Solutions Shared** table, find the virtual data center to delete.
3. Click the vertical overflow menu next to the **Status** column, and then click **Delete instance**.
   The status of the virtual data center is changed to **Deleting**. When the virtual data center is deleted successfully, the components of the virtual data center are released, and the status is changed to **Deleted**.

## Procedure to delete virtual data centers from the virtual data center details page
{: #shared_deletinginstance-procedure2}

1. From the {{site.data.keyword.vmwaresolutions_short}} console, click **Resources** from the left navigation pane.
2. In the **VMware Solutions Shared** table, click the virtual data center to delete.
3. Click **Actions** next to **vCenter console**, and then click **Delete instance**.
   The status of the virtual data center is changed to **Deleting**. When the virtual data center is deleted successfully, the components of the virtual data center are released, and the status is changed to **Deleted**.
4. If you want to delete the virtual data center record from the {{site.data.keyword.vmwaresolutions_short}} console, complete the following steps:
   1. Click **Actions** again and then click **Delete from the console**.
   2. In the **Delete instance** window, click **Delete**.

## Related links
{: #shared_deletinginstance-related}

* [Ordering virtual data centers](/docs/vmwaresolutions?topic=vmwaresolutions-shared_ordering)
* [Viewing and managing virtual data centers](/docs/vmwaresolutions?topic=vmwaresolutions-shared_viewing-vdc-summary)
* [Operating VMware Solutions Shared](/docs/vmwaresolutions?topic=vmwaresolutions-shared_vcd-ops-guide)
* [VMware vCloud Director](https://www.vmware.com/ca/products/vcloud-director.html){: external}
* [Contacting IBM Support](/docs/vmwaresolutions?topic=vmwaresolutions-trbl_support)
