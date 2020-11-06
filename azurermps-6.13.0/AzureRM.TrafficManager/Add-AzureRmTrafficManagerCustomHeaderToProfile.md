---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584816"
---
# <span data-ttu-id="2bd56-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="2bd56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bd56-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd56-103">Lägger till anpassad rubrik information i ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bd56-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bd56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bd56-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd56-106">Cmdleten **Add-AzureRmTrafficManagerCustomHeaderToProfile** lägger till anpassad huvud information i ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-106">The **Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2bd56-107">Du kan hämta en profil med hjälp av New-AzureRmTrafficManagerProfile eller Get-AzureRmTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="2bd56-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="2bd56-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2bd56-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd56-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="2bd56-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bd56-110">EXAMPLES</span></span>

### <span data-ttu-id="2bd56-111">Exempel 1: lägga till anpassad rubrik information i en profil</span><span class="sxs-lookup"><span data-stu-id="2bd56-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2bd56-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="2bd56-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2bd56-113">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="2bd56-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="2bd56-114">Det andra kommandot lägger till anpassad huvud information till profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2bd56-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2bd56-115">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2bd56-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2bd56-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bd56-116">PARAMETERS</span></span>

### <span data-ttu-id="2bd56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-117">-DefaultProfile</span></span>
<span data-ttu-id="2bd56-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd56-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd56-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bd56-119">-Name</span></span>
<span data-ttu-id="2bd56-120">Anger namnet på den anpassade rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2bd56-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2bd56-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="2bd56-122">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2bd56-123">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2bd56-124">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2bd56-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd56-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="2bd56-125">-Value</span></span>
<span data-ttu-id="2bd56-126">Anger värdet på den anpassade huvud rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="2bd56-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2bd56-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bd56-127">-Confirm</span></span>
<span data-ttu-id="2bd56-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bd56-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd56-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd56-129">-WhatIf</span></span>
<span data-ttu-id="2bd56-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bd56-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd56-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bd56-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd56-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd56-132">CommonParameters</span></span>
<span data-ttu-id="2bd56-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd56-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd56-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd56-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd56-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bd56-135">INPUTS</span></span>

### <span data-ttu-id="2bd56-136">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2bd56-137">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd56-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="2bd56-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bd56-138">OUTPUTS</span></span>

### <span data-ttu-id="2bd56-139">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2bd56-140">Denna cmdlet returnerar ett ändrat **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2bd56-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2bd56-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bd56-141">NOTES</span></span>

## <span data-ttu-id="2bd56-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bd56-142">RELATED LINKS</span></span>

[<span data-ttu-id="2bd56-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="2bd56-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2bd56-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2bd56-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
