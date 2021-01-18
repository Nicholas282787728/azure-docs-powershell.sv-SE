---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522088"
---
# <span data-ttu-id="19409-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="19409-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="19409-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19409-102">SYNOPSIS</span></span>
<span data-ttu-id="19409-103">Tar bort en regel för åtkomst begränsning från en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="19409-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="19409-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19409-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19409-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19409-105">DESCRIPTION</span></span>
<span data-ttu-id="19409-106">Cmdleten **Remove-AzWebAppAccessRestrictionRule** tar bort en begränsnings regel för åtkomst från en Azure Web App</span><span class="sxs-lookup"><span data-stu-id="19409-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="19409-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19409-107">EXAMPLES</span></span>

### <span data-ttu-id="19409-108">Exempel 1: ta bort en begränsnings regel för webb program</span><span class="sxs-lookup"><span data-stu-id="19409-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="19409-109">Det här kommandot tar bort regeln för begränsning av IpRule från Azure Web App med namnet ContosoSite som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="19409-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="19409-110">Exempel 2: ta bort en begränsnings regel för webb programmet för Service märke</span><span class="sxs-lookup"><span data-stu-id="19409-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="19409-111">Det här kommandot tar bort regeln för åtkomst begränsning med ServiceTag är lika med AzureFrontDoor. backend från Azure Web App som heter ContosoSite som tillhör resurs gruppen som heter default-West.</span><span class="sxs-lookup"><span data-stu-id="19409-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="19409-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19409-112">PARAMETERS</span></span>

### <span data-ttu-id="19409-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="19409-113">-Action</span></span>
<span data-ttu-id="19409-114">Regeln Tillåt eller neka.</span><span class="sxs-lookup"><span data-stu-id="19409-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19409-115">-DefaultProfile</span></span>
<span data-ttu-id="19409-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19409-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19409-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="19409-117">-IpAddress</span></span>
<span data-ttu-id="19409-118">IP Address v4 eller V6 CIDR-intervall.</span><span class="sxs-lookup"><span data-stu-id="19409-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="19409-119">T. ex.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="19409-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="19409-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="19409-120">-Name</span></span>
<span data-ttu-id="19409-121">Namn på regel för åtkomst begränsning</span><span class="sxs-lookup"><span data-stu-id="19409-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="19409-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19409-122">-PassThru</span></span>
<span data-ttu-id="19409-123">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="19409-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="19409-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19409-124">-ResourceGroupName</span></span>
<span data-ttu-id="19409-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="19409-125">Resource Group Name</span></span>

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

### <span data-ttu-id="19409-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="19409-126">-ServiceTag</span></span>
<span data-ttu-id="19409-127">Namn på Service märke</span><span class="sxs-lookup"><span data-stu-id="19409-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="19409-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="19409-128">-SlotName</span></span>
<span data-ttu-id="19409-129">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="19409-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="19409-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="19409-130">-SubnetId</span></span>
<span data-ttu-id="19409-131">ResourceId för undernät.</span><span class="sxs-lookup"><span data-stu-id="19409-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="19409-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="19409-132">-SubnetName</span></span>
<span data-ttu-id="19409-133">Namn på under nätet.</span><span class="sxs-lookup"><span data-stu-id="19409-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="19409-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="19409-134">-TargetScmSite</span></span>
<span data-ttu-id="19409-135">Regeln är avsedd för huvud webbplatsen eller SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="19409-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="19409-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="19409-136">-VirtualNetworkName</span></span>
<span data-ttu-id="19409-137">Namn på virtuellt nätverk (måste finnas i samma resurs grupp som Web App).</span><span class="sxs-lookup"><span data-stu-id="19409-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="19409-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="19409-138">-WebAppName</span></span>
<span data-ttu-id="19409-139">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="19409-139">The name of the web app.</span></span>

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

### <span data-ttu-id="19409-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19409-140">-Confirm</span></span>
<span data-ttu-id="19409-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19409-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19409-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19409-142">-WhatIf</span></span>
<span data-ttu-id="19409-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19409-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19409-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19409-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19409-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19409-145">CommonParameters</span></span>
<span data-ttu-id="19409-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19409-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19409-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19409-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19409-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19409-148">INPUTS</span></span>

### <span data-ttu-id="19409-149">System. String</span><span class="sxs-lookup"><span data-stu-id="19409-149">System.String</span></span>

## <span data-ttu-id="19409-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19409-150">OUTPUTS</span></span>

### <span data-ttu-id="19409-151">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="19409-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="19409-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19409-152">NOTES</span></span>

## <span data-ttu-id="19409-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19409-153">RELATED LINKS</span></span>

[<span data-ttu-id="19409-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="19409-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="19409-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="19409-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="19409-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="19409-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
