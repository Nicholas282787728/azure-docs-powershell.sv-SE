---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8f26030f726d472024dd788abb02e55f8eac4c6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921106"
---
# <span data-ttu-id="93ddf-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="93ddf-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="93ddf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="93ddf-103">Tar bort ett förväntat status kods område från ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="93ddf-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="93ddf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93ddf-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ddf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="93ddf-106">Cmdleten **Remove-AzTrafficManagerExpectedStatusCodeRange** tar bort ett intervall med förväntade status koder från ett lokalt Azure Traffic Manager-profil objekt.</span><span class="sxs-lookup"><span data-stu-id="93ddf-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="93ddf-107">Du kan hämta en profil med hjälp av New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="93ddf-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="93ddf-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="93ddf-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="93ddf-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ddf-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="93ddf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="93ddf-111">Exempel 1: ta bort ett intervall med status koder från en profil</span><span class="sxs-lookup"><span data-stu-id="93ddf-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="93ddf-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="93ddf-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="93ddf-113">Med det andra kommandot tas ett förväntat status kods område bort från profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="93ddf-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="93ddf-114">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="93ddf-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="93ddf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93ddf-115">PARAMETERS</span></span>

### <span data-ttu-id="93ddf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-116">-DefaultProfile</span></span>
<span data-ttu-id="93ddf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93ddf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ddf-118">-Min</span><span class="sxs-lookup"><span data-stu-id="93ddf-118">-Min</span></span>
<span data-ttu-id="93ddf-119">Anger det lägsta värdet i intervallet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="93ddf-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="93ddf-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="93ddf-121">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="93ddf-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="93ddf-122">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="93ddf-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="93ddf-123">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="93ddf-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="93ddf-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93ddf-124">-Confirm</span></span>
<span data-ttu-id="93ddf-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93ddf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ddf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ddf-126">-WhatIf</span></span>
<span data-ttu-id="93ddf-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93ddf-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93ddf-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93ddf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ddf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ddf-129">CommonParameters</span></span>
<span data-ttu-id="93ddf-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ddf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ddf-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ddf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ddf-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93ddf-132">INPUTS</span></span>

### <span data-ttu-id="93ddf-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="93ddf-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93ddf-134">OUTPUTS</span></span>

### <span data-ttu-id="93ddf-135">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="93ddf-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93ddf-136">NOTES</span></span>

## <span data-ttu-id="93ddf-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93ddf-137">RELATED LINKS</span></span>

[<span data-ttu-id="93ddf-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="93ddf-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="93ddf-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="93ddf-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="93ddf-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
