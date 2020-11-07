---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921119"
---
# <span data-ttu-id="f2bcf-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f2bcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bcf-103">Uppdaterar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="f2bcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2bcf-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2bcf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bcf-106">Cmdleten **set-AzTrafficManagerProfile** uppdaterar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f2bcf-107">Denna cmdlet uppdaterar inställningarna för profilen från ett lokalt profil objekt.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="f2bcf-108">Du kan ange ett profil objekt antingen med hjälp av parametern *TrafficManagerProfile* eller genom att använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="f2bcf-109">Du kan få ett lokalt objekt som representerar en profil med hjälp av Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2bcf-110">Ändra objektet lokalt och Använd sedan **set-AzTrafficManagerProfile** för att bekräfta dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="f2bcf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2bcf-111">EXAMPLES</span></span>

### <span data-ttu-id="f2bcf-112">Exempel 1: uppdatera en profil</span><span class="sxs-lookup"><span data-stu-id="f2bcf-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f2bcf-113">Det första kommandot får en Azure Traffic Manager-profil med hjälp av Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2bcf-114">Kommandot lagrar profilen lokalt i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f2bcf-115">Det andra kommandot ändrar profilen lokalt.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="f2bcf-116">Det här kommandot inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-116">This command disables the profile.</span></span>

<span data-ttu-id="f2bcf-117">Det tredje kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f2bcf-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2bcf-118">PARAMETERS</span></span>

### <span data-ttu-id="f2bcf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-119">-DefaultProfile</span></span>
<span data-ttu-id="f2bcf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2bcf-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f2bcf-122">Anger ett lokalt **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f2bcf-123">Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="f2bcf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bcf-124">CommonParameters</span></span>
<span data-ttu-id="f2bcf-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bcf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bcf-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2bcf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bcf-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2bcf-127">INPUTS</span></span>

### <span data-ttu-id="f2bcf-128">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2bcf-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2bcf-129">OUTPUTS</span></span>

### <span data-ttu-id="f2bcf-130">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2bcf-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2bcf-131">NOTES</span></span>

## <span data-ttu-id="f2bcf-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2bcf-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2bcf-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2bcf-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2bcf-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2bcf-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2bcf-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2bcf-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2bcf-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2bcf-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


