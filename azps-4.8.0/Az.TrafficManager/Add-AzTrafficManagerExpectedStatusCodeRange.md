---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259750"
---
# <span data-ttu-id="c1d1f-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="c1d1f-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="c1d1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d1f-103">Lägger till ett förväntat status kods område i ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="c1d1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1d1f-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1d1f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d1f-106">Cmdleten **Add-AzTrafficManagerExpectedStatusCodeRange** lägger till ett intervall med förväntade status koder i ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="c1d1f-107">Du kan hämta en profil med hjälp av New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="c1d1f-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="c1d1f-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c1d1f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1d1f-110">EXAMPLES</span></span>

### <span data-ttu-id="c1d1f-111">Exempel 1: Lägg till ett förväntat status kods område i en profil</span><span class="sxs-lookup"><span data-stu-id="c1d1f-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="c1d1f-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c1d1f-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="c1d1f-113">Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="c1d1f-114">Det andra kommandot lägger till ett förväntat status kods område till profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="c1d1f-115">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="c1d1f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1d1f-116">PARAMETERS</span></span>

### <span data-ttu-id="c1d1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-117">-DefaultProfile</span></span>
<span data-ttu-id="c1d1f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d1f-119">-Max</span><span class="sxs-lookup"><span data-stu-id="c1d1f-119">-Max</span></span>
<span data-ttu-id="c1d1f-120">Anger det högsta värdet i intervallet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d1f-121">-Min</span><span class="sxs-lookup"><span data-stu-id="c1d1f-121">-Min</span></span>
<span data-ttu-id="c1d1f-122">Anger det lägsta värdet i intervallet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d1f-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="c1d1f-124">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="c1d1f-125">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c1d1f-126">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c1d1f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1d1f-127">-Confirm</span></span>
<span data-ttu-id="c1d1f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d1f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d1f-129">-WhatIf</span></span>
<span data-ttu-id="c1d1f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1d1f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d1f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d1f-132">CommonParameters</span></span>
<span data-ttu-id="c1d1f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d1f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d1f-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d1f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d1f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1d1f-135">INPUTS</span></span>

### <span data-ttu-id="c1d1f-136">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c1d1f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1d1f-137">OUTPUTS</span></span>

### <span data-ttu-id="c1d1f-138">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c1d1f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1d1f-139">NOTES</span></span>

## <span data-ttu-id="c1d1f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1d1f-140">RELATED LINKS</span></span>

[<span data-ttu-id="c1d1f-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="c1d1f-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="c1d1f-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c1d1f-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c1d1f-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
