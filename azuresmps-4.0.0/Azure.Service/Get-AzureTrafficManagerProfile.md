---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093262"
---
# <span data-ttu-id="11d5f-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="11d5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="11d5f-103">Hämtar information om en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="11d5f-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="11d5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11d5f-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11d5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11d5f-105">DESCRIPTION</span></span>
<span data-ttu-id="11d5f-106">Cmdleten **Get-AzureTrafficManagerProfile** får information om en profil i Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="11d5f-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="11d5f-107">Om du inte anger parametern *Name* visar cmdleten Traffic Manager-profilerna i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11d5f-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="11d5f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11d5f-108">EXAMPLES</span></span>

### <span data-ttu-id="11d5f-109">Exempel 1: hämta listan med profiler för Traffic Manager i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="11d5f-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="11d5f-110">Det här kommandot får listan över Traffic Manager-profiler i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="11d5f-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="11d5f-111">Exempel 2: skaffa en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="11d5f-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="11d5f-112">Det här kommandot får Traffic Manager-profilen som heter min-profil.</span><span class="sxs-lookup"><span data-stu-id="11d5f-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="11d5f-113">Exempel 3: lägga till en slut punkt till en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="11d5f-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="11d5f-114">Det här kommandot lägger till en slut punkt till en Traffic Manager-profil och sparar sedan profilen.</span><span class="sxs-lookup"><span data-stu-id="11d5f-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="11d5f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11d5f-115">PARAMETERS</span></span>

### <span data-ttu-id="11d5f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="11d5f-116">-Name</span></span>
<span data-ttu-id="11d5f-117">Anger namnet på den Traffic Manager-profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="11d5f-117">Specifies the name of the Traffic Manager profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d5f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="11d5f-118">-Profile</span></span>
<span data-ttu-id="11d5f-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="11d5f-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="11d5f-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="11d5f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d5f-121">CommonParameters</span></span>
<span data-ttu-id="11d5f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d5f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d5f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d5f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11d5f-124">INPUTS</span></span>

## <span data-ttu-id="11d5f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11d5f-125">OUTPUTS</span></span>

### <span data-ttu-id="11d5f-126">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="11d5f-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="11d5f-127">Denna cmdlet skapar ett profil objekt eller objekt för Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="11d5f-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="11d5f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11d5f-128">NOTES</span></span>

## <span data-ttu-id="11d5f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11d5f-129">RELATED LINKS</span></span>

[<span data-ttu-id="11d5f-130">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="11d5f-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="11d5f-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="11d5f-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="11d5f-133">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="11d5f-134">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="11d5f-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11d5f-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


