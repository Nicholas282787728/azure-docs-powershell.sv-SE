---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099539"
---
# <span data-ttu-id="0372a-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="0372a-101">Get-AzureService</span></span>

## <span data-ttu-id="0372a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0372a-102">SYNOPSIS</span></span>
<span data-ttu-id="0372a-103">Returnerar ett objekt med information om moln tjänsterna för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0372a-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="0372a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0372a-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0372a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0372a-105">DESCRIPTION</span></span>
<span data-ttu-id="0372a-106">Cmdleten **Get-AzureService** returnerar ett List objekt med alla Azure Cloud-tjänster som är kopplade till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0372a-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="0372a-107">Om du anger *ServiceName* -parametern returnerar **Get-AzureService** information om den matchande tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0372a-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="0372a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0372a-108">EXAMPLES</span></span>

### <span data-ttu-id="0372a-109">Exempel 1: få information om alla tjänster</span><span class="sxs-lookup"><span data-stu-id="0372a-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="0372a-110">Det här kommandot returnerar ett objekt som innehåller information om alla Azure-tjänster som är kopplade till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0372a-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="0372a-111">Exempel 2: Hämta information om en viss tjänst</span><span class="sxs-lookup"><span data-stu-id="0372a-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="0372a-112">Det här kommandot returnerar information om $MySvc tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0372a-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="0372a-113">Exempel 3: Visa tillgängliga metoder och egenskaper</span><span class="sxs-lookup"><span data-stu-id="0372a-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="0372a-114">Det här kommandot visar de egenskaper och metoder som är tillgängliga i cmdleten **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="0372a-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="0372a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0372a-115">PARAMETERS</span></span>

### <span data-ttu-id="0372a-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0372a-116">-InformationAction</span></span>
<span data-ttu-id="0372a-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="0372a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0372a-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0372a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0372a-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="0372a-119">Continue</span></span>
- <span data-ttu-id="0372a-120">Över</span><span class="sxs-lookup"><span data-stu-id="0372a-120">Ignore</span></span>
- <span data-ttu-id="0372a-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="0372a-121">Inquire</span></span>
- <span data-ttu-id="0372a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0372a-122">SilentlyContinue</span></span>
- <span data-ttu-id="0372a-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="0372a-123">Stop</span></span>
- <span data-ttu-id="0372a-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="0372a-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0372a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0372a-125">-InformationVariable</span></span>
<span data-ttu-id="0372a-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="0372a-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0372a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="0372a-127">-Profile</span></span>
<span data-ttu-id="0372a-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0372a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0372a-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0372a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0372a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0372a-130">-ServiceName</span></span>
<span data-ttu-id="0372a-131">Anger namnet på den tjänst där informationen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="0372a-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0372a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0372a-132">CommonParameters</span></span>
<span data-ttu-id="0372a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0372a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0372a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0372a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0372a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0372a-135">INPUTS</span></span>

## <span data-ttu-id="0372a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0372a-136">OUTPUTS</span></span>

### <span data-ttu-id="0372a-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="0372a-137">HostedServiceContext</span></span>

## <span data-ttu-id="0372a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0372a-138">NOTES</span></span>

## <span data-ttu-id="0372a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0372a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0372a-140">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="0372a-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="0372a-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="0372a-141">Set-AzureService</span></span>](./Set-AzureService.md)


