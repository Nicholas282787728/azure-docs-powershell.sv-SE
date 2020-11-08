---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099322"
---
# <span data-ttu-id="5c66f-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c66f-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5c66f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c66f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c66f-103">Tar bort en slut punkt från en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="5c66f-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="5c66f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c66f-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c66f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c66f-105">DESCRIPTION</span></span>
<span data-ttu-id="5c66f-106">Cmdleten **Remove-AzureTrafficManagerEndpoint** tar bort en slut punkt från en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="5c66f-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5c66f-107">När du har tagit bort en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="5c66f-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5c66f-108">Denna cmdlet ansluter till Azure för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="5c66f-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="5c66f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c66f-109">EXAMPLES</span></span>

### <span data-ttu-id="5c66f-110">Exempel 1: ta bort en slut punkt från en profil</span><span class="sxs-lookup"><span data-stu-id="5c66f-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="5c66f-111">Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="5c66f-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="5c66f-112">Det andra kommandot tar bort en slut punkt som innehåller domän namnet Contoso02App.cloudapp.net från Traffic Manager-profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5c66f-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="5c66f-113">Kommandot skickar Profile-objektet till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.</span><span class="sxs-lookup"><span data-stu-id="5c66f-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="5c66f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c66f-114">PARAMETERS</span></span>

### <span data-ttu-id="5c66f-115">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="5c66f-115">-DomainName</span></span>
<span data-ttu-id="5c66f-116">Anger domän namnet för slut punkten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c66f-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c66f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5c66f-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c66f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="5c66f-118">-Profile</span></span>
<span data-ttu-id="5c66f-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5c66f-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5c66f-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5c66f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c66f-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c66f-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="5c66f-122">Anger den Traffic Manager-profil som du vill ta bort slut punkten från.</span><span class="sxs-lookup"><span data-stu-id="5c66f-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c66f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c66f-123">CommonParameters</span></span>
<span data-ttu-id="5c66f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c66f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c66f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c66f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c66f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c66f-126">INPUTS</span></span>

## <span data-ttu-id="5c66f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c66f-127">OUTPUTS</span></span>

### <span data-ttu-id="5c66f-128">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="5c66f-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="5c66f-129">Denna cmdlet skapar ett profil objekt för Traffic Manager, som innehåller information om den uppdaterade profilen.</span><span class="sxs-lookup"><span data-stu-id="5c66f-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="5c66f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c66f-130">NOTES</span></span>

## <span data-ttu-id="5c66f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c66f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c66f-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c66f-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="5c66f-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c66f-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="5c66f-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c66f-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="5c66f-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c66f-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


