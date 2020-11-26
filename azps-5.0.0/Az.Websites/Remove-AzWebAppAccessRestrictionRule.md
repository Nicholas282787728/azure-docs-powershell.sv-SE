---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272484"
---
# <span data-ttu-id="4336b-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4336b-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="4336b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4336b-102">SYNOPSIS</span></span>
<span data-ttu-id="4336b-103">Tar bort en regel för åtkomst begränsning från en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4336b-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="4336b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4336b-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4336b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4336b-105">DESCRIPTION</span></span>
<span data-ttu-id="4336b-106">Cmdleten **Remove-AzWebAppAccessRestrictionRule** tar bort en begränsnings regel för åtkomst från en Azure Web App</span><span class="sxs-lookup"><span data-stu-id="4336b-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="4336b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4336b-107">EXAMPLES</span></span>

### <span data-ttu-id="4336b-108">Exempel 1: ta bort en begränsnings regel för webb program</span><span class="sxs-lookup"><span data-stu-id="4336b-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="4336b-109">Det här kommandot tar bort regeln för begränsning av IpRule från Azure Web App med namnet ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="4336b-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4336b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4336b-110">PARAMETERS</span></span>

### <span data-ttu-id="4336b-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="4336b-111">-Action</span></span>
<span data-ttu-id="4336b-112">Regeln Tillåt eller neka.</span><span class="sxs-lookup"><span data-stu-id="4336b-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4336b-113">-DefaultProfile</span></span>
<span data-ttu-id="4336b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4336b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4336b-115">-IpAddress</span></span>
<span data-ttu-id="4336b-116">IP Address v4 eller V6 CIDR-intervall.</span><span class="sxs-lookup"><span data-stu-id="4336b-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="4336b-117">T. ex.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="4336b-117">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4336b-118">-Name</span></span>
<span data-ttu-id="4336b-119">Namn på regel för åtkomst begränsning</span><span class="sxs-lookup"><span data-stu-id="4336b-119">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4336b-120">-PassThru</span></span>
<span data-ttu-id="4336b-121">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="4336b-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="4336b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4336b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4336b-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4336b-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4336b-124">-SlotName</span></span>
<span data-ttu-id="4336b-125">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="4336b-125">Deployment Slot Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4336b-126">-SubnetId</span></span>
<span data-ttu-id="4336b-127">ResourceId för undernät.</span><span class="sxs-lookup"><span data-stu-id="4336b-127">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4336b-128">-SubnetName</span></span>
<span data-ttu-id="4336b-129">Namn på under nätet.</span><span class="sxs-lookup"><span data-stu-id="4336b-129">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="4336b-130">-TargetScmSite</span></span>
<span data-ttu-id="4336b-131">Regeln är avsedd för huvud webbplatsen eller SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="4336b-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="4336b-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4336b-132">-VirtualNetworkName</span></span>
<span data-ttu-id="4336b-133">Namn på virtuellt nätverk (måste finnas i samma resurs grupp som Web App).</span><span class="sxs-lookup"><span data-stu-id="4336b-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="4336b-134">-WebAppName</span></span>
<span data-ttu-id="4336b-135">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="4336b-135">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4336b-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4336b-136">-Confirm</span></span>
<span data-ttu-id="4336b-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4336b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4336b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4336b-138">-WhatIf</span></span>
<span data-ttu-id="4336b-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4336b-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4336b-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4336b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4336b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4336b-141">CommonParameters</span></span>
<span data-ttu-id="4336b-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4336b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4336b-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4336b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4336b-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4336b-144">INPUTS</span></span>

### <span data-ttu-id="4336b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4336b-145">System.String</span></span>

## <span data-ttu-id="4336b-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4336b-146">OUTPUTS</span></span>

### <span data-ttu-id="4336b-147">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4336b-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="4336b-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4336b-148">NOTES</span></span>

## <span data-ttu-id="4336b-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4336b-149">RELATED LINKS</span></span>

[<span data-ttu-id="4336b-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4336b-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4336b-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4336b-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4336b-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4336b-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)