---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260181"
---
# <span data-ttu-id="bec86-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bec86-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="bec86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bec86-102">SYNOPSIS</span></span>
<span data-ttu-id="bec86-103">Lägger till en Access-Restiction regel i en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bec86-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="bec86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bec86-104">SYNTAX</span></span>

### <span data-ttu-id="bec86-105">IpAddressParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bec86-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bec86-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec86-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec86-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec86-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec86-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bec86-108">DESCRIPTION</span></span>
<span data-ttu-id="bec86-109">Cmdleten **Add-AzWebAppAccessRestrictionRule** lägger till en åtkomst begränsnings regel i en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bec86-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="bec86-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bec86-110">EXAMPLES</span></span>

### <span data-ttu-id="bec86-111">Exempel 1: lägga till en begränsnings regel för IP-adresser i ett webb program</span><span class="sxs-lookup"><span data-stu-id="bec86-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="bec86-112">Det här kommandot lägger till en åtkomst begränsnings regel med prioritet 200 och IP-intervall till ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="bec86-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="bec86-113">Exempel 2: Lägg till begränsnings regeln åtkomst gräns för under näts tjänst till ett webb program</span><span class="sxs-lookup"><span data-stu-id="bec86-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="bec86-114">Det här kommandot lägger till en begränsnings regel för åtkomst med 300 och under nätet appgw-delnät i Corp-VNet till ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="bec86-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bec86-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bec86-115">PARAMETERS</span></span>

### <span data-ttu-id="bec86-116">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="bec86-116">-Action</span></span>
<span data-ttu-id="bec86-117">Regeln Tillåt eller neka.</span><span class="sxs-lookup"><span data-stu-id="bec86-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="bec86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec86-118">-DefaultProfile</span></span>
<span data-ttu-id="bec86-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bec86-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec86-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="bec86-120">-Description</span></span>
<span data-ttu-id="bec86-121">Beskrivning av åtkomst begränsningen.</span><span class="sxs-lookup"><span data-stu-id="bec86-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="bec86-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bec86-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="bec86-123">Ange om tjänst slut punkts registrering på undernät ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="bec86-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="bec86-124">-IpAddress</span></span>
<span data-ttu-id="bec86-125">IP Address v4 eller V6 CIDR-intervall.</span><span class="sxs-lookup"><span data-stu-id="bec86-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="bec86-126">T. ex.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="bec86-126">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="bec86-127">-Name</span></span>
<span data-ttu-id="bec86-128">Regel namn</span><span class="sxs-lookup"><span data-stu-id="bec86-128">Rule Name</span></span>

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

### <span data-ttu-id="bec86-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec86-129">-PassThru</span></span>
<span data-ttu-id="bec86-130">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="bec86-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="bec86-131">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="bec86-131">-Priority</span></span>
<span data-ttu-id="bec86-132">Prioritet för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="bec86-132">Access Restriction priority.</span></span> <span data-ttu-id="bec86-133">T. 500.</span><span class="sxs-lookup"><span data-stu-id="bec86-133">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec86-134">-ResourceGroupName</span></span>
<span data-ttu-id="bec86-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bec86-135">Resource Group Name</span></span>

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

### <span data-ttu-id="bec86-136">-SlotName</span><span class="sxs-lookup"><span data-stu-id="bec86-136">-SlotName</span></span>
<span data-ttu-id="bec86-137">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="bec86-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="bec86-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bec86-138">-SubnetId</span></span>
<span data-ttu-id="bec86-139">ResourceId för undernät.</span><span class="sxs-lookup"><span data-stu-id="bec86-139">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bec86-140">-SubnetName</span></span>
<span data-ttu-id="bec86-141">Namn på under nätet.</span><span class="sxs-lookup"><span data-stu-id="bec86-141">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="bec86-142">-TargetScmSite</span></span>
<span data-ttu-id="bec86-143">Regeln är avsedd för huvud webbplatsen eller SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="bec86-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="bec86-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bec86-144">-VirtualNetworkName</span></span>
<span data-ttu-id="bec86-145">Namn på virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="bec86-145">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec86-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="bec86-146">-WebAppName</span></span>
<span data-ttu-id="bec86-147">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="bec86-147">The name of the web app.</span></span>

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

### <span data-ttu-id="bec86-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bec86-148">-Confirm</span></span>
<span data-ttu-id="bec86-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bec86-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec86-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec86-150">-WhatIf</span></span>
<span data-ttu-id="bec86-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bec86-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bec86-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bec86-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec86-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec86-153">CommonParameters</span></span>
<span data-ttu-id="bec86-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec86-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec86-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bec86-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec86-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bec86-156">INPUTS</span></span>

### <span data-ttu-id="bec86-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bec86-157">System.String</span></span>

## <span data-ttu-id="bec86-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bec86-158">OUTPUTS</span></span>

### <span data-ttu-id="bec86-159">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bec86-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="bec86-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bec86-160">NOTES</span></span>

## <span data-ttu-id="bec86-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bec86-161">RELATED LINKS</span></span>

[<span data-ttu-id="bec86-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bec86-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="bec86-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bec86-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="bec86-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bec86-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
