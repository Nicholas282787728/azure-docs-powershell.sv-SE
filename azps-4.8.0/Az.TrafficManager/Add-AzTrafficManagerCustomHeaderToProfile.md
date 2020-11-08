---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262395"
---
# <span data-ttu-id="8cea0-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="8cea0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cea0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cea0-103">Lägger till anpassad rubrik information i ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea0-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="8cea0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cea0-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cea0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cea0-105">DESCRIPTION</span></span>
<span data-ttu-id="8cea0-106">Cmdleten **Add-AzTrafficManagerCustomHeaderToProfile** lägger till anpassad huvud information i ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea0-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="8cea0-107">Du kan hämta en profil med hjälp av New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="8cea0-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="8cea0-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea0-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="8cea0-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cea0-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="8cea0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cea0-110">EXAMPLES</span></span>

### <span data-ttu-id="8cea0-111">Exempel 1: lägga till anpassad rubrik information i en profil</span><span class="sxs-lookup"><span data-stu-id="8cea0-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="8cea0-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="8cea0-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="8cea0-113">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="8cea0-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="8cea0-114">Det andra kommandot lägger till anpassad huvud information till profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cea0-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="8cea0-115">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cea0-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="8cea0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cea0-116">PARAMETERS</span></span>

### <span data-ttu-id="8cea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-117">-DefaultProfile</span></span>
<span data-ttu-id="8cea0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cea0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cea0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cea0-119">-Name</span></span>
<span data-ttu-id="8cea0-120">Anger namnet på den anpassade rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="8cea0-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8cea0-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="8cea0-122">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea0-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="8cea0-123">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="8cea0-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8cea0-124">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8cea0-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8cea0-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="8cea0-125">-Value</span></span>
<span data-ttu-id="8cea0-126">Anger värdet på den anpassade huvud rubrik informationen som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="8cea0-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8cea0-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cea0-127">-Confirm</span></span>
<span data-ttu-id="8cea0-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cea0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cea0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cea0-129">-WhatIf</span></span>
<span data-ttu-id="8cea0-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cea0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cea0-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cea0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cea0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cea0-132">CommonParameters</span></span>
<span data-ttu-id="8cea0-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cea0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cea0-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cea0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cea0-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cea0-135">INPUTS</span></span>

### <span data-ttu-id="8cea0-136">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8cea0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cea0-137">OUTPUTS</span></span>

### <span data-ttu-id="8cea0-138">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8cea0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cea0-139">NOTES</span></span>

## <span data-ttu-id="8cea0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cea0-140">RELATED LINKS</span></span>

[<span data-ttu-id="8cea0-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="8cea0-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8cea0-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8cea0-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
