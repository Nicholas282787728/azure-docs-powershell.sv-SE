---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414715"
---
# <span data-ttu-id="b21a6-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="b21a6-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="b21a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b21a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b21a6-103">Hämta alla upptäckta servrar i ett migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="b21a6-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="b21a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b21a6-104">SYNTAX</span></span>

### <span data-ttu-id="b21a6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b21a6-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b21a6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b21a6-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b21a6-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="b21a6-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b21a6-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="b21a6-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b21a6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b21a6-109">DESCRIPTION</span></span>
<span data-ttu-id="b21a6-110">Skaffa Azure Migrate Server-cmdleten hämtar alla servrar i ett migrerat projekt.</span><span class="sxs-lookup"><span data-stu-id="b21a6-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="b21a6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b21a6-111">EXAMPLES</span></span>

### <span data-ttu-id="b21a6-112">Exempel 1: lista</span><span class="sxs-lookup"><span data-stu-id="b21a6-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="b21a6-113">Hämta alla servrar i ett migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="b21a6-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="b21a6-114">Exempel 2: get</span><span class="sxs-lookup"><span data-stu-id="b21a6-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="b21a6-115">Skaffa en server i ett migrera projekt efter namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="b21a6-116">Name är ett unikt paramenter för en server.</span><span class="sxs-lookup"><span data-stu-id="b21a6-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="b21a6-117">Exempel 3: lista i en apparat</span><span class="sxs-lookup"><span data-stu-id="b21a6-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="b21a6-118">Lista alla servrar för en apparat i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b21a6-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="b21a6-119">Exempel 4: skaffa en apparat</span><span class="sxs-lookup"><span data-stu-id="b21a6-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="b21a6-120">Skaffa en server för en apparat i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="b21a6-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="b21a6-121">Name är ett unikt paramenter för en server.</span><span class="sxs-lookup"><span data-stu-id="b21a6-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="b21a6-122">Exempel 5: lista och filtrera efter visnings namn</span><span class="sxs-lookup"><span data-stu-id="b21a6-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="b21a6-123">Visa servrar i ett migrera projekt och filtrera svar med visnings namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="b21a6-124">Exempel 6: lista i en apparat och filtrera efter visnings namn</span><span class="sxs-lookup"><span data-stu-id="b21a6-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="b21a6-125">Lista servrar för en enhet i ett migrera projekt och filtrera svar med visnings namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="b21a6-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b21a6-126">PARAMETERS</span></span>

### <span data-ttu-id="b21a6-127">-ApplianceName</span><span class="sxs-lookup"><span data-stu-id="b21a6-127">-ApplianceName</span></span>
<span data-ttu-id="b21a6-128">Anger namnet på apparaten.</span><span class="sxs-lookup"><span data-stu-id="b21a6-128">Specifies the appliance name.</span></span>
<span data-ttu-id="b21a6-129">Det här kan mappas internt till en webbplats.</span><span class="sxs-lookup"><span data-stu-id="b21a6-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b21a6-130">-DisplayName</span></span>
<span data-ttu-id="b21a6-131">Anger visnings namnet för VMware-datorn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="b21a6-132">-Name</span></span>
<span data-ttu-id="b21a6-133">Anger VMware-datorns namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="b21a6-134">Det här är ett internt namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-134">This is an internal Name.</span></span>
<span data-ttu-id="b21a6-135">För användare, Använd visnings namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-136">-Projektetsnamn</span><span class="sxs-lookup"><span data-stu-id="b21a6-136">-ProjectName</span></span>
<span data-ttu-id="b21a6-137">Anger det migrerande projekt namnet.</span><span class="sxs-lookup"><span data-stu-id="b21a6-137">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b21a6-138">-ResourceGroupName</span></span>
<span data-ttu-id="b21a6-139">Anger resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b21a6-139">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b21a6-140">-SubscriptionId</span></span>
<span data-ttu-id="b21a6-141">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="b21a6-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a6-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b21a6-142">-Confirm</span></span>
<span data-ttu-id="b21a6-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b21a6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21a6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21a6-144">-WhatIf</span></span>
<span data-ttu-id="b21a6-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b21a6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21a6-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b21a6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21a6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21a6-147">CommonParameters</span></span>
<span data-ttu-id="b21a6-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b21a6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21a6-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b21a6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21a6-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b21a6-150">INPUTS</span></span>

## <span data-ttu-id="b21a6-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b21a6-151">OUTPUTS</span></span>

### <span data-ttu-id="b21a6-152">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api202001. IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="b21a6-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="b21a6-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b21a6-153">NOTES</span></span>

<span data-ttu-id="b21a6-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b21a6-154">ALIASES</span></span>

## <span data-ttu-id="b21a6-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b21a6-155">RELATED LINKS</span></span>

