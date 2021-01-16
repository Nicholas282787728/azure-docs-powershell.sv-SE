---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407603"
---
# <span data-ttu-id="38bbe-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="38bbe-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="38bbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="38bbe-103">Lägger till en Access-Restiction regel i en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="38bbe-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="38bbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38bbe-104">SYNTAX</span></span>

### <span data-ttu-id="38bbe-105">IpAddressParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="38bbe-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bbe-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bbe-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bbe-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bbe-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bbe-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bbe-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bbe-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38bbe-109">DESCRIPTION</span></span>
<span data-ttu-id="38bbe-110">Cmdleten **Add-AzWebAppAccessRestrictionRule** lägger till en åtkomst begränsnings regel i en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="38bbe-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="38bbe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38bbe-111">EXAMPLES</span></span>

### <span data-ttu-id="38bbe-112">Exempel 1: lägga till en begränsnings regel för IP-adresser i ett webb program</span><span class="sxs-lookup"><span data-stu-id="38bbe-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="38bbe-113">Det här kommandot lägger till en åtkomst begränsnings regel med prioritet 200 och IP-intervall till ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="38bbe-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="38bbe-114">Exempel 2: Lägg till begränsnings regeln åtkomst gräns för under näts tjänst till ett webb program</span><span class="sxs-lookup"><span data-stu-id="38bbe-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="38bbe-115">Det här kommandot lägger till en begränsnings regel för åtkomst med 300 och under nätet appgw-delnät i Corp-VNet till ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="38bbe-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="38bbe-116">Exempel 3: lägga till ServiceTag åtkomst begränsnings regel i ett webb program</span><span class="sxs-lookup"><span data-stu-id="38bbe-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="38bbe-117">Det här kommandot lägger till en begränsnings regel för åtkomst med 200 och ett Service märke som representerar IP-scopet för Azure-frontend till ett webb program med namnet ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="38bbe-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="38bbe-118">Exempel 4: Lägg till åtkomst begränsning för flera adresser i ett webb program</span><span class="sxs-lookup"><span data-stu-id="38bbe-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="38bbe-119">Det här kommandot lägger till en begränsnings regel för åtkomst med 200 och två IP-adressintervall till ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="38bbe-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="38bbe-120">Exempel 5: lägga till begränsnings regeln för åtkomst med HTTP-rubrik till ett webb program</span><span class="sxs-lookup"><span data-stu-id="38bbe-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="38bbe-121">Det här kommandot lägger till en åtkomst begränsnings regel med prioritet 400 för service tag AzureFrontDoor. Server märke och ytterligare begränsar åtkomsten till http-huvudena för vissa värden till ett webb program med namnet ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="38bbe-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="38bbe-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38bbe-122">PARAMETERS</span></span>

### <span data-ttu-id="38bbe-123">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="38bbe-123">-Action</span></span>
<span data-ttu-id="38bbe-124">Regeln Tillåt eller neka.</span><span class="sxs-lookup"><span data-stu-id="38bbe-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="38bbe-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bbe-125">-DefaultProfile</span></span>
<span data-ttu-id="38bbe-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38bbe-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38bbe-127">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="38bbe-127">-Description</span></span>
<span data-ttu-id="38bbe-128">Beskrivning av åtkomst begränsningen.</span><span class="sxs-lookup"><span data-stu-id="38bbe-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="38bbe-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="38bbe-129">-HttpHeader</span></span>
<span data-ttu-id="38bbe-130">Begränsningar för HTTP-huvuden.</span><span class="sxs-lookup"><span data-stu-id="38bbe-130">Http header restrictions.</span></span> <span data-ttu-id="38bbe-131">Exempel:-HttpHeader @ {' x-fdid ' = ' 7acacb02-47ea-4cd4-b568-5e880e72582e '; ' x-forwarded-Host ' = ' www.contoso.com ', ' app.contoso.com '}</span><span class="sxs-lookup"><span data-stu-id="38bbe-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="38bbe-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="38bbe-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="38bbe-133">Ange om tjänst slut punkts registrering på undernät ska verifieras.</span><span class="sxs-lookup"><span data-stu-id="38bbe-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="38bbe-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="38bbe-134">-IpAddress</span></span>
<span data-ttu-id="38bbe-135">IP Address v4 eller V6 CIDR-intervall.</span><span class="sxs-lookup"><span data-stu-id="38bbe-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="38bbe-136">T. ex.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="38bbe-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="38bbe-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="38bbe-137">-Name</span></span>
<span data-ttu-id="38bbe-138">Regel namn</span><span class="sxs-lookup"><span data-stu-id="38bbe-138">Rule Name</span></span>

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

### <span data-ttu-id="38bbe-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38bbe-139">-PassThru</span></span>
<span data-ttu-id="38bbe-140">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="38bbe-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="38bbe-141">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="38bbe-141">-Priority</span></span>
<span data-ttu-id="38bbe-142">Prioritet för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="38bbe-142">Access Restriction priority.</span></span> <span data-ttu-id="38bbe-143">T. 500.</span><span class="sxs-lookup"><span data-stu-id="38bbe-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="38bbe-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bbe-144">-ResourceGroupName</span></span>
<span data-ttu-id="38bbe-145">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="38bbe-145">Resource Group Name</span></span>

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

### <span data-ttu-id="38bbe-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="38bbe-146">-ServiceTag</span></span>
<span data-ttu-id="38bbe-147">Namn på Service märke</span><span class="sxs-lookup"><span data-stu-id="38bbe-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bbe-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="38bbe-148">-SlotName</span></span>
<span data-ttu-id="38bbe-149">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="38bbe-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="38bbe-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="38bbe-150">-SubnetId</span></span>
<span data-ttu-id="38bbe-151">ResourceId för undernät.</span><span class="sxs-lookup"><span data-stu-id="38bbe-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="38bbe-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="38bbe-152">-SubnetName</span></span>
<span data-ttu-id="38bbe-153">Namn på under nätet.</span><span class="sxs-lookup"><span data-stu-id="38bbe-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="38bbe-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="38bbe-154">-TargetScmSite</span></span>
<span data-ttu-id="38bbe-155">Regeln är avsedd för huvud webbplatsen eller SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="38bbe-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="38bbe-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="38bbe-156">-VirtualNetworkName</span></span>
<span data-ttu-id="38bbe-157">Namn på virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="38bbe-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="38bbe-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="38bbe-158">-WebAppName</span></span>
<span data-ttu-id="38bbe-159">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="38bbe-159">The name of the web app.</span></span>

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

### <span data-ttu-id="38bbe-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38bbe-160">-Confirm</span></span>
<span data-ttu-id="38bbe-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38bbe-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bbe-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bbe-162">-WhatIf</span></span>
<span data-ttu-id="38bbe-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38bbe-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38bbe-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38bbe-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bbe-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bbe-165">CommonParameters</span></span>
<span data-ttu-id="38bbe-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bbe-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bbe-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bbe-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bbe-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38bbe-168">INPUTS</span></span>

### <span data-ttu-id="38bbe-169">System. String</span><span class="sxs-lookup"><span data-stu-id="38bbe-169">System.String</span></span>

## <span data-ttu-id="38bbe-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38bbe-170">OUTPUTS</span></span>

### <span data-ttu-id="38bbe-171">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="38bbe-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="38bbe-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38bbe-172">NOTES</span></span>

## <span data-ttu-id="38bbe-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38bbe-173">RELATED LINKS</span></span>

[<span data-ttu-id="38bbe-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="38bbe-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="38bbe-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="38bbe-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="38bbe-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="38bbe-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
