---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273164"
---
# <span data-ttu-id="2eb29-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="2eb29-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="2eb29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eb29-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb29-103">Uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="2eb29-103">Update a private cloud</span></span>

## <span data-ttu-id="2eb29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eb29-104">SYNTAX</span></span>

### <span data-ttu-id="2eb29-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="2eb29-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2eb29-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2eb29-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2eb29-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eb29-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb29-108">Uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="2eb29-108">Update a private cloud</span></span>

## <span data-ttu-id="2eb29-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eb29-109">EXAMPLES</span></span>

### <span data-ttu-id="2eb29-110">Exempel 1: uppdatera storlek på privat moln efter namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="2eb29-111">Uppdatera storlek på privat moln efter namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="2eb29-112">Exempel 2: uppdatera storleken på ett privat moln genom att ange objekt</span><span class="sxs-lookup"><span data-stu-id="2eb29-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="2eb29-113">Uppdatera storlek på privat moln efter indata</span><span class="sxs-lookup"><span data-stu-id="2eb29-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="2eb29-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eb29-114">PARAMETERS</span></span>

### <span data-ttu-id="2eb29-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb29-115">-AsJob</span></span>
<span data-ttu-id="2eb29-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2eb29-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb29-117">-DefaultProfile</span></span>
<span data-ttu-id="2eb29-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb29-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="2eb29-119">-IdentitySource</span></span>
<span data-ttu-id="2eb29-120">Enkel inloggning med vCenter för att konstruera, se avsnittet anteckningar för IDENTITYSOURCE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2eb29-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eb29-121">-InputObject</span></span>
<span data-ttu-id="2eb29-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2eb29-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="2eb29-123">-Internet</span></span>
<span data-ttu-id="2eb29-124">Anslutning till Internet är aktiverat eller inaktive rad</span><span class="sxs-lookup"><span data-stu-id="2eb29-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="2eb29-125">-ManagementClusterSize</span></span>
<span data-ttu-id="2eb29-126">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="2eb29-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-127">-Name</span></span>
<span data-ttu-id="2eb29-128">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="2eb29-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2eb29-129">-NoWait</span></span>
<span data-ttu-id="2eb29-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2eb29-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb29-131">-ResourceGroupName</span></span>
<span data-ttu-id="2eb29-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2eb29-132">The name of the resource group.</span></span>
<span data-ttu-id="2eb29-133">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="2eb29-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eb29-134">-SubscriptionId</span></span>
<span data-ttu-id="2eb29-135">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2eb29-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2eb29-136">-Tag</span></span>
<span data-ttu-id="2eb29-137">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="2eb29-137">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2eb29-138">-Confirm</span></span>
<span data-ttu-id="2eb29-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2eb29-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb29-140">-WhatIf</span></span>
<span data-ttu-id="2eb29-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2eb29-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eb29-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2eb29-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb29-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb29-143">CommonParameters</span></span>
<span data-ttu-id="2eb29-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb29-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb29-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eb29-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb29-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eb29-146">INPUTS</span></span>

### <span data-ttu-id="2eb29-147">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2eb29-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2eb29-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eb29-148">OUTPUTS</span></span>

### <span data-ttu-id="2eb29-149">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="2eb29-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="2eb29-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eb29-150">NOTES</span></span>

<span data-ttu-id="2eb29-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2eb29-151">ALIASES</span></span>

<span data-ttu-id="2eb29-152">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="2eb29-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eb29-153">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="2eb29-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eb29-154">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2eb29-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eb29-155">IDENTITYSOURCE <IIdentitySource [] >: enkel inloggning för vCenter</span><span class="sxs-lookup"><span data-stu-id="2eb29-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="2eb29-156">`[Alias <String>]`: Domänens NetBIOS-namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="2eb29-157">`[BaseGroupDn <String>]`: Gruppens unika namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="2eb29-158">`[BaseUserDn <String>]`: Användarens unika namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="2eb29-159">`[Domain <String>]`: Domänens DNS-namn</span><span class="sxs-lookup"><span data-stu-id="2eb29-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="2eb29-160">`[Name <String>]`: Namnet på identitets källan</span><span class="sxs-lookup"><span data-stu-id="2eb29-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="2eb29-161">`[Password <String>]`: Lösen ordet för Active Directory-användaren med minst skrivskyddad åtkomst till bas namn för användare och grupper.</span><span class="sxs-lookup"><span data-stu-id="2eb29-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="2eb29-162">`[PrimaryServer <String>]`: Primär server-URL</span><span class="sxs-lookup"><span data-stu-id="2eb29-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="2eb29-163">`[SecondaryServer <String>]`: Sekundär server webb adress</span><span class="sxs-lookup"><span data-stu-id="2eb29-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="2eb29-164">`[Ssl <SslEnum?>]`: Skydda LDAP-kommunikation med SSL-certifikat (LDAPs)</span><span class="sxs-lookup"><span data-stu-id="2eb29-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="2eb29-165">`[Username <String>]`: ID för en Active Directory-användare med minst skrivskyddad åtkomst till bas namn för användare och grupper</span><span class="sxs-lookup"><span data-stu-id="2eb29-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="2eb29-166">INPUTOBJECT <IVMWareIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="2eb29-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eb29-167">`[AuthorizationName <String>]`: Namnet på ExpressRoute-kretsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="2eb29-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2eb29-168">`[ClusterName <String>]`: Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="2eb29-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2eb29-169">`[HcxEnterpriseSiteName <String>]`: Namnet på den HCX företags webbplatsen i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="2eb29-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2eb29-170">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="2eb29-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eb29-171">`[Location <String>]`: Azure-region</span><span class="sxs-lookup"><span data-stu-id="2eb29-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2eb29-172">`[PrivateCloudName <String>]`: Namnet på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="2eb29-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2eb29-173">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2eb29-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2eb29-174">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="2eb29-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="2eb29-175">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="2eb29-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2eb29-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eb29-176">RELATED LINKS</span></span>
