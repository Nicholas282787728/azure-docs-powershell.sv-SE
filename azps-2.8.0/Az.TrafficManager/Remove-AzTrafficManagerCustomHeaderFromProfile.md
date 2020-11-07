---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: f7870cd3c6786388e34a9b243c962aa48788f91a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921092"
---
# <span data-ttu-id="6f8e6-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="6f8e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8e6-103">Tar bort anpassad huvud information från ett lokalt Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="6f8e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f8e6-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f8e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8e6-106">Cmdleten **Remove-AzTrafficManagerCustomHeaderFromProfile** tar bort anpassad huvud information från ett lokalt Azure Traffic Manager-Profile-objekt.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="6f8e6-107">Du kan hämta en profil med hjälp av New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="6f8e6-108">Denna cmdlet fungerar på det lokala profilens objekt.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="6f8e6-109">Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="6f8e6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f8e6-110">EXAMPLES</span></span>

### <span data-ttu-id="6f8e6-111">Exempel 1: ta bort anpassad huvud information från en profil</span><span class="sxs-lookup"><span data-stu-id="6f8e6-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6f8e6-112">Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="6f8e6-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="6f8e6-113">Det andra kommandot tar bort den anpassade huvud informationen från profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6f8e6-114">Kommandot uppdaterar profilen i Traffic Manager så att den matchar det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6f8e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f8e6-115">PARAMETERS</span></span>

### <span data-ttu-id="6f8e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-116">-DefaultProfile</span></span>
<span data-ttu-id="6f8e6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8e6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f8e6-118">-Name</span></span>
<span data-ttu-id="6f8e6-119">Anger namnet på den anpassade huvud informationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="6f8e6-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="6f8e6-121">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6f8e6-122">Denna cmdlet ändrar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6f8e6-123">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6f8e6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f8e6-124">-Confirm</span></span>
<span data-ttu-id="6f8e6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f8e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f8e6-126">-WhatIf</span></span>
<span data-ttu-id="6f8e6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f8e6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f8e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8e6-129">CommonParameters</span></span>
<span data-ttu-id="6f8e6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8e6-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8e6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f8e6-132">INPUTS</span></span>

### <span data-ttu-id="6f8e6-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6f8e6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f8e6-134">OUTPUTS</span></span>

### <span data-ttu-id="6f8e6-135">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6f8e6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f8e6-136">NOTES</span></span>

## <span data-ttu-id="6f8e6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f8e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f8e6-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="6f8e6-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6f8e6-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f8e6-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
