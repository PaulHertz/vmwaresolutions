---

copyright:

  years:  2016, 2021

lastupdated: "2021-09-10"

keywords: troubleshooting, configuration issue, ESXi server issue

subcollection: vmwaresolutions

---

{{site.data.keyword.attribute-definition-list}}

# Why does the ESXi server display a message about management network redundancy?
{: #trbl_host_displays_warning_msg}
{: troubleshoot}
{: support}

A configuration issue is displayed in the **Issues** tab of the **Monitor** tab of the VMware ESXi® server in the vSphere client.
{: tsSymptoms}

The following message is displayed in the **Issues** tab for the ESXi server:

`This host currently has no management network redundancy`

The message is displayed even though two uplinks are available for the private distributed switch, which provides a redundancy.

This configuration issue is a VMware® known issue.
{: tsCauses}

To resolve the problem, follow the instructions in [ESX/ESXi host displays warning message when test condition is false (2008602)](https://kb.vmware.com/s/article/2008602){: external}.
{: tsResolve}
