---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757813"
---
# <span data-ttu-id="699e4-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="699e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="699e4-102">SYNOPSIS</span></span>
<span data-ttu-id="699e4-103">Lägger till anpassad rubrik information i ett lokalt Traffic Manager-slutobjekt.</span><span class="sxs-lookup"><span data-stu-id="699e4-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="699e4-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="699e4-105">DESCRIPTION</span></span>
<span data-ttu-id="699e4-106">Cmdleten **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** lägger till anpassad huvud information i ett lokalt objekt i Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="699e4-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="699e4-107">Du kan få en slut punkt genom att använda New-AzureRmTrafficManagerEndpoint eller Get-AzureRmTrafficManagerEndpoint cmdletar.</span><span class="sxs-lookup"><span data-stu-id="699e4-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="699e4-108">Denna cmdlet fungerar med det lokala slutpunktsmapparen.</span><span class="sxs-lookup"><span data-stu-id="699e4-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="699e4-109">Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699e4-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="699e4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="699e4-110">EXAMPLES</span></span>

### <span data-ttu-id="699e4-111">Exempel 1: lägga till anpassad rubrik information i en slut punkt</span><span class="sxs-lookup"><span data-stu-id="699e4-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="699e4-112">Det första kommandot skapar en slut punkt för Azure Traffic Manager genom att använda cmdlet **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="699e4-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="699e4-113">Kommandot lagrar den lokala slut punkten i $TrafficManagerEndpoint variabel.</span><span class="sxs-lookup"><span data-stu-id="699e4-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="699e4-114">Det andra kommandot lägger till anpassad huvud information till slut punkten som lagras i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="699e4-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="699e4-115">Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="699e4-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="699e4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="699e4-116">PARAMETERS</span></span>

### <span data-ttu-id="699e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699e4-117">-DefaultProfile</span></span>
<span data-ttu-id="699e4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="699e4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699e4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="699e4-119">-Name</span></span>
<span data-ttu-id="699e4-120">Anger namnet på den anpassade rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="699e4-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="699e4-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="699e4-122">Anger ett lokalt **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="699e4-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="699e4-123">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="699e4-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="699e4-124">Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzureRmTrafficManagerEndpoint eller New-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699e4-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699e4-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="699e4-125">-Value</span></span>
<span data-ttu-id="699e4-126">Anger värdet på den anpassade huvud rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="699e4-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="699e4-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="699e4-127">-Confirm</span></span>
<span data-ttu-id="699e4-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="699e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699e4-129">-WhatIf</span></span>
<span data-ttu-id="699e4-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="699e4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="699e4-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="699e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699e4-132">CommonParameters</span></span>
<span data-ttu-id="699e4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699e4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699e4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="699e4-135">INPUTS</span></span>

### <span data-ttu-id="699e4-136">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="699e4-137">Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699e4-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="699e4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="699e4-138">OUTPUTS</span></span>

### <span data-ttu-id="699e4-139">Microsoft. Azure. commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="699e4-140">Denna cmdlet returnerar ett ändrat **TrafficManagerEndpoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="699e4-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="699e4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="699e4-141">NOTES</span></span>

## <span data-ttu-id="699e4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="699e4-142">RELATED LINKS</span></span>

[<span data-ttu-id="699e4-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="699e4-144">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="699e4-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="699e4-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="699e4-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="699e4-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
