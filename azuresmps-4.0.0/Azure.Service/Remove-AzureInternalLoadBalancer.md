---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099705"
---
# <span data-ttu-id="7c4ed-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c4ed-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="7c4ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c4ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4ed-103">Tar bort en intern belastnings Utjämnings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="7c4ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c4ed-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c4ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c4ed-105">DESCRIPTION</span></span>
<span data-ttu-id="7c4ed-106">Cmdleten **Remove-AzureInternalLoadBalancer** tar bort konfigurationen för intern belastnings utjämning från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="7c4ed-107">Om en slut punkt refererar till intern belastningsutjämnaren kan denna cmdlet inte ta bort konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="7c4ed-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c4ed-108">EXAMPLES</span></span>

### <span data-ttu-id="7c4ed-109">Exempel 1: ta bort en intern belastnings Utjämnings konfiguration</span><span class="sxs-lookup"><span data-stu-id="7c4ed-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="7c4ed-110">Det här kommandot tar bort konfigurationen för intern belastnings utjämning för tjänsten med namnet ContosoService.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="7c4ed-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c4ed-111">PARAMETERS</span></span>

### <span data-ttu-id="7c4ed-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7c4ed-112">-InformationAction</span></span>
<span data-ttu-id="7c4ed-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c4ed-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7c4ed-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c4ed-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="7c4ed-115">Continue</span></span>
- <span data-ttu-id="7c4ed-116">Över</span><span class="sxs-lookup"><span data-stu-id="7c4ed-116">Ignore</span></span>
- <span data-ttu-id="7c4ed-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="7c4ed-117">Inquire</span></span>
- <span data-ttu-id="7c4ed-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c4ed-118">SilentlyContinue</span></span>
- <span data-ttu-id="7c4ed-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="7c4ed-119">Stop</span></span>
- <span data-ttu-id="7c4ed-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="7c4ed-120">Suspend</span></span>

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

### <span data-ttu-id="7c4ed-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c4ed-121">-InformationVariable</span></span>
<span data-ttu-id="7c4ed-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7c4ed-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="7c4ed-123">-Profile</span></span>
<span data-ttu-id="7c4ed-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c4ed-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c4ed-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c4ed-126">-ServiceName</span></span>
<span data-ttu-id="7c4ed-127">Anger namnet på den tjänst som den här cmdleten tar bort en intern belastningsutjämnare från.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c4ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4ed-128">CommonParameters</span></span>
<span data-ttu-id="7c4ed-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4ed-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4ed-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c4ed-131">INPUTS</span></span>

## <span data-ttu-id="7c4ed-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c4ed-132">OUTPUTS</span></span>

### <span data-ttu-id="7c4ed-133">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="7c4ed-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="7c4ed-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c4ed-134">NOTES</span></span>

## <span data-ttu-id="7c4ed-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c4ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="7c4ed-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c4ed-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="7c4ed-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c4ed-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="7c4ed-138">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="7c4ed-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="7c4ed-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7c4ed-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


