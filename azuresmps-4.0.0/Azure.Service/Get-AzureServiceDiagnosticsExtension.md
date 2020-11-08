---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093329"
---
# <span data-ttu-id="6a67f-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6a67f-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="6a67f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a67f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a67f-103">Får tillägget Cloud Service Diagnostics installerat på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="6a67f-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="6a67f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a67f-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a67f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a67f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a67f-106">Cmdleten **Get-AzureServiceDiagnosticsExtension** får tillägget Cloud Service Diagnostics installerat på alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="6a67f-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="6a67f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a67f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a67f-108">Exempel 1: hitta tillägget service Diagnostics</span><span class="sxs-lookup"><span data-stu-id="6a67f-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="6a67f-109">Med det här kommandot får du tjänst diagnos för en tjänst i alla roller.</span><span class="sxs-lookup"><span data-stu-id="6a67f-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="6a67f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a67f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a67f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6a67f-111">-InformationAction</span></span>
<span data-ttu-id="6a67f-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="6a67f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a67f-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6a67f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a67f-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="6a67f-114">Continue</span></span>
- <span data-ttu-id="6a67f-115">Över</span><span class="sxs-lookup"><span data-stu-id="6a67f-115">Ignore</span></span>
- <span data-ttu-id="6a67f-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="6a67f-116">Inquire</span></span>
- <span data-ttu-id="6a67f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a67f-117">SilentlyContinue</span></span>
- <span data-ttu-id="6a67f-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="6a67f-118">Stop</span></span>
- <span data-ttu-id="6a67f-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="6a67f-119">Suspend</span></span>

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

### <span data-ttu-id="6a67f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a67f-120">-InformationVariable</span></span>
<span data-ttu-id="6a67f-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="6a67f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6a67f-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a67f-122">-Profile</span></span>
<span data-ttu-id="6a67f-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6a67f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a67f-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6a67f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a67f-125">-Roll</span><span class="sxs-lookup"><span data-stu-id="6a67f-125">-Role</span></span>
<span data-ttu-id="6a67f-126">Anger en matris med roller.</span><span class="sxs-lookup"><span data-stu-id="6a67f-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a67f-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6a67f-127">-ServiceName</span></span>
<span data-ttu-id="6a67f-128">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6a67f-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="6a67f-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a67f-129">-Slot</span></span>
<span data-ttu-id="6a67f-130">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="6a67f-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="6a67f-131">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="6a67f-131">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a67f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a67f-132">CommonParameters</span></span>
<span data-ttu-id="6a67f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a67f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a67f-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a67f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a67f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a67f-135">INPUTS</span></span>

## <span data-ttu-id="6a67f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a67f-136">OUTPUTS</span></span>

## <span data-ttu-id="6a67f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a67f-137">NOTES</span></span>

## <span data-ttu-id="6a67f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a67f-138">RELATED LINKS</span></span>

[<span data-ttu-id="6a67f-139">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6a67f-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="6a67f-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6a67f-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


