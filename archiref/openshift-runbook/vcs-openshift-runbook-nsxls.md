---

copyright:

  years:  2019, 2021

lastupdated: "2021-08-10"

subcollection: vmwaresolutions


---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}

# OpenShift NSX logical switches configuration
{: #openshift-runbook-runbook-nsxls-intro}

Review the NSX logical switches that are used to support the OpenShift 4.7 environment. To use this information, you must understand how to create these components and add the configuration.

Review [Add a logical switch](https://docs.vmware.com/en/VMware-NSX-Data-Center-for-vSphere/6.4/com.vmware.nsx.admin.doc/GUID-295720D5-DD75-4523-9095-1D694D99717A.html){: external}. PowerNSX commands are provided if you would want to use this method.

## NSX Logical Switches
{: #openshift-runbook-runbook-nsxls-config}

The design requires two NSX Logical Switches:

* Transit - This logical switch is used to connect the DLR and the ESGs. The DLR Control VMs have an interface on this network.
* OpenShift - This logical switch is used for the OpenShift VM network. The DLR has a connection to this logical switch.
* HA - This logical switch is used for the DLR Control VMs. You do not need to assign an IP range to this network as NSX assigns internal IP range to it.

## PowerNSX commands
{: #openshift-runbook-runbook-nsxls-powernsx}

Review the example of PowerNSX commands that you can use to automate the provisioning and configuration of the NSX logical switches.

Use the following table to document the parameters you need for your deployment, examples are shown that match the deployment described previously.

| Parameters | Example | Your deployment |
|:---------- |:------- |:--------------- |
| vCenter Server IP address | | |
| vCenter Server user | | |
| vCenter Server password | | |
| NSX Transport Zone| transport-1 | |
{: caption="Table 1. PowerNSX LS Parameters" caption-side="top"}

```powernsx
# Allow self-signed certificates on PowerCLI
Set-PowerCLIConfiguration -InvalidCertificateAction:Ignore

# Connect to NSX Manager
Connect-NsxServer -vCenterServer <IP_Address> -User <UserName> -Password '<Password>'

# Create logical switches
Get-NsxTransportZone transport-1 | new-nsxlogicalswitch -Name OpenShift-LS -Description "OpenShift network"
Get-NsxTransportZone transport-1 | new-nsxlogicalswitch -Name OpenShift-Transit -Description "OpenShift transit network"
Get-NsxTransportZone transport-1 | new-nsxlogicalswitch -Name OpenShift-HA -Description "OpenShift DLR HA network"

# Disconnect
Disconnect-NsxServer
```

**Next topic:** [Red Hat OpenShift NSX Edge configuration](/docs/vmwaresolutions?topic=vmwaresolutions-openshift-runbook-runbook-nsxedge-intro)

## Related links
{: #vcs-openshift-runbook-nsxdls-related}

* [OpenShift Bastion node setup](/docs/vmwaresolutions?topic=vmwaresolutions-openshift-runbook-runbook-bastion-intro)
* [Red Hat OpenShift 4.7 user provider infrastructure installation](/docs/vmwaresolutions?topic=vmwaresolutions-openshift-runbook-runbook-install-intro)
